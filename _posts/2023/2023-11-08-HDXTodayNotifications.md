---
title:  "HDX Today - The Notifications Issue (+Theme Persistence!)"
toc: true
categories:
  Acxiom
tags:
  GameDev
  CultivatingCompetencies
  AppDev
  HendrixToday
---

Notifications are working! Theme Persistence is on the HDXToday App!

## Hendrix Today App

### Notifications

Over the past month we have been working tirelessly to get notifications working. Especially on iPhone.
Well I am happy to report that they are not fully working on all devices that I have tested this on!
This was a tiring process of first getting them working on Android, which was the easier problem, and then working to get the app to build and work on iPhone.
I ran into a ton of problems during this.
The main problem was that the APNS token was not being sent to Firebase before receiving the FCM token for notifications.
This meant that we couldn't subscribe to the "new_events" topic, or any others that could be made in the future.
To get this functioning I had to first make a lot of changes to the AppDelegate.swift file as shown below.

#### Previous AppDelegate.swift

``` swift
import UIKit
import Flutter

@UIApplicationMain
@objc class AppDelegate: FlutterAppDelegate {
  override func application(
    _ application: UIApplication,
    didFinishLaunchingWithOptions launchOptions: [UIApplication.LaunchOptionsKey: Any]?
  ) -> Bool {
    GeneratedPluginRegistrant.register(with: self)
    return super.application(application, didFinishLaunchingWithOptions: launchOptions)
  }
}
```

#### New AppDelegate.swift

``` swift
import UIKit
import FirebaseMessaging
import Flutter

@UIApplicationMain
@objc class AppDelegate: FlutterAppDelegate {
  override func application(
    _ application: UIApplication,
    didFinishLaunchingWithOptions launchOptions: [UIApplication.LaunchOptionsKey: Any]?
  ) -> Bool {
      UNUserNotificationCenter.current().delegate = self
          let authOptions: UNAuthorizationOptions = [.alert, .badge, .sound]
          UNUserNotificationCenter.current().requestAuthorization(
              options: authOptions) { _, _ in }
          application.registerForRemoteNotifications()
    GeneratedPluginRegistrant.register(with: self)
    return super.application(application, didFinishLaunchingWithOptions: launchOptions)
  }
    override func userNotificationCenter(
            _ center: UNUserNotificationCenter,
            willPresent notification: UNNotification,
            withCompletionHandler completionHandler:
            @escaping (UNNotificationPresentationOptions) -> Void
            ) {
              if #available(iOS 14.0, *) {
                  completionHandler([[.banner, .sound]])
              } else {
                  // Fallback on earlier versions
              }
        }

    override func userNotificationCenter(
            _ center: UNUserNotificationCenter,
            didReceive response: UNNotificationResponse,
            withCompletionHandler completionHandler: @escaping () -> Void
          ) {
            completionHandler()
          }
    override func application(
          _ application: UIApplication,
          didRegisterForRemoteNotificationsWithDeviceToken deviceToken: Data
        ) {
          Messaging.messaging().apnsToken = deviceToken
            Messaging.messaging().subscribe(toTopic: "new_events")
        }
}
```

This stopped the previous errors, but I was still running into them, so I continued looking for a solution.
Finally, during the meeting last week I found that the reason this wasn't working was that I wasn't on the right development group in Xcode.
Upon switching this and a plethora of testing, I found that the notifications where now working!

![Hendrix Today Notification](/blog/assets/img/blog/HDX_Notifs.png)

After pushing this, I ran into a weird issue where I couldn't get the app to run anymore.

<img align="right" width="100" height="100" src="/blog/assets/img/blog/HDX_Install_Error.png">

It was constantly showing up this message no matter how much I updated my software, my operating systems, or anything.
So, I was at this for a few hours trying to figure out what could have caused this issue.
I was looking up all sorts of things, trying what other people did, looking for the certificate in VPN & Devices, but nothing would work.
Then, I finally decided to completely delete the repository off of my computer and reinstall it... And it worked.
This is frustrating that I didn't do this initially, but at least it is working now!

### Theme Persistence

One major issue that I decided to work on last night was theme persistence.
Currently in the app build, if someone decided to change their theme then it will always put them in dark mode, they could change this to light mode,
but then every time they restarted the app it would reset their mode back to dark.
Obviously, this is not the intended effect.
Therefor, I looked into this issue using the [link]("https://stackoverflow.com/questions/75570316/dark-mode-flutter-with-shared-preferences-and-provider") that Dr. Goadrich provided.
This was an amazing starting point and I immediately got to working on implementing this.
After a couple hours of getting it to run, it almost ran perfectly first time!
However, the app wouldn't show which state it was in on the setting to switch the mode until you flipped it once, and it would always be in light mode upon a fresh install.
Both of these were easy fixes! Turns out, for the switch I was looking at the wrong variable, so I changed the value back to what it previously was,
`Theme.of(context).brightness == Brightness.dark;`.
For the initial install of the app, what I really wanted was it to start with your system preferences. This was a simple case of separating out the conditionals to make null values tell the app that it needs to use the system settings, since null means that it hasn't been set before.

``` dart
  getThemeAtInit() async {
    SharedPreferences sharedPreferences = await SharedPreferences.getInstance();
    bool? isDarkTheme = sharedPreferences.getBool("is_dark");
    if (isDarkTheme == null) {
      themeMode = ThemeMode.system;
    } else if (isDarkTheme) {
      themeMode = ThemeMode.dark;
    } else {
      themeMode = ThemeMode.light;
    }
    notifyListeners();
  }
```

Now, I can safely say that everything is working as intended.

## What's Coming Up?

- Continue working on a better landing page for this blog. (one day)
- Change "Projects" page to be a portfolio.
- Edit all the pages connected to the WIP landing page.

## TL;DR

- Notifications are now working for IOS and Android
- Theme Persistence is now working upon app restarts

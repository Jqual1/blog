---
title:  "Lake Nixon Scheduler Android Working!"
toc: true
categories:
  DiscoTrayStudios
tags:
  AppDev
  LakeNixonScheduler
  Acxiom
---

This semester has been one of my busiest.
While I haven't had too difficult classes, I have been doing a lot around Hendrix, been apartment hunting, been job hunting, and much more.
We had Spring Break though! My final one that is.
As I reach graduation I am getting more nervous, but excited about what the future has in store for me.
My future roommate and I have also found a place that we really like here in Conway called Orso Vista.
It was just built last year, it looks nice, feels spactious, has no carpet, isn't too expensive, and is in a good area!
We toured 6 different apartments over the break, so it was nice that we could find something that we really liked.

Speaking of the break, over Spring Break I went to Branson for a day with my current roommate, and really just spent a lot of time relaxing and having fun. It was definitely needed.

## Lake Nixon Scheduler

This past week I was able to get the Lake Nixon Scheduler working for Beta Tests on Google Play! 
This was something that was quite difficult to accomplish, but most of that was because of all the different pages that the guide kept linking me to.
[Here]('https://docs.flutter.dev/deployment/android') is the guide that I was using. It is the Flutter Android deployment document.
What I ended up doing was overthinking every time there was a link, clicking on it, and following a new guide for a specific section of the guide.
It was overwhelming, and it turns out that I could do a majority of it without even clicking these external links.

One issue that I ran into during this was that the package name was `final_project` rather than `lake_nixon_scheduler`.
Due to this, the deployment of the android build took a bit longer than expected.
I knew that I didn't want the package to stay this way if we were entering deployment, so I changed it in just one place at first.
This ended up stopping the app from working.
Because the config was changed, it was searching for a different package rather than what was being provided and was crashing every time the app was opened.
I didn't understand what went wrong at first, but then figured out that I needed to go through the entire program and replace every `final_project` with `lake_nixon_scheduler`.

Once this was all fixed, I was able to upload the app again with almost no issue.
The only issue left was that I needed to update the build number.
At first I was confused and updated the version number only to find out that it still wouldn't upload.
For future reference, in the config our version is 1.0.0+1.
Everything before the + is the version number.
Everything after the + is the build number.
Now with this all done, I was able to upload the app for closed beta testing successfully.

## Acxiom

At Acxiom, I have been working hard to make sure that all of my tasks get complete, but it is difficult to stay on top of everything.
The final day of my internship is May 10th, so I need to make sure that there are some people on my team that can continue my work on the internal website before then.
I am also making sure that nothing is lost once I leave. This will make sure that the things that I have helped start continue.
Unfortunately, my team doesn't have the budget to hire me on full-time, but currently I am pursueing a position on another team and working on applying to other places.


## What's Coming Up?

- Continue working on a better landing page for this blog. (one day)
- Change "Projects" page to be a portfolio.
- Edit all the pages connected to the WIP landing page.

## TL;DR

- Spring Break was needed
  - I went apartment hunting
  - I went job hunting
- Lake Nixon Scheduler is now on Google Play for closed testing
  - I struggled with this
- My last day as an intern is May 10th
- The next stage of life approaches

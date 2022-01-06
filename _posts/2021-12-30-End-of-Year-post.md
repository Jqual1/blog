---
title:  "End of Year Update"
categories:
  DiscoTrayStudios
tags:
  DiscoTrayStudios
  GameDev
  @itsmaya
  ClimateGoesPolitical
---

A lot has been going on this past month. Much work has been done to both @itsmaya and Climate Goes Political.
For a list of updates, scroll to the "-={Comprehensive Lists}=-" section.
As a quick update on my life, I have been spending time with my family this Christmas and just focusing on my mental health for a bit.
I will continue to go back to work at Walmart Neighborhood market tomorrow, but this week's break has been nice.
Some focuses of mine have been art and writing while I watch things, and that has gone well.
It feels good to do things in my free time that could also help me with DiscoTrayStudios in the future.
I may include a section for showcasing my art as well on this website in the future.

On @itsmaya I worked on the mechanics and visuals of the game.
To start off with, I added Ian and I to the Credits.
I then added and improved all things referring to the character walking animations.
This included making sure the characters were always visible when they were supposed to be and have them walk at a pace slower than the speed of light.
Then I turned my focus to creating a decision timer.
This stops the player from taking too long when faced with a choice from the characters.
The length of the timer can be changed to a different preset in the new settings menu located on the main menu.
This new settings menu also includes the ability to change the volume of the music, other, or the master volume.
Along with the new menu, I polished up restarting the game, so now everything resets when the game restart.
Now when you are playing the game the next button is not always visible.
It will be gone while the text is typing, but if you click on the text box, the text will finish typing and the next button will appear.
Throughout the time I have spent working on this game, I have also worked on polishing up a lot of bugs that can be seen below.

On Climate Goes Political I did a lot of similar things.
I created a settings menu that incorporates the same options for audio and the timer.
While I haven't implemented the timer yet, I at least have the options there for future implementation.
Working on the UI and animations of this new menu was difficult.
It felt nice to take a break from @itsmaya, but I was intimidated on working on the game again.
After I got working on it though, everything felt like it was coming together pretty quickly.
However, when I finished as tried to save, Unity crashed.
This was devastating as I had to figure out how to redo everything that I had just done.
Needless to say, I will be saving my progress much more frequently.

In the future, I will be working on making an animation or effect to make the capital face changes more noticeable.
This could be a shaking animation or something similar.
Also there is a bug in @itsmaya that happens when the player goes to the menu during a choice.
After going back to play the game, the choice is the first thing the player sees and then the game starts from the beginning.
This is an odd bug that I am looking into.
Other things I will be looking at includes changing the dialogue depending on the choice.
In Climate Goes Political, I want to focus on implementing a timer and changing the map to be a zoomed out view, with ways to zoom into each city.

I hope to also focus on revamping this website to be a lot more personalized.
I feel it could be beneficial to include more information on some of the pages and to move things around.
Changes have already begun being made this week, and hopefully more will be made as the week draws on.

Since I won't be making another post soon, Happy New Year!
May 2022 be a great year for everyone.

## -={Comprehensive Lists}=- ##
#### List of Updates on <b> @itsmaya: </b> ####
- Added Ian and Jonathon to the Credits
- Added Character Animations
- Updated the Character Animations
- Added a Timer on Decisions
- Added a Settings Screen
- Added a Settings Button to Main Menu
- Put Sound on Settings Screen
- Separated Sound into 3 Options (Master, Music, Other)
- Removed Sound Icon
- Added a Decision Timer
- Added Timer Options onto Settings Screen (30 seconds, 15 seconds, No Timer)
- Changed the Relationship between Arrows and Faces
(if there is an arrow, the face will change)
- Added a black outline to the Arrows so that it is more visible
- Made the Credits more visible
- Capital change arrows are disabled at the start
- Reset the Policies on restart
(Included resetting the colors of policies back to #737373)
- Reset the Capital on restart
- Reset the Faces on restart
- Reset the Background on restart
- Removed the Next Button while Dialogue Coroutine is active
(aka the text is typing)
- Added functionality for clicking on the text box to finish Dialogue Coroutine
- Dialogue Box now hides when the Policy Screen shows
- Timer Pauses when the Game is Paused

#### Bug Fixes on <b> @itsmaya: </b> ####
- Background Scaling Bug
- Credit Background not showing Bug
- Characters not showing up Bug
- The above bugs where fixed by changing things from sprites to UI images
- Dialogue showing on Credits Screen Bug
- Capital Panel showing on Credits Screen Bug
- Dialogue Box being clickable while animating away Bug

#### List of Updates on <b> Climate Goes Political </b> ####
- Separated Sound into 3 Options (Master, Music, Other)
- Added A Settings Button to Main Menu
- Added a Settings Screen
- Put sound on Settings Screen
- Added Timer Options onto Settings Screen (30 seconds, 15 seconds, No Timer)
- Updated Show/Hide Animations to account for the new Settings button
- Removed Volume Icon
- Made an animation for the Settings Screen

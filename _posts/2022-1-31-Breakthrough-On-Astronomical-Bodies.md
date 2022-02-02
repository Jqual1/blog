---
title:  "Breakthrough on Astronomical Bodies"
categories:
  DiscoTrayStudios
tags:
  DiscoTrayStudios
  GameDev
  @itsmaya
  ClimateGoesPolitical
  AstroBodies
---

This week felt very productive, but also very stressful as I tried to catch up on all of my classes.
Homework seemed to be pouring out of my classes and I had to dedicate my entire weekend to both Disco Tray Studios and my homework. It was difficult to get caught up, but it was relieving to finally get to where I am.

In @itsmaya I pixelated part of the sound sliders to make it more consistent with the game.
I also fixed bugs regarding the timer not choosing an option, and choosing the wrong option occasionally.
I changed the policy screen to where the done button is no more and the enact button will only show up when a policy is selected.
Additionally, I switched the lighting for the policies to be brighter when they are not active and darker when they are active to show that you can no longer choose them.
I am currently working on fixing bugs in @itsmaya, but every bug I fix, another one appears.
One of those bugs is that the Dialogue box is not going away on the policy screen anymore, but it isn't that noticeable.

I purchased some new textbooks for programming, some of which happened to be unity textbooks.
One of these textbooks was about improving performance in games, so I just knew I had to have it.
As I read through it i began looking at the game with the most performance issues, Astronomical Bodies.
After a little bit of debugging and searching for sources of the problem in the profiler, it turned out that I could fix it in the Unity Project Settings.
It turned out that the Timesteps and Time Scale were too big making it to where too many function calls were happening every second.
Once this was fixed, the game stopped lagging, so I decided to remove the cap limiting the amount of planets, and I updated the [itch.io](https://discotraystudios.itch.io/astronomical-bodies) page.

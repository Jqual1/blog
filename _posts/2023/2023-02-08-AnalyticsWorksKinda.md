---
title:  "Analytics (Sort of) Works!"
toc: true
categories:
  DiscoTrayStudios
  Acxiom
tags:
  GameDev
  CultivatingCompetencies
  Internship
---

The past two weeks have been very eventful,
school got canceled a couple of times due to an ice storm,
one of my team members left at work and he left me a couple of his projects,
we made a lot of progress on Cultivating Competencies, and
I've been working hard at self-improvement.
There has been so much more leisure time in my life this semester.
I am so excited about it. I love my classes as well, so thats a big plus.
Work, school, and life are making me happy.

## Cultivating Competencies

Good news and bad news! First of all, analytics is passing us data now!
We have most of the events in the game and are getting analytics from these with the following code!
``` python
  # Dict to Json
  # Difference is { "test":10, "test2":20 }
  data = json.dumps(data)
  # Convert to String
  data = str(data)
  # Convert string to byte
  data = data.encode('utf-8')
  # Post Method is invoked if data != None
  req =  request.Request(f'https://www.google-analytics.com/mp/collect?measurement_id={measurement_id}&api_secret={api_secret}', data=data)
  # Response
  resp = request.urlopen(req, cafile=certifi.where())
```
It is differentiating users, but it is not letting us look at individual users to see an individuals choices currently. That is one thing we are working on. We are working on how to fix this and how to get more data, if possible. One issue has arose as well though. When playing the game on the web, we run into an error when it tries to send the analytics.
This error is: **`ValueError: SSL support not available`**. Now, this was an error that I got originally,
but I was able to fix it by including `certifi`. For some reason, however, this doesn't seem to work here.
I am actively looking into the issue, because this is the last thing that we need.
After this, we focus on other games, and I might help with some of the app projects.

## Acxiom

These past two weeks at Acxiom have been insane.
I am getting invited to help or to work on many more projects.
As my coworker was preparing to leave, I got invited a lot of training/handoff meetings,
and so I spent most of last week in meetings.
Then, I started working on the internal React website Monday
and was able to get a view for a table I wanted successfully implemented by the end of the day!
Yesterday, I worked on a separate analysis project and then focused on the website again for the last hour.
I made quick progress in both things.
I even heard back from the people transferring everyone from using BitBucket to GitHub on Monday.
However, it turns out that, since we plan to use it on our server that we store our code on,
we will have to wait for them to develop a solution for access to GitHub.
An alternative thing we could do is keep the repository on our personal machines and then just push the current code to the server for now. I'll have to discuss this with my team though.

Overall, a good two weeks. A lot has happened that has kept me busy,
and I am excited to see where all of these projects go!

## What's Coming Up?

- Figure out the SSL support not available bug.
- Add more analytics data.
- Get a section of the Acxiom internal website working.
- Continue working on a better landing page for this blog.
- Change "Projects" page to be a portfolio.
- Edit all the pages connected to the WIP landing page.

## TL;DR

- I've had more leisure time (so I'm less likely to burn out)
- We got analytics working on the Cultivating Competencies app version
  - But ran into an issue of the web version
- I am now the owner of an internal website as well as other projects

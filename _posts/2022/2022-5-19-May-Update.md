---
title:  "May Update, Pre internship"
toc: true
toc_label: ""
toc_icon: "cog"
categories:
  DiscoTrayStudios
  Acxiom
tags:
  GameDev
  AstroBodies
  CultivatingCompetencies
  ClimateGoesPolitical
  Internship
---

This is a long post, but keep in mind that you can use the Table of Contents on the right!

## General Life Updates

This month has been pretty good overall!
I went through the process of getting a new truck because my car kept having issues.
This has been financially stressful, but the internship at Acxiom will help greatly for financing this vehicle.
Why a truck? Because it makes moving easier, and I know that I will be moving at least twice in the next 2 years.
First I will be moving into summer housing, which is also my housing for next school year at Hendrix.
Then I will be moving after my senior year is over with.
Therefore, either a truck or a SUV were clearly the best choices.
In other news, since I got the Acxiom internship, I quit Walmart!

I ended this semester with all A's and have been enjoying this time without schoolwork.
One of the ways I have done so is by cooking almost every day with a friend!
It is a lot of fun learning new recipes and just working with whatever we have.
I was worried about how my mental health would fair over the summer, but I have a few new summer friends,
and so far everything has been going good. It has been a lot of fun!

## Disco Tray Studios

### Art Game

On May 5th, Ian and I had a meeting with Lindsey Knight, the Education Curator at the Windgate Museum.
In this meeting we talked a lot about the game that she would like to be made.
This will be a bigger project since we will have to start over, but we bounced a lot of ideas off of eachother and hope to be able to start in September.
She is very lenient on how the game is shown to the user, but she definitely wants a more fleshed out story, even if it isn't a story game.
Make things intentional and give the player a reason to be there.
She wants a 3D game with a birdseye view with inspiration being drawn from Mario 64 and Mario's time machine for how the game can play out.
Another thing Lindsey mentioned was her love of lore and creepyness, so if there is a way to include that, she would love it.

How might this be included? The lore of the art itself.
The different pieces of art may have a dark backstory that we don't know about, so it would be highly reccomended to speak with any living artists of these pieces.
Pieces that will be included in the game are going to be the permanent ones. These can be found all around campus as lobby pieces, room decoration, or something else.
Overall, there are many different ways that this project will go and I think that it will be fun to work on it.

### Play Make Learn Prep

Since we are going to Play Make Learn in August, I have been working to make sure that all of the games that we plan to submit for a GEE! Learning Games Award
are ready for submission by June 1st.
This means that I have had to check for bugs, make sure that all the assets are attributed, and make sure we are happy with how the games play.
The games we plan to submit are Astronomical Bodies, Climate Goes Political, @itsmaya, and Cultivating Competencies,
so it's been very important that we improve these however possible before June.
One of the ways we are doing this is by switching from Trello to GitHub Issues.
This way we can keep track of everything quicker and easier.
At first GitHub Issues wasn't enabled on the repositories, but that has since been fixed.

The rest of our prep will be for our 15 minute presentation at Play Make Learn.
I think discussion about this will really kick off in July as the date nears for the conference.

### Cultivating Competencies

This month we got feedback from Career Services about the newest version of Cultivating Competencies that we sent to them.
They shared this with two of their student workers to recieve feedback.
The feedback that we recieved from them was extremely useful!
It included:

- Grammer Corrections
- Likes/Dislikes
- Missing Avatars
- Wording
- Other General Feedback

After getting this feedback I was able to make quick changes to the game.
All the feedback was detailed enough to allow me to find grammer corrections and such easily.
I put all of the feedback into an obsidian file to be able to read it all easier and then started crossing things off as I did them.
I was also sure to start putting these in as GitHub Issues since we are transferring from Trello to that.
GitHub Issues definitely feels a lot more convenient to use once it is all set up.

One of the feedback we recieved was that we should find another way to display the Career Competencies.
The solution I came up with is to show a list of options to choose from to learn about.
This way the player has a choice of if they with to learn about them all or just a couple of them that they aren't sure about.
It also makes sure that there is never a huge block of text.

Another thing I changed was the main menu background.
The main menu didn't look amazing so I made a new background with a different picture of the SLTC.
After using LunaPic to add the filter to the picture, I used Canva to arrange the layers and add text.
Currently, the working name for the game is Cultivating Competencies, so I was sure that that was on the title screen.

Additionally, now that there are fewer people on campus, I was able to go around and take some pictures of places we needed in the game.
We now have an empty Couch Hall room, the snoddy center, a study corral, and mills. The current version of the game has been sent off for review by Career Services once more.

### Climate Goes Political

I've been working on the world of Climate Goes Political for a while now.
It has been a lot of effort to go through and change each version of the cities and land around them to fit the new design plans and make them look different enough.
However, this has been very rewarding.
Now, when one looks at the cities from afar, it is much easier to differentiate them from eachother.
I ended up zooming the camera back in for the time being, but it is in the plans for the future to enable some kind of zoomed-out camera.
Simply put, my energy is better spent on making sure the other games are ready for submission seeing that this game is already in a good place.
This new version that I have been working on throughout the semester is now on [itch.io](https://discotraystudios.itch.io/climate-goes-political).
Version 2.1 includes many new features:

- New Settings Menu
  - New Timer Feature
  - Seperate Master, Music, and Other sound controls
- Differentiation in cities
- Probably Brand New Bugs Somewhere!
- Much more detailed land in-between cities with hills and rivers.

### Astronomical Bodies

When looking through Astronomical Bodies to make sure everything was credited, I noticed that there where a few issues present:

- Objects were being culled when they got a certain distance away from the original center.
  - This happened even if no other objes were present
- No Center of Gravity Marker
- Automatic Camera Zoom was slow
- Manual Scrolling Zoom was slow

Once I saw these issues I began looking at the code once more.
It turns out that somewhere along the way we changed the code in such a way that the center of gravity was no longer updated!
After fixed this issue in the code, the object culling improved, however, I wanted to allow objects to be further away from eachother.
So, I increased the range from the center before culling happens.
Next was camera zooming issues, these were easy to fix. All I needed to do was change the numbers that each thing was being multiplied by.
One thing I wanted to do though was make it to where even if you were zoomed out a lot you could zoom back in really quick.
To do this I made a multiplier that increases as you zoom out and decreases as you zoom in.
This makes zooming a lot less effort, and I think it is a good improvement.

## Acxiom Internship Prep

I have already learned a lot about the process of starting a new, more serious, job!
For the first time ever, I had to go through a background check and a drug test.
Both were pretty simple processes, but I did hit a few snags when going through the background check.
In the background check, I forgot to take out my first ever "experience" on my resume.
This was something that I did when I was just under 14 with my uncle and, therefore, didn't have any tax paperwork to prove I was employed.
It was just something that my uncled payed me for doing that I put on my resume to show that I could handle labor when I started applying to jobs.
Now, however, I have that removed from my resume. It is no longer necessary to have on there and will make for less of a headache in the future.
Besides that snag, the background check went and drug test went well!

On the Hendrix side of things, I went through Career Services and got everything approved through them to do the internship for Odyssey credit and stay over the summer.
This took a while to get approved, but now I just have to wait until the 26th to move into summer housing.
I am making sure to do all of the Professional Development Seminar stuff as I go for Career Services as is required by the college.
I start at Acxiom on the 23rd and I so am excited to begin! I am sure I will learn many career competencies while I am there!

## Blog Work

I have taken some time to work on my blog a little more this month.
The game-dev page is slowly getting more fleshed out and will lay the way for the web-dev and app-dev pages.
Also, the page that was previously named "home" is now the "portfolio" page. This renders the "projects" page useless.
I will be transferring any information from there to other parts of this website.
One may notice that these changes are in affect on the nav-bar already.

## What's Coming Up?

- Start internship at Acxiom
- Finish up Cultivating Competencies for Submission.
- Continue working on a better landing page for this blog.
- Create a logo for my blog (Might be done? Unsure)
- Change "Projects" page to be a portfolio.
- Edit all the pages connected to the WIP landing page.

## TL;DR

- Personal
  - New Truck
  - All A's
  - Cooking a lot
  - Quit Walmart
- Disco Tray Studios
  - Art Game
    - Had a meeting with a lot of ideas
    - Hoping to start work in Sept
  - Play Make Learn Prep
    - Had a meeting
    - Plan to submit 4 games for Gee Award
    - Switching to GitHub Issues
    - We will have a 15 min presentation
  - Cultivating Competencies
    - Received Feedback from Career Services
    - Made suggested changes
    - Changed how Career Competencies are Displayed
    - Changed the main menu background
    - Added new backgrounds and avatars
    - Uploaded to itch
  - Climate Goes Political
    - Finshed making the cities more varied
    - Uploaded to itch
  - Astronomical Bodies
    - Fixed Center of Gravity
    - Fixed Culling of Far Objects
    - Fixed Camera Zooming issues
    - Uploaded to itch
- Acxiom Internship Prep
  - Went through a background check and drug test
  - Got everything approved through Career Services
  - I start on the 23rd
- Blog Work
  - Updated game-dev page
  - New "portfolio" page

---
title:  "A Working Game!"
toc: true
categories:
  DiscoTrayStudios
  Acxiom
tags:
  GameDev
  TempestWinds
  Internship
---

This past week has been busy all around, but I was able to get a few things done regarding Tempest Winds still.
Also, my choir concert was last night, and it went well!
I had a solo that a lot of people loved, and people were saying that I was radiating confidence.
It was a nice break from my school work even though it took away some of the time that I had to work on things.

## Tempest Winds

This week I have spent a decent amount of time polishing up the Dialogue. I fixed typos, made character names consistent,
and fixed a couple of bugs that were surrounding it. The first of these bugs was that it was typing out things like
\<I>, \<B>, etc slowly rather than just putting it on the screen with the player not being able to see it.
It makes the players think they they could've missed dialogue, or something similar,
because it typed out these italics or bold tags and then they would disappear.
Another bug that I fixed was that there was white space appearing at the beginning of each dialogue.
It wasn't noticeable in the one-liner dialogues, but when there were multiple lines, it became very noticeable.
This turned out to just be a problem with how our coroutine was set up.
It was set to put a space before it started typing any words, so that has now been fixed as well with the following:

``` C#
    private IEnumerator typeText()
    {
        
        List<string> textList = fullDialogueText.Split(' ').ToList<string>();
        isTyping = true;
        dialogueText.text = "";
        int curChars = 0;
        foreach (string word in textList)
        {
            if (curChars + word.Length > 200)
            {
                while (!Input.GetMouseButtonDown(0))
                {
                    isTooLong = true;
                    yield return null;
                }
                timeBetweenChars = 0.03f;
                isTooLong = false;
                curChars = 0;
                dialogueText.text = "";

                isWaitingBetweenChars = true;
            }
            if (dialogueText.text != "") {dialogueText.text += " ";}
            foreach (char c in word)
            {
                dialogueText.text += c;
                curChars++;
                if (c == '<')
                {
                    isWaitingBetweenChars = false;
                }
                if (c == '>')
                {
                    isWaitingBetweenChars = true;
                }
                if (isWaitingBetweenChars)
                {
                    yield return new WaitForSeconds(timeBetweenChars);
                }
            }
        }

        isWaitingBetweenChars = true;
        isTyping = false;
        yield return null;

    }
```

One other thing I was working on that I thought would be easy to figure out but turned out to take time away from everything else
was the volume slider bugs.
So, to preface, the volume slider is not moving for some reason and, because of that, the user are not able to change the volume.
On top of this, some users were getting trapped in this settings screen that allowed you to adjust the volume.
I thought maybe it was an issue with how we were setting the volume, so I created a volume mixer and set all volumes to be in it.
Then, I tried to make sure everything else was disable while I was trying to use the slider, but it still wasn't working.
I thought the issue might be [this](https://answers.unity.com/questions/945148/ui-sliders-1.html), but our Canvas is already Screen Overlay instead of Camera Space. I will be continuing to work on this as much as I can before our meeting today.

## Acxiom

At Acxiom, I have been working hard to make sure I deliver on what my team expects from me,
but have also slowed down a little bit due to the final projects I am working on.
It has just gotten harder to put my focus on any one things. This week I could have to take some time off.
Some progress is still being made on my projects, just slower than normal.
My team knows that it is finals time though, so they know I have less time and mental energy.

## What's Coming Up?

- Fix a lot of the bugs in **Tempest Winds**
- Set up that meeting with our client from the Art Museum.
- Continue working on a better landing page for this blog.
- Change "Projects" page to be a portfolio.
- Edit all the pages connected to the WIP landing page.

## TL;DR

- Fixed a few Tempest Winds Bugs:
  - Fixed typos in the dialogue
  - Fixed leading white space issue
  - Fixed \<I>, \<B>, etc. tags typing out in the coroutine
- Attempted to fix the volume slider related bugs
  - Changed the audio to use an audio mixer
  - Tried to just disable everything that wasn't being used
  - Slider is still not adjustable

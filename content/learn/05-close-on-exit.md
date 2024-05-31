---
title: How to close the Terminal window on 'shell' exit
description: Ellane finds the option in Terminal, and has a tech support issue.
author: Ellane
date: 2024-05-31T03:27:44
tags:
  - concept
mastodon: https://pkm.social/@ellane/112528946316189230
---

## Homework assignment part 1

> Figure out how to make it so that when you type `logout`, the window closes.

I poked around in Settings, and found an option under Shell called **When the shell exits**. The default behaviour was **Don’t close the window**, which was just the clue I needed!

As I’d hoped, **Close the window** was also an option in the drop down list.

## Homework assignment part 2

> Why doesn’t Johnny like closing the window with the red button?

I couldn’t find a clear answer to this, so here’s my best guess: Using the red button might run the risk of closing the window before a process has completed successfully, leading to problems.

Is it like leaving the car in a gear other than Park before turning it off?

---

# A tech support question

This lesson also brought up one of the frustrations I’ve faced in the past when trying to use Terminal.

I’ve pasted in the string I was given (in this case, `printenv`), pressed `Enter`, and a process completed successfully. I then wanted to do something else, but nothing I typed showed up on the screen, even though there was a blinking cursor.

What am I missing? Surely the answer isn’t to close the window and open a new one, is it, but if so, why?

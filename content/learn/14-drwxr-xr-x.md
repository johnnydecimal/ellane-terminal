---
title: drwxr-xr-x
description: What is the output of `ls -la` trying to tell me?
author: Ellane
date: 2024-06-06T08:38:54
tags:
  - command
  - concept
mastodon: https://pkm.social/@ellane/112568300924652209
---

Interesting podcast excerpt, thanks. It's good to know about Macs having a different approach to case than other systems. Seems to me if we're going to err, it should be on the side of precision—so I'll play it safe by treating everything as case sensitive from now on.

Thanks for explaining the `ttys000`. I figured it wasn't something I _needed_ to know, but having that confirmed saves me from the distraction of wondering what it is every time I see it.

Just to check, I opened another window and yep, it said `ttys001`.

I played with `ls -la` for different locations on my hard drive, and the `--color=always` one, too. The latter produced mostly one colour, with splashes of another here and there. I suppose we'll get to the logic behind that later, if it's important enough to discuss.

When displaying `ls -la` there's a column on the left with information like `drwxr-xr-x@` that I don't understand.

As with the colour, we'll either get to that later or it'll turn out to be something else I don't need to worry about.

Referring to the `ls` information at [ss64.com/mac/ls.html](https://ss64.com/mac/ls.html), I tried `ls-F` as a shorter way of writing `ls -F`, but it returned an error: `zsh: command not found: ls-F`.

Okay. Commands, flags and options, arguments, in that order. Got it.

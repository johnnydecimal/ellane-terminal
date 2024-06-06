---
title: Case-sensitivity, ttys, and the prompt
description: Two follow-up questions.
author: Johnny
date: 2024-06-05T23:41:53
tags:
  - concept
  - follow-up
mastodon: https://hachyderm.io/@johnnydecimal/112566833518091202
---

## Case-sensitivity

> **Ellane**  
> Question: is case important?

I didn't know you could do that thing with `cd desktop`. I find that a little weird and surprising.

Traditionally, [\*nix](https://en.wikipedia.org/wiki/Unix-like) systems _are_ case-sensitive.

Your Mac is not. It could be, but it isn't. There was a really good discussion on ATP recently: check [episode 583](https://atp.fm/583) at `1:12:10`.

Pretend like it is and you won't go far wrong.

## `ttys`

> **Ellane**  
> One more question: what's `ttys000`?

[When Terminals were the whole computer](/learn/04-let-me-show-you-around-your-new-car/#history-lesson), they each had an ID. Just like your computer has a name.

When you launch a new Terminal window, it gets an identifier in the same way. Because you can launch _another_ Terminal window, and be running commands in each.

Your system needs to know which command belongs to which window. So that's what `ttys000` is.

Fun fact: `ttys` is short for `t`ele`ty`per `s`ecure. There's a [great history lesson here](https://thehistoryofcomputing.net/the-teletype-and-tty) -- this stuff goes back _centuries_.

We'll talk about this more [later](/about/#later).

## The prompt

> **Ellane**  
> And why the `%` sign? I seem to remember a `$` sign being there last time.

This is just a style thing.

Until recently, the language that you were using in your Terminal was [**bash**](<https://en.wikipedia.org/wiki/Bash_(Unix_shell)>). The default 'prompt' for bash is `$`.

A couple of macOS versions ago they switched to [**zsh**](https://en.wikipedia.org/wiki/Z_shell), which is more modern. Its default prompt is `%`.

The **sh** part of both of those is short for 'shell'. The original shell was just called **sh**! [Wikipedia](https://en.wikipedia.org/wiki/Unix_shell) has a nice overview.

We won't use any zsh-specific stuff in this tutorial. And unless they say otherwise, all of the commands you'll find online that tell you how to install a thing will work in both shells.

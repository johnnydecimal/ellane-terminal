---
title: The structure of a command
description: Our first look at the fundamental structure of a command.
author: Johnny
date: 2024-05-31T06:03:06
tags:
  - command
  - concept
mastodon: http************
---

## Feedback on homework

Regarding [closing the window vs. typing `logout`](/learn/05-close-on-exit/#homework-assignment-part-2), not only does it feel like getting out before putting the car in 'park', it feels like opening the door and jumping out while the car is moving!

Now, this isn't what actually happens. When you close the Terminal window, it **sends a signal** to the CLI, and if something important is happening you'll be warned about it. It's like how modern cars lock the doors when you start moving: it makes it difficult (but not impossible) to jump out as you're hurtling down the motorway.

I think [Gordon hit the spirit of it](https://monrepos.casa/display/0e03068e-2166-586a-170a-1cd580731423). When you're in the CLI, _that's where your control is_; that's where you should be issuing commands.

This is a Windows (as in Microsoft) vs. Unix mindset. Windows people think in the GUI. Unix people think in the CLI. When you're doing this stuff, put your CLI hat on.

We'll come back to this passing-around-of-signals in the future.

## Tech support question

For those of you following along at home, Ellane's Terminal window is responsive again. I [tooted her a video](https://hachyderm.io/@johnnydecimal/112532621902965084) of 'normal behaviour', which is exactly what you'd expect: after each command, you can type the next command.

We're not sure what was going on there, so we'll keep an eye on it.

---

# The structure of a command

Let's get to the good stuff.

Commands are all structured in the same way. They all follow one of a few patterns. When you learn those patterns, you learn the syntax of _all commands_.

We know that `pie lunch cook` isn't a valid sentence, even if we're not a chef.

And soon you'll immediately recognise that `--food pie &meal lunch cook` couldn't ever be a valid command: it just doesn't _look_ right.

`cook --meal lunch pie`, however: while that _isn't_ a valid command, it _could be_.

## The first thing is always the command

The command is the thing that decides what happens. Are you moving, copying, deleting, listing, installing, or printing a thing? It doesn't matter: **but it comes first**.

And sometimes that's all there is. We've already seen this: `printenv`. That was it. That was the command.

Let's introduce a few that we'll actually use.

---

# Command traffic lights 🚦

When I introduce a new command, I'll always give it a traffic light:

- 🟢 Totally safe. There is nothing you could possibly do that could cause harm.
- 🟡 Usually safe. You _can_ cause harm, but it's really unlikely.
- 🔴 Possibility of harm. I'll tell you how not to, and you probably won't, but you _could_.

## Reference page

I'll also create a short entry for each command on the new [reference](/reference/) page.

These will be brief, as every command has its own documentation. We'll see that later.

---

# New command: `cd` 🟢

Many -- most? -- commands are abbreviations of the thing that they do.

The shorter the command, the older it likely is. `cd` stands for `c`hange `d`irectory and it's older than me.

You can use it with no **arguments**. I'll introduce and define these soon. But for now, just type it.

```bash
cd
```

You should be underwhelmed! Nothing happened? But actually something did.

For one, you didn't get an error. Try garbage -- `lksjdfl` -- and see what happens.

Always pay attention to the _output_ of a command. Never just assume that it worked. If it didn't work, it'll _always_ tell you.

---

# New command: `ls` 🟢

Try this one.

```bash
ls
```

This is short for `l`i`s`t directory contents. And look at the results: seem familiar?

Pause here until you know exactly what you're looking at.

## Guess this next bit

So we're looking at the contents of your home folder. That's where a Terminal window opens to, by default.

Let's `c`hange `d`irectory. Try to guess how to move in to your **Documents** folder. Type it in.

.

.

.

.

```bash
cd Documents
```

Again, it doesn't look like much happened. But notice two things: first, your **prompt** has changed. It now has the word `Documents` before the `%`.

Second, if you try `ls` again, you'll see the contents of your Documents folder.

**Change directory. List the contents. Change directory. List the contents.**

This is something you do _all the time_.

## Arguments

You just saw your first **argument**: `Documents` was an argument to the `cd` command.

We'll go in to this in detail later, I just wanted to briefly note it here.

---

# New command: `pwd` 🟢

This one stands for `p`rint `w`orking `d`irectory. Try it and see what you get.

You `cd`'d to your Documents folder, so it should say something like

```txt
/Users/ellane/Documents
```

So you know where you are because your prompt gives you a clue, and if you want to be totally certain, you `pwd`.

This syntax, with the forward slashes, is very specific. I'll explain it soon.

## How to get home

`c`hanging `d`irectory to your home folder is such a common task, there's a shortcut for it.

We've already seen it. Care to guess?

.

.

.

.

```bash
cd
```

`cd` with **no arguments** takes you home.

---

# Take yourself on a trip 🚗

Use these commands a bunch until you're really comfortable with them. See where you can go. And see where you _can't_ go.

You might have some questions about how you move around. Let me know. If not, we'll keep going.

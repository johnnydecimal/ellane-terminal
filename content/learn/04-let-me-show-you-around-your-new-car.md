---
title: Let me show you around your new car
description: Computers are like cars. Let's head to the showroom and pick you a nice model.
author: Johnny
date: 2024-05-30T02:55:39
tags:
  - concept
---

Oh good analogy! That's going to be helpful.

Learning 'the command line' is like learning how to drive. But before we can drive, we need a vehicle.

Let me show you around your new car.

> Before we start, to save me some typing let's introduce a shortcut for 'the command line': **CLI**.
>
> It stands for **command-line interface**. I'll use it from now on.

---

# Terminal

You can't drive without a car. The car is the framework that gives you the ability to drive: it has a chassis, four wheels, seats, air conditioning, and they come in a variety of models which you pick according to your needs.

In the same way, you need some sort of application to use the CLI. We call these 'terminals', and your Mac comes with one. Conveniently, it's called **Terminal.**

## History lesson

[Terminals](https://en.wikipedia.org/wiki/Computer_terminal) used to be the whole computer. The _only thing it did_ was to be a terminal.

These days computers are a lot more powerful, and 'the terminal' is just an app. Technically we call it a [terminal emulator](https://en.wikipedia.org/wiki/Terminal_emulator).

## There are other terminal apps

Apple's Terminal is like a Ford Escort. It's pretty basic, it doesn't have many extras, but it comes with the job and doesn't cost you anything to drive.

If you want more features -- a better stereo, nicer wheels -- you can go shopping and get yourself a nicer model. There's [iTerm 2](https://iterm2.com), [Warp](https://www.warp.dev), and a bunch of others.

You can even get them [for your iPad](https://panic.com/prompt/).

But when you're just learning, stick with the simple car. I still use Terminal; it does everything that I need.

---

# Launching Terminal

Let's get your seat and mirrors adjusted. Launch Terminal, which is in your Mac's  
`/Applications/Utilities` folder.

> By the way, that notation with the slashes -- it means something _very_ specific, which you'll soon understand. :-)

You'll be greeted by a fairly austere window.

<img
  src="/img/04.01-terminal-basic-682x483.png"
  alt="A screenshot of the basic Terminal window with it's default configuration. Small black text on a white window."
  width="682"
  height="483"
/>

I like to feel more like an old-school nerd when I'm at the CLI, so I set my default terminal to have green text on a black background. You can do that in Terminal's **Settings**: on the **Profiles** tab, select **Homebrew**,[^unrelated] and click **Default** at the bottom of the list.

[^unrelated]: Unrelated to the CLI tool that we'll learn about later.

I also bump up my font size, which you can do on the right under **Font**.

Now hit `Command-N` to get a new window.

<img
  src="/img/04.02-terminal-homebrew-1002x650.png"
  alt="Terminal, now green-on-black and with a larger font."
  width="1002"
  height="650"
/>

<p style="font-size: 4rem; margin: 0; text-align: center;">😎</p>

## Tip: duplicate the default profiles

You can modify these profiles to your heart's content. If you select one of the defaults and click the three-dots-in-a-circle icon at the bottom of the list, you can **Duplicate Profile**. Now if you mess it up you can just delete it and start again.

## We haven't started the car yet

It's important to note that what you're messing about with here is _the Terminal application's settings_. There's no harm you can do here, other than making it look ugly.

We haven't put the key in the ignition yet. Let's do that and make sure it starts.

## Start the engine

It can help to see some text in the otherwise-empty window. So let's type your first command, which I'm not going to explain. It's just a command that will fill up your window with text.

Crucially, it's totally harmless.

Type `printenv` and hit **return**.

<img
  src="/img/04.03-terminal-printenv-1017x650.png"
  alt="Terminal, showing the result of the `printenv` command. Which is mostly a bunch of incomprehensible junk."
  width="1017"
  height="650"
/>

# Shut it down

To close this window, you have a few options.

1. Type `logout`.
2. Type `exit`.
3. Press `Control-D`.
4. Close the window using the red button at the top right.

They all do the same thing. I prefer `logout` because it feels more nerdy. `Control-D` is also very old-school.

Closing the window feels like the _least_ correct thing to do.

---

# Homework

## 1: Have the window close automatically

When you use one of the first three methods, the window won't actually close. Instead you'll be left looking at this text:

```bash
Saving session...completed.

[Process completed]
```

Figure out how to make it so that when you type `logout`, the window closes. Have a look around Settings, but use the internet if you're not sure.

## 2: Why don't I like using the red button?

I said that closing the window using the red button felt like the 'least correct' thing to do.

Why?

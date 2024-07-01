---
title: Homebrew
description: Let's install Homebrew.
author: Johnny
date: 2024-07-01T07:42:16
tags:
  - command
mastodon: https://hachyderm.io/@johnnydecimal/112676220917130785
---

Okay, let's turn in the direction of `hledger`. We're going to install it.

First, we need to install Homebrew. But first: what is it?

## Package managers

We're all used to installing software, and keeping that software up to date.

You might use the App Store, which is one-click with invisible updates in the background.

You might download a `.pkg` file, which you double-click and **next, next, next** your way through. The application it installs then prompts you, over time, to perform updates.

But how do you install and keep updated applications for your Terminal? There are a bunch of ways, but **Homebrew** has become the de-facto standard for the Mac. Because it's just really nice.

## Other `hledger` options

It's worth nothing that there _are_ [other installation options](https://hledger.org/install.html) for `hledger`.

But given how nice Homebrew is, we're going to use it.

---

# Install Homebrew

Okay, right there on the [home page](https://brew.sh). Simply copy paste this command in to Terminal.

# 🚨 🛑 ‼️ 🚨 🛑 ‼️

Okay, a massive word of caution. Whenever someone, including me, tells you to 'simply copy/paste a command in to Terminal': **don't do that.**

By now you have an idea of what this thing can do. It's a window in to the deepest parts of your system. And so entering random commands from the internet is a massive, massive risk.

So what do we do? Well, we just have to be aware of that, and to trust Homebrew. Because, realistically, we can't validate this command ourselves. It's too hard. So unless Homebrew has been hacked, or the people running it suddenly sold out, we'll be okay.

Just be aware of the risk.

## The installation command

We don't _need_ to understand it, but let's deconstruct it a little just so you're aware.

```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

## `/bin/bash -c`

This is an absolute path to a command: actually, to the `bash` shell itself. Then the flag `-c` says to 'read the next command from a string'.

So this just says, 'do the rest of this command in a shell'. And we're already in a shell.

I'm not sure why this is required, to be honest. I think it's just the Homebrew people being really, really safe: you should be able to run this command from darned-near anywhere and it'll work.

## `"$( ... )"`

The command to be passed to `bash -c` is enclosed in quotes and dollars and brackets for reasons. ;-)

## `curl` 🟢

This is what's doing all of the work.

`curl` gets web pages. Try it out: `curl https://jdcm.al` will dump the HTML of my home page in your Terminal.

> I'm not sure what the `c` is for, but `url` as in, a URL.

The flags `-fsSL` presumably do important things in this context, which `man curl` would explain to us, but I'm not going to go there.

So what is `curl` getting? This:

`https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh`

And that's just a URL! So we can [view it in a browser](https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh).

It's ... long ... and ... really complicated. But what we're looking at here is the installation script for Homebrew. I barely understand it.

Now if we zoom back out and look at the whole installation command, we've got:

- `bash -c` running something that
- `curl -fsSL` downloads, which is
- this script.

It should be obvious why this is risky from a security perspective.

## Caution to the wind

It's time, though. Copy the command from the Homebrew home page, paste it in your Terminal, and off you go.

When the installation finishes, it'll tell you to do something like:

```bash
- Run these two commands in your terminal to add Homebrew to your PATH:
    (echo; echo 'eval "$(/opt/homebrew/bin/brew shellenv)"') >> /Users/john/.zprofile
    eval "$(/opt/homebrew/bin/brew shellenv)"
- Run brew help to get started
- Further documentation:
    https://docs.brew.sh
```

Yours will be subtly different to mine, so copy them from your screen, not this page. But just so it's clear, the two commands are:

1. `(echo; echo 'eval "$(/opt/homebrew/bin/brew shellenv)"') >> /Users/john/.zprofile`
2. `eval "$(/opt/homebrew/bin/brew shellenv)"`

...and then `brew help` to check it's worked. If it hasn't, closing and re-opening your Terminal window might help.

That's enough for today, and I need to go and cook dinner!

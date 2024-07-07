---
title: Install some (Homebrew) packages
description: We use Homebrew to install and remove some stuff.
author: Johnny
date: 2024-07-06T07:58:28
tags:
  - command
mastodon:
---

> **Ellane**
>
> Done. I was held up briefly because there was no visual feedback when typing my password; got it on the second try.
>
> It seems to have worked, as `brew help` is showing me a list of ways to get started. I'll be (wisely) leaving those alone until you help me learn what they're all about.

So the purpose of Homebrew is just to install hledger. How might we do that?

Homebrew's web site is _amazing_ so we might as well double-check. Head [over there](https://brew.sh) and search for `hledger` using the box at the top. You should find yourself [on the formulae page for the app](https://formulae.brew.sh/formula/hledger#default).

We don't really need to know how Homebrew works. Just like we don't really know what's happening when we launch an installer and **next, next, next**. But, just briefly, it has what it calls 'formulae', which are just installation scripts. And sometimes you have to add a 'cask' (they really push this metaphor) so that you can access these formulae.

But in this case, the page tells us exactly what we need to do:

```bash
brew install hledger
```

Which is a familiar pattern by now: some command, `brew`, followed by some options. Let's keep reinforcing this with a quick trip to `man brew`, which tells us that the syntax for `brew` is:

```bash
brew command [--verbose|-v] [options] [formula]
```

Let's drop our command in below that.

```bash
brew command [--verbose|-v] [options] [formula] # man brew
brew install                           hledger  # our command
```

So that's:

- `brew`, the main command.
- `install`, which is brew's 'command': you're saying, _brew, please install a thing_.
  - Similarly you can `brew remove ...`.
- Optionally the flags `--verbose` _or_ `-v` -- a very common flag that tells the command to be verbose in its output.
  - You tend to use this when you're trying to troubleshoot something.
  - We didn't specify them in our command. You can if you like.
- `[options]`, some optional options.
  - Which we're not using.
- `[formula]`, which we're specifying as `hledger`.

All of this is just to get these patterns deeper in your brain. The more familiar they are the more comfortable you'll be.

---

# `hledger`

Assuming there were no errors -- and you should always read the last few lines of the installation output just to be sure -- you've now got `hledger` installed. Run it!

```bash
hledger
```

So when I ran it I thought two things:

1. Oh that looks cool!
2. It's flashing a cursor ... does it want me to run a command?

<img
  src="/img/18.01-hledger-help-2004x1394@2x.png"
  alt="hledger's welcome/help screen"
  width="1002"
  height="697"
/>

## Homework

Now that this is installed, see what you can do with it. I've played myself and it _is_ pretty arcane! So don't worry if you don't get too far.

(You can't mess this up. If the worst happens, we just remove it and add it again.)

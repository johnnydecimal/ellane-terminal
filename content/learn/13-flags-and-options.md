---
title: Flags and options
description: The final piece of the command puzzle, we introduce 'flags' and 'options'.
author: Johnny
date: 2024-06-06T00:35:58
tags:
  - command
  - concept
mastodon: https://
---

We almost understand the syntax of a command. To recap, we've met the **command**, and its (often optional) **arguments**.

Now let's meet **flags** and **options**, which are two sides of the same coin.

## Behaviour modifiers

Flags modify the behaviour of a command. Let's try one out.

```bash
ls -l
```

That's a dash/hyphen, then a lowercase letter 'ell'.

Try the un-flagged `ls` and then `ls -l` and compare the output. The flagged variant gives you a _longer_ output; more detailed.

The `l` stands for `l`ong. We've said to `ls` _please exercise your ability to give us a longer output_.

Let's try another.

```bash
ls -a
```

There's _more_ stuff here: depending on your system you might see `.DS_store`, `.localized`, and look carefully: our [friends](/learn/08-file-paths/#and-also-have-special-meaning) `.` and `..` are now shown.

By default, some system-level stuff is hidden from a basic `ls`. But `a` is short for `a`ll: you're asking `ls` to _show you all the things_.

## Combining flags

You can ask `ls` for both things.

```bash
ls -l -a
```

Note the order doesn't matter. But that's clunky. Dash-l, dash-a. It'd be nicer if we could combine them...

```bash
ls -la
```

This pattern -- `ls -la` -- is so common that many people make it their default. We'll see how to do that later. I just type it instinctively, it's seared in to my muscle-memory.

## You can still specify an argument(s)

Let's combine everything we know.

```bash
ls -la ~/Downloads
```

If that doesn't make you want to clean up that folder, nothing will.

(We'll go in to more detail about what `ls -l` is showing you later.)

---

# Conventions

There are well-held conventions that are used here. They aren't hard rules -- developers can and do break them -- but if you use them as a guide you won't go far wrong.

The **command** always comes first. That is a hard rule.

Then **flags** come next. A convention, very widely held. I can't think of an example where it isn't the case.

Then lastly, the **arguments**.

```bash
  ls -la ~/Desktop
`# │   │  └─ argument(s)`
`# │   └──── flag(s)`
`# └──────── command`
```

## Flags-as-words

`-l` isn't very expressive, and there are only 26 letters of the alphabet. So full-word flags are also totally normal.

And here's a well-held convention that I _do_ see broken: full-word flags should start with **two dashes**.[^dscacheutil]

[^dscacheutil]: Looking at you, [Apple](https://ss64.com/mac/dscacheutil.html).

```bash
ls --color=always
```

## ...and this is now an option

I just realised that we've moved from a **flag** to an **option**. Do you know why?

Flags are either there or not. On or off. I imagine the analogy is to a raised flag: up, or down.

Options have more data. What's with `=always`? Well, the other options are `=auto` or `=none`.

You can think of this as an argument _to the option_. We'll see a lot more of this as we go on so don't worry too much about this for now.

## All together now

As you might imagine, you can mash all of this together.

```bash
ls -la --color=always ~/Downloads
```

---

# Everything is just a variety of this

First the **command**.

Then all of the **flags and options**.

And finally any **arguments**.

That's the basic structure of every command.

## Homework

The **man page** for `ls` is [online here](https://ss64.com/mac/ls.html).

Try a bunch more options and see what you can get `ls` to produce. Soon, I'll show you how to bring these **man(ual) pages** up directly in Terminal.

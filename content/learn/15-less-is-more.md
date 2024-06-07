---
title: Less is more
description: Viewing text files, including 'man pages'.
author: Johnny
date: 2024-06-06T08:41:38
tags:
  - command
  - concept
mastodon: https://hachyderm.io/@johnnydecimal/112573007010733810
---

Great questions, and we'll get to `drwxr-xr-x` really soon.

For now, addressing the `ls-F` error, let's introduce you to the built-in help pages: known as **man pages**.

The reason the instruction from the [page at ss64](https://ss64.com/mac/ls.html) didn't work is because that page is out of date.

So how do you view up-to-date information? Well let's start with how you view _any_ information.

## Do you have a plain text file handy?

Typing this at my kitchen table I thought, I'll have to tell her to create a plain text file that she can use to test this next bit. Most people don't just have a bunch of plain text files knocking about.

<img
  src="/img/15.01-facepalm-777x437.jpg"
  alt="The Picard facepalm. (If I do say so myself, I bear a resemblance to Jean-Luc.)"
  width="777"
  height="437"
/>

Then I remembered who I was talking to.

## Let's view a file

Emphasis on _view_: we have no desire to _edit_ it.

This gets to one of the general principles in the CLI: the _principle of least privilege_.[^serendipity] If you don't need to edit a file, don't open it in a file editor: open it in a file viewer.

[^serendipity]: A better writer would have had this in mind when they titled this post.

The oldest command, and the one you'll see referenced most often, is `more`. Unfortunately that's another one that's in my muscle-memory. Because there's a better command, and as you're new you might as well start using it.

In classic Unix style, it's called `less`.[^most]

[^most]: Apparently there's an even better version called `most`, but a) we don't need it, and b) it's not installed by default.

We'll use `less`, but if you see `more` in online instructions you can either use it, or substitute `less`.

---

# `less` 🟢

`cd` yourself to a folder that has some text files.[^help] And then, as you might expect:

[^help]: If you're following along at home and you don't have a plain text file handy, you can launch `less --help` and use the help file to practice navigation.

```bash
less yourfile
```

## It'll show the file

Big whoop! What's more interesting is how we move _around_ the file, because you should assume that your mouse won't work. (It will probably scroll up and down for you. But don't do that.)

Again, there are well-worn conventions that will serve you in many CLI situations.

- The `space` key will move you down one full page. This is a really nice way to read a long article.
- `Arrow-up` and `arrow-down` will move you up and down a line.
  - But the more CLI way to do it is to use `j` and `k`.
  - These keys are on the home row. Your fingers are already there.
  - And they're the same keys that `vim` uses, so learning them now will be really handy later.
- `q` quits.

There are tons more, and there's no point me listing them all: press `h` to bring up the help screen.

## `^` means the `control` key

Another convention, and this one's universal. `^E` means `control-E`.

## Search is interesting

If you hit `/`, you're in search mode. Type a word, hit return.

To find the next instance of the same search, hit `n`. The previous, `N`.

Again, this is how `vim` works.

When you get used to these shortcuts -- `j`, `k`, `/` to search -- you start to move around a lot more quickly.

(Just curious: do you touch-type?)

## Homework: read all of the `less` help

The help page has a lot of nerdy terminology that ties together everything we've learned so far. It might look scary to start, but just read it all slowly, try out the various options, and get used to how it all looks.

Being able to see a screen like this and absorb it all is the superpower we're aiming for. None of it's difficult; it's just unfamiliar.

Make sure you're really comfortable with that before we move on

---

# `man` pages

So this brings us to the `man` page, one of the wonders of the modern world.

Every (well-behaved) command has its own manual page. It tells you everything you need to know about that command: its flags, options, and the arguments that it takes.

So `man` is the command, and it takes flags, options, and arg... well, let's just have a look.

```bash
man man
```

You're looking at the man page for `man`. :-)

## Convention: indicating flags and arguments

Let's dissect this first line.

```txt
man [-adho] [-t | -w] [-M manpath] [-P pager] [-S mansect]
         [-m arch[:machine]] [-p [eprtv]] [mansect] page ...
```

This is telling us that:

- The command is `man`.
- It optionally accepts `a` `d` `h` and `o`, or any combination thereof, as flags.
- It optionally takes _either_ `t` or `w` as flags. But not both.
  - The pipe symbol `|` means 'or'. One _or_ the other.
  - Or, because they're both in `[square brackets]`, neither!
- It optionally takes `M` as an option with a required `manpath` argument.
- It optionally takes `P` as an option with a required `pager` argument.
- It optionally takes `S` as an option with a required `mansect` argument.
- It optionally takes `m` as an option with a required `arch` argument, and optionally you can specify `arch:machine`. Options-in-options!
- It optionally takes `p` as an option with any combination of `eprtv` as additional arguments.
- It optionally takes a `mansect` argument.
- It requires a `page` argument.
- You can supply multiple arguments, denoted by `...`.

There's a _lot_ there, and I've never used any of those options to `man`. The point of this was just to decipher that stuff at the top.

So when we did `man man`, we typed the command, `man`, and supplied the only required argument, `page`, which just so happened to also be `man`!

## Keep reading

I wonder what `-a` does. I can either scroll down with `space`, or the smarter way is to search for it with `/` then `-a` and `return`.

The first search result shows us this line that we're reading. Hit `n` for the next result, and there we go.

```txt
-a   Display all manual pages instead of just
     the first found for each page argument.
```

Now, we still don't really care what this actually does. The lesson here is manoeuvring around the viewer, not understanding all of `man`'s options.

## `man` is `less`

Because `man` uses `less`. You can prove this by hitting `h` to bring up the help.

## `BUILTIN(1)`

There's a small idiosyncrasy if you `man cd`. You'll see the man page for `BUILTIN(1)`.

This is because `cd` isn't considered its own program: it's so core to everything, it's built-in to the shell. To see these man pages, type `man zshbuiltins`.[^zsh]

[^zsh]: This one is obviously specific to the more modern **zsh** vs. **bash**.

---

# Now you can view anything

Check the man pages for stuff we've already seen. Now you can see that `man ls` doesn't have that weird `ls-F` thing going on.

Get comfortable with this and we'll move on. Start browsing and searching some of your own plain text files using `less`.

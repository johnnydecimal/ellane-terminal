---
title: Escape arguments, completely
description: The CLI doesn't handle spaces in file names very well. We use 'escaping' to work around it.
author: Johnny
date: 2024-06-03T20:59:57
tags:
  - concept
  - filesystem
mastodon: https://pkm.social/@ellane/112549360746816133
---

Let's use these annoying spaces to go a little deeper on the concept of **arguments**.

We've already met them. We have a **command** which is _optionally_ followed by an **argument**.

```bash
cd ~/Desktop
`# └─┬─────┘`
`#   the argument`
```

- Command: `cd`
- Argument: `~/Desktop`

Arguments are sometimes called **parameters**. If the command is the thing that _does a thing_, the argument is the _thing it does it to_.

`cd` _to where_?

`ls` _which folder_?

So far we've seen zero- and one-argument commands. But many commands can take multiple arguments; many commands _need_ multiple arguments.

Think about copying a file: you have to know _which file to copy_ and then _where to copy it to_.

Two arguments. And we separate them by ... you guessed it ... a space.

`ls` will accept more than one argument. Just give it more than one folder to list.

```bash
ls ~/Desktop ~/Downloads
`# └─┬─────┘ └─┬───────┘`
`#   first     second`
```

- Command: `ls`
- First argument: `~/Desktop`
- Second argument: `~/Downloads`

So now it should be obvious why trying to list out a folder with a space in its name doesn't work. The CLI doesn't know that it's one folder: actually, you gave it two arguments, and neither is the name of a folder!

---

# How to 'escape' this problem

This is obviously a very common issue. The solution is a technique called **escaping**.

When we escape a character, we're telling the CLI: _treat the next character as exactly what it is_.

So if it's a space, just _be a space_. Don't be _the boundary between two arguments_.

The escape character in your CLI's language is `\`. Put a backslash before any character to 'escape it'.

```bash
`#   one argument`
`# ┌─┴───────────────────┐`
cd My\ great\ folder\ name
`#   ^      ^       ^`
`#  escape characters`
```

## Not just spaces

Create a folder on your Desktop called `"A_folder_in_quotes"` and see if you can `cd` to it.

You'll need to escape those double-quote characters.

```bash
cd ~/Desktop/\"A_folder_in_quotes\"
`#           ^                   ^`
`#           the escape characters`
```

It's ugly. You never get used to it; you just have to learn to live with it.

## Remember, _any_ character

It's worth reinforcing that this works before _any_ character. Not just special characters.

So in our continuing series of it-works-but-you'd-never-actually-do-it, this is perfectly valid.

```bash
cd ~/\D\e\s\k\t\o\p
```

You're saying 'be a D!', 'be an e!', 'be an s!' ... but that's what they were anyway. So nothing changes.

---

# Tab completion saves the day

You'll drive yourself mad -- and get it wrong very, very often -- if you try to manually escape your file paths. Fortunately, there's an easier way.

The CLI will **auto-complete** a file path for you if you press the `tab` key. I'll denote that as `<tab>` in these code blocks.

```bash
cd ~/A<tab>
```

There's only one folder in my home folder that starts `A`, and it's `Applications`. Hitting `tab` autocompletes it for me.

Note that it _doesn't_ press `return` for you. It doesn't run the command: you might have more to type before you're ready for that.

## Multiple results

On this Mac, I've got five folders in my home folder that start with `D`: `Databases`, `Desktop`, `Documents`, `Downloads`, and `dev`.

So try that:

```bash
cd ~/D<tab>
```

Your CLI will show you the possibilities. Now you can do two things.

1. Type some more characters to disambiguate your intent, and hit `tab` again.
2. Mash the `tab` key and watch it cycle through all the options for you. Stop when it reaches the one you want.

Pretty cool![^johnnydecimal]

[^johnnydecimal]: For extra nerd points think about how easy this might make navigating a Johnny.Decimal hierarchy...

## What's this got to do with spaces?

Try tab completion on a folder with a space in it and find out. :-)

---

# Homework

## 1. `"A folder in quotes"`

Make sure you can `cd` in to `"A folder in quotes"`. Note the spaces in this version.

You might have to escape something yourself to get started, but as soon as you can you should use tab completion to finish the job.

## 2. `this\that`

Using Finder, create a folder on your Desktop called `this\that`.

Now, _without using tab completion_, try to `cd` to it.

## 3. Too much escaping

Earlier, we saw that this worked.

```bash
cd ~/\D\e\s\k\t\o\p
```

But this does _not_ work. Why?

```bash
cd \~/\D\e\s\k\t\o\p
`# ^ extra escape character here`
```

---
title: File paths
description: How do we get around the file system if the folder we want isn't a direct subfolder of where we are?
author: Johnny
date: 2024-06-01T06:34:46
tags:
  - command
  - filesystem
mastodon: https://********
---

You stumbled in to a [meme](https://thenewstack.io/how-do-you-exit-vim-a-newbie-question-turned-tech-meme/)! What are the odds.

We'll come back to `vim`, which it turns out you can also launch by typing `view` (I had no idea!), much later.

But for now, yes, that's a valuable lesson. There are many situations where guessing a thing is a good idea. The CLI is not one of them.

(I might ask you to guess things, like `cd Documents`, where I'm pretty sure you're not going to accidentally wipe your hard drive.)

---

# `cd`'ing to a nested folder

File paths are core to this whole experience: many things you do involve a file, or being in a specific folder before you take an action. So let's go a bit deeper.

We'll need a subfolder, which it sounds like you have. But to keep this example simple I'm going to get you to create one on your Desktop; then people following along at home can use the same commands.

So, using the Mac Finder, create a folder called `TestFolder` on your Desktop. Note the lack of a space between the words.

## The `/` forward slash

This is the long way around:

```bash
cd `# takes you home if you're not already there`
cd Desktop
cd TestFolder
```

> That `# takes you home...` bit in grey is a comment. Don't type that bit, including the first backtick. I'll use these to add comments to specific lines, or to show you what output to expect.

Or you can do it in a single step by using the `/` forward-slash, which separates subfolders.

```bash
cd
cd Desktop/TestFolder
```

Your prompt should update, and `pwd` will show you where you are.

## Specify 'my home folder'

We know that `Desktop` is in our home folder. But we might not be there already, so we have that annoying first `cd` to take us there.

We can skip this by using the shortcut for _my home folder_ which is `~`.

```bash
cd ~/Desktop/TestFolder
```

This is a common shortcut that you'll see in online instructions. It's handy because the person writing doesn't need to know where your home folder is: `~` is universal. Keep an eye out for it.

## `.` and `..` also have special meaning

A single `.` in a file path means _the folder that I'm currently in_.

So this works. It's not useful here, but later we'll see where we do use this.

```bash
cd ~/Desktop
cd ./TestFolder
pwd `# /Users/ellane/Desktop/TestFolder`
```

Two periods `..` means _the parent folder_. You use this one all the time.

```bash
cd ~/Desktop/TestFolder
cd ..
pwd `# /Users/ellane/Desktop`
```

## This works everywhere

You can use all of these wherever you'd type a file path; it's not just a `cd` thing.

So you can `ls ~/Downloads/some/other/folder`.

## You can combine all of this

This crazy thing works. You'd never do it, but it works.

```bash
ls ~/../john/Desktop/TestFolder/../../././Downloads
`# lists the chaos of my Downloads folder`
```

Note that my username is `john`. Substitute for yours: if you're not sure what it is, `whoami` 🟢 will show it. In these lessons I assume it's `ellane`.

Make sure you understand _why_ this works. Make some of your own crazy file paths just for practice.

---

# Relative vs. absolute paths

File paths can be **relative** or they can be **absolute**.

If they're relative, they're relative to _where you are_. This is what we've seen so far.

```bash
cd
cd Desktop `# relative to your current location`
```

These are usually shorter and more convenient. But they can go wrong: someone might assume you're in folder A, and tell you to issue some instruction that includes a relative file path.

But if you're actually in folder B, the results are unpredictable.

So we can specify **absolute** file paths that work _regardless of where you are_. We've already seen one.

```bash
cd ~/Desktop
pwd `# /Users/ellane/Desktop`
```

`pwd` always reports an absolute file path.

## `/Users/ellane/Desktop`

Let's look at this in detail.

The first thing to note is that it _starts_ with a forward-slash. This is another special character: at the beginning of a file path, it means _the top of my file system_.

Try this.

```bash
ls /
```

Seem familiar? Before you move on, see if you can find this same location in a Finder window.

You're looking at a listing of what we call the **root** of your file system.

In Finder, it's what you see if you open the **Macintosh HD** view.[^macintoshhd] Or from your home folder, you can `Command-up arrow` twice.

[^macintoshhd]: Assuming you haven't renamed your drive.

In Finder, `Command-up arrow` takes you up to the parent folder. So if you compare this view to `/Users/ellane` -- the absolute path to your home folder -- it should make sense.

1. The first `Command-up arrow` is like typing `cd ..`, and takes you to `/Users`.
2. The second does the same again, and takes you to `/`. The root of your file system.

Absolute paths basically always start with a `/`. I'm sure there's an exception, but if you have that in mind, you won't go far wrong.

That slash says, _regardless of where you are, go back to the top_. It's very powerful.

## Keep playing

Of course all of this is interlinked.

```bash
cd /Users/./ellane/../ellane/Desktop/TestFolder/..
```

Again, absurd, but you get the idea.

## The `shared` user

Note that there's another user on your Mac whose home folder is at `/Users/Shared` if you want to play around with more paths.

## This is an exact science

Pay attention to how you see file paths written online. You will never, ever see someone specify `Users/Shared`. Because that's a relative path.

If your current directory just happens to be `/` then that's valid. But it probably isn't. So it'll always be specified as `/Users/Shared`.

---

# Get super comfortable with this

Simple enough concepts but you need to know these backwards. Just have a good play around and let me know if you find anything interesting.

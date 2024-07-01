---
title: A rapid advance
description: I recommend Ellane use the amateur 'pico'. She goes straight to 'vim'. Nice.
author: Ellane & Johnny
date: 2024-07-01T07:33:31
tags:
  - command
mastodon: https://hachyderm.io/@johnnydecimal/112676220917130785
---

> Just copy/pasting this one from Mastodon. I'm a bit behind, sorry everyone!
> –j.

Okay, terribly late on this one, and I still haven’t written a proper post for our little site. But I figure if I just type this at the kitchen table rather than agonising over perfection, that’s probably better.

(I will update the site later.)

So we’re going to ‘pivot’, as we say in the tech industry. I set out to teach you ‘the CLI’, but that’s a _massive_ undertaking, and your actual goal is to ‘learn plain text accounting, specifically hledger’.

Rather than possibly useless theory, therefore, we’re going to focus on the goal, and cover topics _as required_ on our way to that goal.

In your latest blog post you mentioned that you can read stuff, but you can’t yet edit. So let’s do that now.

Now, this qualifies as a ‘potentially dangerous’ command. Because if you edit the wrong file, you could mess something up! So just make sure you’re in the right place, and maybe create some test files to start.

The command 🥁 is 🥁

`pico`

That’s it. You can just type `pico` and it’ll open.

And I’m going to leave you there. Because if you look around, I think you’ll work it out. The hints are all on-screen: see the bar along the bottom.

This is a pretty rudimentary text editor. It’s not the legendary `vim`. But it’s easy to use, and it’ll do the job.

And think about this: once this is all set up, there’s no reason to use the CLI to edit your plain text files. They’re just plain text files.

You can use whatever you like to edit them. And just dive down to the CLI as required.

But still, I think this is a valuable exercise. So have a play with pico, create a few files, edit a few files, and let me know how you get on.

Next, we’re going to go straight for the hledger installation page. 😬

# Ellane responds...

Challenge accepted! You’re right about not needing to use the CLI to edit my files; it’s just a vehicle for learning a skill. A mountain to climb, not to build a house on.

I’m looking forward to the next bit! I messed around with installing hLedger last year, but never understood what I was doing, or how to update to the latest version.

## Later that day...

Ahah— a challenge for both of us! I've followed your instructions to the best of my ability, and am stuck.

"You can just type `pico` and it will open".

What will open? I managed to use Terminal to create a new file in the location of my choice, but not to open an existing file. If I type `less` I can read the file, but not edit it.

This is the kind of roadblock that would have made me give up in the past—but not now! I'll keep trying to work it out.

## Johnny...

Okay, we have two possibilities here.

Just like with any other text editor, you can either:

1. Open it ‘empty’, and start typing a new document, or
2. Open it with an existing document.

It never hurts to have a look at the first line of the man page, `man pico`:

`pico [ options ] [ file ]`

So:

- `pico`, then
- some optional [options], then
- optionally, a [file].

Ignoring the optional options, this gives us two paths... which might sound familiar?…

## Ellane...

I did it! Pico is more familiar with its `⌃T` commands, but you've introduced me to `j` and `k` for moving around, and so I've been spoiled with single letter commands!

So… I jumped off the cliff into `vim` land. And I like it! With `:q!` under my belt I'm having fun learning how to navigate a doc.

## Johnny...

Ha! What! This is excellent.

There are many, many fine `vim` tutorials out there. And really once you’ve got the hang of it, ten commands gets you by.

Next stop: Homebrew. 🚏 Give me a day or so. We’re heading to the National Library to work today, it’s our happy focus place.

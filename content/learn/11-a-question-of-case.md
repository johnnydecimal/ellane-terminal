---
title: A question of case
description: Ellane wonders about case-sensitivity.
author: Ellane
date: 2024-06-04T07:45:26
tags:
  - concept
  - filesystem
mastodon: https://pkm.social/@ellane/112555732018896440
---

I successfully `cd`d to `"A_folder_in_quotes"` by typing `cd \"A` and then pressing `<tab>`.

Then I navigated to a folder with word spaces inside my Obsidian vault, which is nestled four folders deep (don't judge), and pressed `<tab>` to auto complete its name, which is `ALL THE NOTES`.

Terminal completed the string like this: `cd ALL\ THE\ NOTES`.

If I was typing it I'd have initially thought to put the backslash close to the next word, but now I can see that it's immediately preceding the word space, which is the thing we need to escape.

## `this\that`

I tried to `cd` to the this/that folder two ways: `cd this\/that` didn't work (and I don't know why), while `cd "this/that" ` did.

> Johnny: Look at this one more closely!
>
> It should be `this\that` — the same backslash that you use for the escape character.
>
> The puzzle is: how do you include the escape character in an argument _if it's the escape character?_

Classic error! Okay, I've named the folder correctly now. The answer is, you use two of them: `cd this\\that`

---

# Is case important?

Question: is case important? It doesn't seem to be. I've noticed that `cd Desktop` returns `ellane@macbook-pro Desktop % `, while `cd desktop` returns `ellane@macbook-pro desktop %`.

It's the same location each time, so I'll assume location names aren't case sensitive unless you tell me otherwise.

## What's a tty?

One more question: what's `ttys000`? And why the `%` sign? I seem to remember a `$` sign being there last time.

```txt
Last login: Mon Jun 3 13:29:54 on ttys000
ellane@macbook-pro ~ %
```

It's good to learn the why behind things that look different to my GUI-trained eyes.

I used to view things like slashes that went the wrong way and underscores between words as tech-virtue signalling: We're More Technical and Clever Than You So We Wrap Things In Extra Bits Because We Can. Seems silly now!

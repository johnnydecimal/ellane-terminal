---
title: It does not like spaces
description: The CLI doesn't handle spaces in file names very well.
author: Ellane
date: 2024-06-03T06:39:02
tags:
  - command
  - filesystem
mastodon: https://pkm.social/@ellane/112549360746816133
---

I’ve managed to change directory to pretty much everywhere, which is cool! Got a bit carried away trying to see the contents of a folder quite deep in multiple subfolders, and saw a `zsh: permission denied` message.

This was puzzling until I realised I’d forgotten to preface the path with a command!

Something else I’ve noticed is that the CLI does _not_ like word spaces. It returns a `too many arguments` message any time I try to access a folder with a multiple-word name.

Is there any way around that, or do I have to rename_everything_to_remove_word_spaces?

Rather than renaming, I looked for paths with locations that were one word only and was able to `ls` the contents of the parent folder of the directory I was looking at.

So far so good.

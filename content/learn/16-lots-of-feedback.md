---
title: Lots of feedback
description: A bunch of feedback with Johnny's comments.
author: Ellane
date: 2024-06-08T06:21:39
tags:
  - command
  - concept
mastodon: https://pkm.social/@ellane/112579664940473735
---

This one has taken me a while to work through, lots to take in.

Firstly, why _yes_, I do happen to have a plain text file or two handy! And I note that `.md` seems to fall under the `.txt` umbrella. Nice.

> **Johnny**
>
> Good spotting! And in fact the CLI doesn't give a hoot about those file extensions. It's what's _in_ the file that counts. You can call it `myfile.sausages` and as long as it's actually text, and not sausages, it'll open just fine.

These exercises began with the frustration of it taking me what felt like an age to navigate to a folder with text files long enough to work with. Autocomplete didn't seem to be working so I reviewed the lesson on that topic. Great! Clear on that at last.

Until I mistakenly pressed tab to summon auto complete with one quote mark at the beginning of a word—it's obvious I should have omitted it, but now I've got `[dquote>` and I don't know what to do with it. None of the commands I've learned thus far helped (including `logout`, `q`) so I closed the window with the red corner dot and opened a new one.

> **Johnny**  
> I do that all the time! It thinks you want to split that text over multiple lines -- because you've opened a quote, but you haven't closed it yet.
>
> The easiest way out of this and _many_ other pickles is to hit `control-C`. This (usually) tells the current process to gracefully quit.
>
> I'll tell you more about this later but for now that'll be useful to know.

## Bookmarks? Shortcuts?

Is there a way to create a bookmark, a shortcut, to get to a deeply nested folder? Please say yes!

> **Johnny**  
> Yes. I've added that to [the list](/about/#later) of stuff to get to. For now, a neat trick is that you can drag a macOS folder icon in to Terminal and it'll appear as a file path.
>
> So type `cd␣`, find the folder you want in Finder, and drag it on to the window.
>
> (Note the `␣` there that we use to represent 'a space character' where it might not otherwise be so obvious.)

## Using the home-row keys

`j` and `k` are much more convenient than searching out the up and down arrow keys.

`q` for quit? It was really that simple?? Good to know. I've been stuck on pages like this in the past, not knowing how to get out.

If spacebar moves down one full page, is there a command to move back up one full page? EDIT: Forget this one—I found it.

## Wrap at word breaks?

I'm seeing character wrapping rather than word wrapping. Is there anything in the Settings to fix this? It disrupts the flow of reading.

> **Johnny**  
> Interesting ... `less` doesn't do that itself, no. I'm surprised.
>
> But! This gives me a lovely example to use in the next lesson. Watch this space.

## Capitalisation of things

Righteo, that `h` brings up shortcuts in the file viewer. Is this a file viewer, or a File Viewer? In my mind the former would be built-in, a CLI system-wide way of navigating a file, whereas the latter would be one flavour, like an app.

> **Johnny**  
> Well in this specific case, we're in `less`. Which is just _a_ file viewer. Unless I misunderstood the question?

Is `Control-E` the same as `Control-e`? When I see an upper case letter in a CLI context it feels like pressing Shift is implied. So would `Control-E` actually be `Control+Shift+E`, or is it case insensitive? Like `Command-S` on the Mac, for Save.

> **Johnny**  
> This niggles me too, but I guess it's an old convention. I _think_ -- if any readers have more history, let's have it -- that it's because `control-shift-<character>` just isn't really a thing in CLI-world. It's `control-<character>` or nothing, so the fact that it's indicated as `E` is just a style thing?
>
> But this is just me speculating. Short answer: not case-sensitive.

## Touch typing

Yes, I touch type. 85 wpm on a good day. (It's such an important skill in my book that I stooped to bribery, offering each of my children a modest cash prize if they could demonstrate it to my satisfaction. All four did, and now as adults they are proficient where many of their peers are not.)

> **Johnny**  
> I totally agree. I taught myself when I was at uni. The reasons were not noble: I was giving myself a headache copying my mate's work, looking from the screen to his work to the keyboard.
>
> So I taught myself and it's one of the best things I've ever done. (They kicked me out of uni.)

## Searching and navigating

I pressed `/` to search for this string "F.." in my text file by escaping the two periods. So far so good, but what I wanted was to be taken to the first instance, and then to the next when I was ready, etc. Searching like this highlighted the right pattern, but I had to scroll through a very long document to find each instance.

> **Johnny**  
> `g` will take you to the top of the document, then `n` will take you to the next instance.

I just typed this: "Why doesn't autocomplete work with the `less` command? Do I really have to type out the full name of the file I want to view?" before realising I'd been pressing `return` after the first part of the name, rather than `tab`.

Until this becomes (new) muscle memory, I can see I'm going to have to slow down and compare what I've learned with what my fingers are used to doing.

So. Auto complete worked when searching for a text file to open, but it returned `no such file or directory` until I added the file extension to the name. What's that all about?

> **Johnny**  
> This should work. Perhaps there were two documents with the same name but different file extensions? Your tab-completion will only take you as far as it can before it hits ambiguity. So did it stop before the extension, but you didn't notice, so when you hit `return` you didn't actually have the file extension in there?
>
> As you noted above, yeah, this is a world where you really do need to check everything. Because the CLI will do _exactly what you tell it to_, and no more.

I'm mentally framing this quote: "None of it is difficult; it's just unfamiliar."

A year or so ago I spent a week interacting with my `.md` notes exclusively in TextEdit (plain text mode), just for the experience. Those raw visuals were a good introduction for becoming familiar with the command line, I now realise.

## `man man`

Wowza, that's a lot of reading! I scanned through the man page for `man` itself, and for `less`. I can see why it's built in; that's a lot to remember. Nothing I'm not used to, though. I'm a big keyboard shortcut user in the apps I spend the most time in.

The "Convention: indicating flags and arguments" section of this lesson feels like deep water. If you've never used any of those options to `man`, chances are high I never will either.

> **Johnny**  
> Yeah don't stress about that -- or the volume of information in many other man pages. I showed you that just to drill home the paths-and-options-and-arguments thing, as it's so fundamental.
>
> Honestly 90% of man pages I open, skim for the tiny thing I need, and quit. They can be inscrutable and scary.

I'll leave it here, and spend the next few days playing around with man (oh gosh, the dad jokes around this one must be plentiful!).

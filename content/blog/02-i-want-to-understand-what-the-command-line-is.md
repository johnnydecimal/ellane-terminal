---
title: What is the command line?
description: A very high-level introduction to the command line. What even is it? Why would we use it?
author: Johnny
date: 2024-05-28T02:00:00
tags:
  - concept
  - language
---

Your computer has many 'languages', or ways of 'thinking', internally.

The phrase '(it's all just) [ones and zeroes](https://en.wiktionary.org/wiki/ones_and_zeroes)' represents the fact that, at its very lowest level, your computer is literally just passing around information that looks like `1010111110101000100111010010110010`.

(It's made of transistors, and they can only be on `1` or off `0`.)

That's not very friendly for us humans, so over the years we've abstracted away from `1010111...` by creating **higher-level languages.** The next-least-complicated language is called **assembly**.[^assembly]

[^assembly]: This is not a scientifically complete list of computer languages.

```asm6502
LDA #$01
STA $0200
LDA #$05
STA $0201
LDA #$08
STA $0202
```

Okay, still not what you'd call friendly. Let's try some **JavaScript:** a higher-level language than assembly.

```js
const firstname = "Johnny";
const nickname = "Decimal";
const surname = "Noble";

console.log(`Hi, ${firstname} ‘${nickname}’ ${surname}.`);
```

Better! You don't have to know JavaScript to at least guess what that's going to do.

If we keep going, we can abstract away this idea of languages entirely, and end up with the **graphical user interface,** or **GUI.**

<img src="/img/02.01-mess-error-image9-398x191.png" width="398" height="191" />

So why would you bother learning a language when you can just go around clicking buttons?

## Control

You can click a button because some designer in Seattle designed the program to have a button.

But what if you want more granular control? What if there isn't a button for the thing you want to do?

**Then you crack open the command line.**

Because at the end of the day, that button passed a command to a high-level language which translated it and passed it down to a lower-level language which translated it to assembly which your computer translated to ones and zeros which is all it can understand.

So if you can insert yourself in that chain, if you can start talking some of these higher-level languages, you can get more control. You can do whatever you want.

**The command line is how you talk to your computer in a high-level language.**

Next, I'll explain how you do that.

---

# Homework

Do a bit of reading on [abstraction layers](https://en.wikipedia.org/wiki/Abstraction_layer). But you don't need to go deep on theory here: as long as you've got the idea, we'll move on.

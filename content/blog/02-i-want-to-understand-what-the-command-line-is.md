---
title: I want to understand what the command line is
description: This is a post on My Blog about leveraging agile frameworks.
author: Johnny
date: 2024-05-28T03:57:38
tags:
  - concept
---

Your computer has many 'languages', or ways of 'thinking', internally.

The phrase 'ones and zeros' represents the fact that, at its very lowest level, your computer is literally just passing around data that looks like `101010100101010100101001010110010`.

That's not very friendly for us humans, so over the years we've abstracted away from `1010111...` by creating _higher-level_ languages. The next-least-complicated language is called **assembly**.[^assembly]

```asm6502
LDA   $60
ADC   $61
STA   $62
```

Okay, still not what you'd call friendly. Let's try some JavaScript: a higher-level language still than assembly.

```js
const firstname = "Johnny";
const nickname = "Decimal";
const surname = "Noble";

console.log(`Hi, ${firstname} ‘${nickname}’ ${surname}.`);
```

Better! You don't have to know JavaScript to at least guess what that's going to do.

If we keep going, we can abstract away this idea of languages entirely, and end up with the **graphical user interface,** or **GUI.**

{% image "./img/02.01-mess-error-image9.png", "A possum parent and two possum kids hanging from the iconic red balloon" %}

[^assembly]: This is not a scientifically complete list of computer languages.

---
layout: default
title: Standard Input
nav_order: 7
has_children: true
permalink: /docs/standard_input
---

{: .fs-6 .fw-300 }

## Standard Input

---

### Background Information

The Terminal and terminal emulators are the software a user interfaces with to issue commands to the shell. The shell then parses the commands and sends it to the kernel.

The Terminal reads and writes information as streams. The input stream is called _Standard Input_ (stdin) and the output stream is called _Standard Output_ (stdout). There is also something called _Standard Error_ (stderr) which is thrown when a problem occurs.

These streams can be redirected to other processes (programs) but the default is the Terminal. This is why after you issue a command you can see the result (output) displayed on the Terminal.

A simplified explanation is the Standard Output from a command can be ‘piped’ as the Standard Input of another process. This can be chained indefinitely but the final output will be either your terminal or a file.
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

### Introduction

Terminal and terminal emulators are software a user interfaces with to issue commands to the shell. The shell then parses the commands and sends it to the kernel.

The terminal reads and writes information as streams. The input stream is called _standard input_ (stdin) and the output stream is called _standard output_ (stdout). There is also something called _standard error_ (stderr) which is thrown when a problem occurs.

These streams can be redirected to other processes but the default is the terminal. This is why after you issue a command you can see the output displayed on the terminal.

A simplified explanation is the standard output from a command can be ‘piped’ as the standard input of another process. This can be chained an unlimited number of times but the final output will be either your terminal or a file.

---

### File Descriptor

A File Descriptor is a number used to represent stdin, stdout, and stderr.

| type   | file descriptor |
| :----- | :-------------- |
| stdin  | 0               |
| stdout | 1               |
| stderr | 2               |

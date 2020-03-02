---
layout: default
title: Processes
nav_order: 6
has_children: true
permalink: /docs/processes
---

## Processes

Introduction to Linux processes
{: .fs-6 .fw-300 }


A process represents something running on your computer. They are classified into two types, foreground processes and background processes. Foreground processes are interactive and require some type of input. Launching a foreground process ties up the terminal so you can not issue new terminal commands until the processes terminates. Background processes can run independently and do not tie up the terminal.

Processes usually terminate after you exit. However, this is not always the case as some programs may keep some processes running even after you exit. There are also times when you may want to kill some processes to free up resources or because the program froze.

This section will explain:
* the different states of processes on Linux,
* how to view processes on the Linux command line,
* search for certain processes,
* how to kill processes,
* and background processes.
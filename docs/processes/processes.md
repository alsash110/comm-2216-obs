---
layout: default
title: Processes
nav_order: 6
has_children: true
permalink: /docs/processes
---

## Processes
{: .fs-6 .fw-300 }

### Introduction to Linux processes

A _process_ represents something running on your computer. They are classified into two types, _foreground processes_ and _background processes_. _Foreground processes_ are interactive and require some type of input. Launching a _foreground process_ ties up the terminal so you can not issue new terminal commands until the processes terminates. _Background processes_ can run independently and do not tie up the terminal.

Processes usually terminate after you exit. However, this is not always the case as some programs may keep some processes running even after you exit. There are also times when you may want to _kill_ some processes to free up resources or because the program froze.

This section will explain:
* the different states of processes on Linux,
* how to view processes on the Linux command line,
* search for certain processes,
* how to _kill_ processes,
* and background processes.
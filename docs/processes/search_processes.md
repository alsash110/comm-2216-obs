---
layout: default
title: Search Processes
parent: Processes
nav_order: 3
---

{: .fs-6 .fw-300 }

## Searching Specific Processes
{: .no_toc }

### Table of Contents
{: .no_toc .text-delta }

* TOC
{:toc}

---

### The `pgrep` Command

The `pgrep` command searches specifically for the process id `PID` of a process.
This is a very useful command if you know what the process is called and want to quickly identify each _process id_ associated with it.

In the example below I've launched firefox and opened a terminal.
If you use `pgrep firefox` it will return a list of all processes with the `firefox` keyword.

>> *`pgrep firefox`*  >-->  **[Enter]**

![Screen shot of pgrep firefox output](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/processes/pgrep_1.png?raw=true "pgrep firefox output")
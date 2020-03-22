---
layout: default
title: Navigating your system
parent: Navigating the File System
nav_order: 3
---

{: .fs-6 .fw-300 }

# Navigating Your System
{: .no_toc }

---

## Using Commands To Navigate

There are a number of commands we can use to navigate the Linux file system in the terminal. This section will use many of the list of commands and teach you to be more familiar with navigating through your Linux system with the terminal.

---

## `pwd`

The `pwd` command is used to identify your current location. It returns the full path of where your terminal is currently in, relative to the directory structure.

---

## `ls`

The `ls` command is used to list all files and directories at your terminal's current location. This is useful if you want to identify and traverse in to sub-directories.

Passing the `ls` command the `-a` switch lists all hidden files as well.

The `-l` switch is used to format the display so its easy to read.

---

## `cd`

The `cd` command is used to "change directories". Issuing the command without any arguments or with the `~` argument results in changing to your _home directory_.

You can pass `cd` a relative path or an absolute path as the argument. Relative path means you want to go in to a sub-directory. Heres an example:

![Screen shot cd](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/navigation/commands/cd_rel.png?raw=true "cd")

You can also pass `.` or `..` as an argument. `cd .` means you want to change to your current directory (so you didn't go anywhere). `cd ..` means you want to change to your locations parent directory. Heres an example:

![Screen shot cd](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/navigation/commands/cd_bck.png?raw=true "cd")

`cd -` returns you to your previous location, but you can only backtrack once.

---

## Summary

* Commands are instructions to perform tasks in Linux. You can specify options (switches) and pass arguments to commands but they differ between each command.

* The three most commonly used commands to navigate the file system in Linux are: `pwd`, `ls`, and `cd`.

The next section will cover how to look up a commands functionality, the _manual_ page or _man pages_.

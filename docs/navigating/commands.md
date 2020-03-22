---
layout: default
title: Commands
parent: Navigating the File System
nav_order: 3
---

{: .fs-6 .fw-300 }

# Commands
{: .no_toc }

This section introduces commands, lists some common commands and describes how to use them.

---

### Table of Contents
{: .no_toc .text-delta }
* TOC
{:toc}

---

## What are Commands

Commands are instructions the operating system uses to perform specific tasks. It provides a _layer of abstraction_ and makes it easier for users to use a computer without the need to know how things work.

We can think of them as _keywords_ that are _mapped_ to a mini program which will execute when we input it into a _terminal_.

Linux commands have set syntax which allows additional _options_ (_switches_) and _arguments_ to be passed. The syntax looks something like this:

>> _command_ [_options_] [_arguments_]

Things we should pay attention to:

1. The command, options (switch), and arguments must be separated by spaces.
1. Short command options starts with `-`. They can be grouped and the order does not matter.
1. Long command options starts with `--`.
1. The command reads from left to right so _options_ and _arguments_ reference to the command on the left.
1. The type of _options_ available and _arguments_ accepted will depend on the command.

Here is an example:

>> `ls -la /etc`

`ls` is the command, `-la` is the option (switch), and `/etc` is the argument.

This is the same as:

>> `ls -al /etc`

>> `ls -l -a /etc`

>> `ls --all -l /etc`

---

## Command Table

Heres a taste of some commands.

| Command         | Description                                                                                             |
| :--------       | :------------------------------------------------------------------------------------------------------ |
| `ls`            | "List" all visible files and folders in the current directory.                                          |
| `pwd`           | "Print working directory" shows your current directory location.                                        |
| `cd`            | "Change directory" to a specified directory or your home directory.                                     |
| `open`          | "Open" a specified file, application, or directory.                                                     |
| `stat`          | Display information about a file or folder.                                                             |
| `clear`         | "Clear" your terminal screen.                                                                           |
| `exit`          | "Exits" a terminal or a terminal session.                                                               |
| `whoami`        | Displays who you are.                                                                                   |
| `who`           | Displays who's logged in.                                                                               |
| `last`          | Lists user login history.                                                                               |
| `bc`            | Launch a terminal calculator.                                                                           |
| `history`       | Lists a "history" of issued commands.                                                                   |
| **[Up Arrow]**  | Scrolls through most recent command.                                                                    |

---

## Using Commands To Navigate

There are a number of commands we can use to navigate the Linux file system in the terminal. This section will go over the most commonly used commands.

---

### `pwd`

The `pwd` command is used to identify your current location. It returns the full path of where your terminal is currently in, relative to the directory structure.

---

### `ls`

The `ls` command is used to list all files and directories at your terminal's current location. This is useful if you want to identify and traverse in to sub-directories.

Passing the `ls` command the `-a` switch lists all hidden files as well.

The `-l` switch is used to format the display so its easy to read.

---

### `cd`

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

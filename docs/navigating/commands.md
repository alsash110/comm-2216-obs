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

Linux commands have set syntax which allows additional _options_ and _arguments_ to be passed. The syntax looks something like this:

>> _command_ [_options_] [_arguments_]

Things we should pay attention to:

1. The command, options, and arguments must be separated by spaces.
1. Short command options starts with `-`. They can be grouped and the order of the option switches do not matter.
1. Long command options starts with `--`.
1. The command reads from left to right so _options_ and _arguments_ reference to the command on the left.
1. The type of _options_ available and _arguments_ accepted will depend on the command.

Here is an example:

>> `ls -la /etc`

`ls` is the command, `-la` is the switch, and `/etc` is the argument.

This is the same as:

>> `ls -al /etc` or `ls -l -a /etc` or `ls --all -l /etc`

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

## Using Commands To Navigate

There are a number of commands we can use to navigate the Linux file system in the terminal. This section will go over the most commonly used commands.

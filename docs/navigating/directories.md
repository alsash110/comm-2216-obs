---
layout: default
title: Directories
parent: Navigating the File System
nav_order: 2
---

{: .fs-6 .fw-300 }

## The Concept of Directories
{: .no_toc }

---

### Table of Contents
{: .no_toc .text-delta }
* TOC
{:toc}

---

### Directories

Linux directories behave similar to folders. In the background, directories are actually a special type of file used to store information about other files. It's contents are controlled by the Linux operating system and it includes things such as name, permission, type, size, and so on.

The home directory for common users are located in `/Users` while the _root user_ is stored in a separate `/root` directory. If you are wondering what the difference is between common users and the _root user_, it will be covered in a separate section.

As an example, if a users has an account named Don, their _default directory_ (unless changed) is `/Users/Don`.
You can check your default directory by opening a terminal and typing:

>> *`pwd`*  >-->  **[Enter]**

![Screen shot pwd](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/navigation/directories/pwd.png?raw=true "pwd")

This directory (or _path_) is where all commands are referenced from and this is called a _relative reference_.

---

### Relative reference vs Absolute reference

There are two types of references in Linux, _relative reference_ and _absolute reference_. _Relative reference_ refers to the directory you are currently in while _absolute reference_ refers to the _root path_. _Absolute references_ starts with the `/`, for example `/Users`.

It is important to know what you are referencing when issuing a command. Open a new terminal and type:

>> *`ls`*  >-->  **[Enter]**

![Screen shot ls](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/navigation/directories/ls_rel.png?raw=true "ls")

The output of the command is based on its _relative reference_, which is always your _home directory_ when you open a new terminal.

To specify an _absolute reference_ to the ls command:

>> *`ls /users`*  >-->  **[Enter]**

![Screen shot ls](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/navigation/directories/ls_abs.png?raw=true "ls")

The output is different because `ls` is given an _absolute path_ and will list all files and directories stored in the _absolute path_.

---

### Summary


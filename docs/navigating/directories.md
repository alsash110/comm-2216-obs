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

As an example, if a users has an account named Don, their _home directory_ (unless changed) is `/Users/Don`.
You can check your default directory path by opening a new terminal window and typing:

>> *`pwd`*  >-->  **[Enter]**

![Screen shot pwd](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/navigation/directories/pwd.png?raw=true "pwd")

---

### Relative vs Absolute Path

There are two types of _paths_ in Linux, _relative path_ and _absolute path_. _Relative path_ refers to the directory you are currently in while _absolute path_ refers to the _root path_. _Absolute paths_ always starts with the `/`, for example `/Users`.

It is important to know what _path_ you are referencing when issuing a command. Open a new terminal and type:

>> *`ls`*  >-->  **[Enter]**

![Screen shot ls](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/navigation/directories/ls_rel.png?raw=true "ls")

![Note icon](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/icons/note.png?raw=true "Note"){: .image-left } You may have noticed that nothing was specified after the `ls` command. By not specifying anything, this implicitly tells the command that this directory (or _path_) is where this command should reference from. This is called a _relative path_ and it refers to the directory location you are currently in. Typically your _home directory_ is the default _path_ when you open a new terminal.

To specify an _absolute reference_ to the ls command:

>> *`ls /users`*  >-->  **[Enter]**

![Screen shot ls](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/navigation/directories/ls_abs.png?raw=true "ls")

The output is different from the previous example because the `ls` command is explicitly given an _absolute path_ (starts with `/`). This causes the command to use the specified path to list all files and directories stored at that location.

---

### Summary

There are two types of paths in Linux. Relative path refers to the current location and absolute path refers to an exact location. It is important to keep this in mind when issuing commands as it may result in unexpected command outputs.

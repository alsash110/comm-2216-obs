---
layout: default
title: Concept of Directories
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

An analogy for linux directories is folders. In actuality, directories are a special type of file used to store information about other files. It's contents are controlled bt the system and it includes things such as name, permission, type, size, and so on.

The home directory for non root users are in the `/Users` directory and for the root user it is `/root`.
For example, if a users has an account named Don, their _default directory_ (unless changed) is `/Users/Don`.
You can check your default directory by opening a terminal and typing:

>> *`pwd`*  >-->  **[Enter]**

![Screen shot pwd](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/navigation/directories/pwd.png?raw=true "pwd")


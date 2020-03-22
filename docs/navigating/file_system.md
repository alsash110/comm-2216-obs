---
layout: default
title: Linux File System
parent: Navigating the File System
nav_order: 1
---

{: .fs-6 .fw-300 }

# The Linux File System
{: .no_toc }

This section covers the basic Linux file system concepts.

---

### Table of Contents
{: .no_toc .text-delta }
* TOC
{:toc}

---

## Background

The purpose of a computers _file system_ is to load and store information in a _non volatile_ manner.

In Linux, "everything is a file" (technically a [_inode_](https://en.wikipedia.org/wiki/Inode)) and every file is stored in the `/` (_root_) directory. Linux's file system follows a _hierarchical directory structure_. This means that the _root directory_ is at the top of the hierarchy and everything else in the file system branches from it, this even includes _partitions_.

If you are familiar with Windows, _partitions_ refer to the drive letters such as `C:\` or `D:\` and so on. In Linux, these partitions are located in `/dev` and are named `sda` followed by a number.

---

![Note icon](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/icons/note.png?raw=true "Note"){: style="float: left" }
>> To open a terminal window, launch the terminal app or right click on the desktop and select `open in terminal`.

---

We can look for it if open a new terminal and type the following:

>```bash
>ls -la /dev
>```

![Screen shot of ls -la /dev/](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/navigation/file_system/sda.png?raw=true "/dev")

---

![Note icon](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/icons/note.png?raw=true "Note"){: style="float: left" }
>> If you are using a browser based terminal emulator, the output may be different.

---

The image above shows that the `/dev/sda`, `/dev/sda1`, `/dev/sda2`, `/dev/sda5`, and `/dev/sg0` are all under the disk _group_. We will go in to more detail about _groups_ later in another section.

This tutorial will not go into detail about how Linux manages its data storage and file formats. If you are interested, [wikipedia](https://en.wikipedia.org/wiki/File_system#Linux) has lots more information.

---

## Summary

Linux operates on the _root_ directory and everything is stored in it. The _root_ directory is represented as `/` and there is no parent directory above it.

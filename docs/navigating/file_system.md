---
layout: default
title: Linux File System
parent: Navigating the File System
nav_order: 1
---

{: .fs-6 .fw-300 }

## The Linux File System
{: .no_toc }

---

### Table of Contents
{: .no_toc .text-delta }
* TOC
{:toc}

---

### Background

The purpose of a computers _file system_ is to load and store information in a _non volatile_ manner.

In Linux, "everything is a file" (_inode_) and every file is stored in the `/` (_root_) directory. Linux's file system follows a _hierarchical directory structure_. This means that the _root directory_ is at the top of the hierarchy and everything else in the file system branches from it, this even includes partitions.

If you are familiar with windows, partitions refer to the drive letters such as `C:\` or `D:\` and so on. In Linux, these partitions are found in `/dev/sda` followed by a number representing which partition.

>> *`ls -la /dev`*  >-->  **[Enter]**

![Screen shot of ls -la /dev/](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/navigation/file_system/sda.png?raw=true "/dev")

The image above shows that the `/dev/sda`, `/dev/sda1`, `/dev/sda2`, `/dev/sda5`, and `/dev/sg0` are all under the disk _group_. We will go in to more detail about _groups_ later in another section.

This tutorial will not go into detail about how Linux manages its data storage and file formats. If you are interested, [wikipedia](https://en.wikipedia.org/wiki/File_system#Linux) has lots more information.

---

### Summary

Linux operates on the _root_ directory and everything is stored in it. The _root_ directory is represented as `/` and there is no parent directory above it.

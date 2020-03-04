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

A _file system_ is used to load and store information in a _non volatile_ way.

In Linux, everything is stored in the `/` (root) directory and follows something whats known as a _hierarchical directory structure_. This means that the _root directory_ is at the top of the hierarchy and everything else in the file system branches from it, this even includes partitions.

If you are familiar with windows, partitions refer to the drive letters such as `C:\` or `D:\` and so on. In Linux, these partitions are found in `/dev/sda` followed by a number representing which partition.

>> >> `ls -la /dev`  >-->  **[Enter]**

![Screen shot of ls -la /dev/](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/navigation/file_system/sda.png?raw=true "/dev")

This image shows that the `/dev/sda`, `/dev/sda1`, `/dev/sda2`, `/dev/sda5`, and `/dev/sg0` are all under the disk _group_.

This tutorial will not go over the data storage format and other details. Feel free to research if you are inclined.
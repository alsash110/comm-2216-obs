---
layout: default
title: Killing Processes
parent: Processes
nav_order: 4
---

{: .fs-6 .fw-300 }

## Killing Processes by PID
{: .no_toc }

---

### Table of Contents
{: .no_toc .text-delta }
* TOC
{:toc}

---

###  The `kill` Command

Once we know the _PID_ of a process, we can issue a _kill command_ to terminate the process.

>> *`pgrep firefox`*  >-->  **[Enter]**
>> *`kill 2513`*  >-->  **[Enter]**

![Screen shot of PID](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/processes/kill_1.png?raw=true "PID")
![Screen shot of kill output](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/processes/kill_2.png?raw=true "kill output")

Keep in mind that the _PID_ is unique to that process and is not the same each time you run it. _PID_ also can not be changed and you may have multiple processes that are the same running on different _PID_.
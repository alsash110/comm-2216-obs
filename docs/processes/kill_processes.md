---
layout: default
title: Killing Processes
parent: Processes
nav_order: 4
---

## Killing Processes by PID

Once we know the _PID_ of a process, we can issue a _kill command_ to terminate the process.

> *`pgrep firefox`*  >-->  **[Enter]**
> *`kill 2513`*  >-->  **[Enter]**

![Screen shot of PID](../images/processes/kill_1.png "PID")
![Screen shot of kill output](../images/processes/kill_2.png "kill output")

Keep in mind that the _PID_ is unique to that process and is not the same each time you run it. _PID_ also can not be changed and you may have multiple processes that are the same running on different _PID_.
---
layout: default
title: View Processes
parent: Processes
nav_order: 2
---

{: .fs-6 .fw-300 }

## How to View Processes
{: .no_toc }

---

### Table of Contents
{: .no_toc .text-delta }
* TOC
{:toc}

---

The two most common commands used to view processes are the process status `ps` and the `top` command. The difference between the two is that `ps` takes a snapshot while `top` continuously updates its list of processes.


The `pgrep` command searches specifically for the process id `PID` of a process.
This is a very useful command if you know what the process is called and want to quickly identify each _process id_ associated with it.
---

### The `ps` Command

1. Open up your terminal.

2. Input the following `ps` command.

    *`ps aux`*

    You should be able to see a list of all processes running on your machine.

    ![Screen shot of ps aux output](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/processes/ps_aux_1.png?raw=true "ps aux output")
    ![Screen shot of ps aux output](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/processes/ps_aux_2.png?raw=true "ps aux output")

    There is a lot more information given, we can see the different _users_, _process id_ `PID`, _state_ `STAT`, when the processes started, and the _root directory_ or _alias_ where the processes loaded from.

3. Input the `pgrep` command and your process name.

    **Note**: processname is a keyword to search for your process name.

    *`pgrep processname`*

    **Note**: The id of a process is different every time you start a process. If the process name exists, you will be able to see the id of your process, as shown below.

    ![Screen shot of pgrep firefox output](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/processes/pgrep-firefox.png?raw=true "pgrep firefox output")

4. Input the `kill` command along with the process id to stop your desired process.

    *`kill processid`*

5. Input the `pgrep` command once more to test if the process did in fact stop.

    *`pgrep processname`*

    If the process did get stopped, there should be no output.

    ![Screen shot of no pgrep firefox output](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/processes/pgrep-firefox-killed.png?raw=true "no pgrep firefox output")

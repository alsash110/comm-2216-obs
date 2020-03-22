---
layout: default
title: Processes
nav_order: 6
has_children: true
permalink: /docs/processes
---

{: .fs-6 .fw-300 }

# Processes

---

A _process_ represents something running on your computer. They are classified into two types, _foreground processes_ and _background processes_. _Foreground processes_ are interactive and require some type of input. Launching a _foreground process_ ties up the terminal so you can not issue new terminal commands until the processes terminates. _Background processes_ can run independently and do not tie up the terminal.

The two most common commands used to view your systems processes are through the ```ps aux``` and ```top``` commands. The difference between the two is that ```ps aux``` takes a snapshot of current processes while ```top``` continuously updates the list of processes.

Processes usually terminate after you exit. However, this is not always the case as some programs may keep some processes running even after you exit. There are also times when you may want to _kill_ some processes to free up resources or because the program froze.

---

### Table of contents
{: .no_toc .text-delta }
* TOC
{:toc}

---

## Display, Search, and Kill Processes Using the Terminal

The following instruction set will show you how to:
* view processes using the ```ps``` command,
* search for a specific process, and
* _kill_ processes using your terminal.

---

**1.** Input the following ```ps``` command inside of your terminal.

>```
>ps aux
>```

>**Note**: Using ```aux``` displays a lot more information given, we can see the different _users_, _process id_ `PID`, _state_ `STAT`, when the processes started, and the _root directory_ or _alias_ where the processes were loaded from.

>You should be able to see a list of all processes running on your machine.

>![Screen shot of ps aux output](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/processes/ps_aux_1.png?raw=true "ps aux output")
>![Screen shot of ps aux output](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/processes/ps_aux_2.png?raw=true "ps aux output")
<br />
<br />

**2.** Input the ```pgrep``` command and your process name to obtain the *`processid`* of your process.

>**Note**: Replace processname with a keyword to search for your process name.

>```
>pgrep processname
>```

>**Note**: The id of a process is different every time you start a process. If the process name exists, you will be able to see the id of your process, as shown below.

>![Screen shot of pgrep firefox output](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/processes/pgrep-firefox.png?raw=true "pgrep firefox output")
<br />
<br />

**3.** Input the ```kill``` command along with the *`processid`* to stop your desired process.

>![Caution icon](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/icons/caution.png?raw=true "Caution"){: style="float: left" } 
>>Ensure you input the correct process id or you may accidentally kill an essential process.

>```
>kill processid
>```
<br />

**4.** Input the ```pgrep``` command along with the same *`processname`* once more to test if the process did in fact stop.

>```
>pgrep processname
>```

>If the process did get stopped, there should be no output for that specific process.

>![Screen shot of no pgrep firefox output](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/processes/pgrep-firefox-killed.png?raw=true "no pgrep firefox output")
<br />
<br />

By reaching the end of this instruction set, you will have successfully learned how to view, search for, and kill any process.

You can see that finding and ending processes can be done through the terminal and without much of a hassle. Just be sure that whenever you do decide to kill a process that you ensure that the process id is correct.

---

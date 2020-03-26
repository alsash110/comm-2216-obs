---
layout: default
title: Processes
nav_order: 6
has_children: false
permalink: /docs/processes
---

{: .fs-6 .fw-300 }

# Processes

---

A _process_ represents something running on your computer. There are two types of processes: _foreground processes_ and _background processes_. _Foreground processes_ are interactive and need some type of input. Launching a _foreground process_ ties up the terminal so you can not issue new terminal commands until the processes terminate. _Background processes_ can run independently and do not tie up the terminal.

The two most common commands you can use to view your systems processes are the ```ps aux``` and ```top``` commands. The difference between the two is that ```ps aux``` takes a snapshot of current processes while ```top``` updates the list of processes.

Processes usually end after you exit. This is not always the case as some programs may keep some processes running even after you exit. There are also times when you may want to _kill_ some processes to free up resources or because the program froze.

---

## Display, Search, and Kill Processes Using the Terminal

The following instruction set shows you how to:
* view processes using the ```ps``` command,
* search for a specific process, and
* _kill_ processes using your terminal.

---
![Note icon](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/icons/note.png?raw=true "Note"){: style="float: left" }
>> **Note**: To follow along with this instruction set, I have Firefox open, but you may open any other program or any program you want to kill.
<br />
<br />

**1.** Open up the Firefox browser that comes with your Linux system.
<br />
<br />

**2.** Open your terminal and input the following ```ps``` command.

>```
>ps aux
>```
<br />

>![Note icon](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/icons/note.png?raw=true "Note"){: style="float: left" }
>>**Note**: The ```aux``` command displays a lot more information. We can see the different _users_, _process id_ `PID`, _state_ `STAT`, when the processes start, and the _root directory_ or _alias_ where the processes load in from.
<br />

>You should be able to see a list of all processes on your machine.

>![Screen shot of ps aux output](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/processes/ps_aux_1.png?raw=true "ps aux output")
>![Screen shot of ps aux output](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/processes/ps_aux_2.png?raw=true "ps aux output")
<br />
<br />

**3.** Input the ```pgrep``` command and your process name to obtain the *`processid`* of your process.

>![Note icon](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/icons/note.png?raw=true "Note"){: style="float: left" }
>> **Note**: Replace processname with a keyword to search for your process name. The id of a process is different every time you start a process. If the process name exists, you will be able to see the id of your process, as shown below.
<br />
<br />

>```
>pgrep processname
>```
<br />

>![Screen shot of pgrep firefox output](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/processes/pgrep-firefox.png?raw=true "pgrep firefox output")
<br />
<br />

**4.** Input the ```kill``` command along with the *`processid`* to stop your desired process.

>![Caution icon](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/icons/caution.png?raw=true "Caution"){: style="float: left" } 
>> **Caution**: Ensure you input the correct process id or you may accidentally kill an essential process.
<br />
<br />

>```
>kill processid
>```
<br />

**5.** Input the ```pgrep``` command along with the same *`processname`* once more to test if the process did in fact stop.

>```
>pgrep processname
>```

>If you killed the process, there should be no output for that specific process.

>![Screen shot of no pgrep firefox output](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/processes/pgrep-firefox-killed.png?raw=true "no pgrep firefox output")
<br />
<br />


You can find and end processes through the terminal without much of a hassle. Just be sure that whenever you do decide to kill a process that you ensure that the process id is correct.

You know most of the essentials and basics to Linux and commands at this point. We recommend you learn how they work at a slightly deeper level with a concept called [standard IO.](https://dl90.github.io/linux-basics/docs/standard_io)

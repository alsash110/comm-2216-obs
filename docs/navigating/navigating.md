---
layout: default
title: Navigating the File System
nav_order: 3
has_children: false
permalink: /docs/navigating
---

{: .fs-6 .fw-300 }

# Navigating Your System
{: .no_toc }

---

Navigating through a computer system without a graphical user interface, _GUI_ can seem daunting. The good news is, most, if not all modern distributions of Linux include a GUI.

The goal of this section is to explain and show you that navigating Linux through the _CLI_ (command-line interface) is not difficult. With enough practice, you may find that using the _CLI_ to navigate through a computer is sometimes easier and even quicker.

Using the CLI also introduces more functionalities that you may overlook while you use a _GUI_. To use the Linux _CLI_, you will use an application called the _terminal_.

---

### Table of contents
{: .no_toc .text-delta }
* TOC
{:toc}

---

## Directories

Linux directories behave similarly to folders. In the background, directories are actually a special type of file used to store information about other files. The Linux operating system controls the contents. Contents include name, permission, type, size, etc.

The home directory is under `/Users` for common users while `root` is the directory for _root user_.

---

## What are Commands

Commands are instructions the operating system uses to perform specific tasks. Instructions provide a _layer of abstraction_ and make using a computer easy without the need to know how things work.

We can think of commands as _keywords_ that are _mapped_ to a mini-program which executes when we input _keywords_ into a _terminal_.

Linux commands have set syntax which allows you to pass extra _options_ and _arguments_. The syntax looks something like this:

>> _command_ [_options_] [_arguments_]

Things you should pay attention to:

* Separate commands, options, and arguments with spaces
* Short command options start with `-`
* Long command options start with `--`
* The command reads from left to right so _options_ and _arguments_ reference to the command on the left
* The type of _options_ available and _arguments_ accepted will depend on the command

>![Note icon](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/icons/note.png?raw=true "Note"){: style="float: left" }
>> **Note:** You can find the full information about a command by using the `man` command. The syntax is `man [command]`.

---

## Command Table

Below is a list of some common Linux commands.

**Note**: This list is not exhaustive.

| Command         | Description                                                                                             |
| :--------       | :------------------------------------------------------------------------------------------------------ |
| `ls`            | "List" all visible files and folders in the current directory.                                          |
| `pwd`           | "Print working directory" shows your current directory location.                                        |
| `cd`            | "Change directory" to a specified directory or your home directory.                                     |
| `open`          | "Open" a specified file, application, or directory.                                                     |
| `clear`         | "Clear" your terminal screen.                                                                           |
| `exit`          | "Exits" a terminal or a terminal session.                                                               |
| `history`       | Lists a "history" of issued commands.                                                                   |
| **[Up Arrow]**  | Scrolls through most recent command.                                                                    |

---

## Using Commands To Navigate Your System

There are many commands we can use to navigate the Linux file system in the terminal. This instruction set uses some of the commands in the list above and teaches you to be more comfortable with navigating through your Linux system using the terminal.

---

**1.** Open up your terminal by right-clicking on your desktop and clicking *`Open Terminal`*.

>![Terminal open](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/navigation/directories/term.png?raw=true "terminal")
<br />
<br />

**2.** Input the following command into your terminal to display your current directory.

>```
>pwd
>```

>You should be able to see exactly which directory you are currently in.

>![Screen shot pwd](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/navigation/directories/pwd.png?raw=true "pwd")
<br />
<br />

**3.** Display the contents inside your current directory with the following command.

>![Note icon](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/icons/note.png?raw=true "Note"){: style="float: left" }
>> **Note**: Using the `ls` command with the `-a` switch lists all hidden files as well.

<br />
>```
>ls
>```

>You can see a list of everything inside your current directory.

>![Screen shot ls](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/navigation/directories/contents.png?raw=true "ls")
<br />
<br />

**4.** Create a new folder inside your current directory by using the following command.

>```
>mkdir testfolder
>```

>Check the contents of your current directory again by inputting the `ls` command again.

>```
>ls
>```

>You will see that you have successfully created a new folder called *`testfolder`*.

>![Screen shot ls with testfolder](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/navigation/directories/contents2.png?raw=true "ls")
<br />
<br />

**5.** Change into the *`testfolder`* directory with the following command.

>![Note icon](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/icons/note.png?raw=true "Note"){: style="float: left" }
>>**Note**: The input after `cd` is the name of the directory you want to change into.

<br />
>```
>cd testfolder
>```

>Check to see which directory you are now currently in with the `pwd` command.

>```
>pwd
>```

>You will see that you are now inside the *`testfolder`* directory.

>![pwd2](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/navigation/directories/pwd2.png?raw=true "ls")
<br />
<br />

**6.** Change back to the previous directory with the following command.

>![Note icon](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/icons/note.png?raw=true "Note"){: style="float: left" }
>> **Note**: By adding `..`, you can jump back up one parent directory. Using `cd -` can also return you to your previous location, but you can only backtrack once.
<br />
<br />

>```
>cd ..
>```

>You can see you have returned back to the previous directory that you were in.

>![Screen shot pwd](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/navigation/directories/pwd.png?raw=true "pwd")
<br />
<br />

By reaching the end of this instruction set, you now know how to open the terminal and input commands which allowed you to navigate through your system. 

Now you are able to see files in your directories as well as your current directory, allowing you to easily navigate through your system.

The next step is to learn how to [create users and assign privileges.](https://dl90.github.io/linux-basics/docs/users)

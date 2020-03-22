---
layout: default
title: Navigating the File System
nav_order: 3
has_children: true
permalink: /docs/navigating
---

{: .fs-6 .fw-300 }

# Navigating Your System
{: .no_toc }

---

Navigating through a computer system without a  graphical user interface, _GUI_, can seem daunting. The good news is, most if not all modern distributions of Linux includes a GUI.

The goal of this section is to explain and show you that navigating Linux through the _CLI_ (command-line interface) is not difficult. With enough practice, you may find that using the _CLI_ to navigate through a computer is sometimes easier and even quicker.

Using the CLI also introduces additional functionalities that may have been overlooked in a _GUI_. To use the Linux _CLI_, we will be using an application called _terminal_.

---

### Table of contents
{: .no_toc .text-delta }
* TOC
{:toc}

---

## What are Commands

Commands are instructions the operating system uses to perform specific tasks. It provides a _layer of abstraction_ and makes it easier for users to use a computer without the need to know how things work.

We can think of them as _keywords_ that are _mapped_ to a mini program which will execute when we input it into a _terminal_.

Linux commands have set syntax which allows additional _options_ and _arguments_ to be passed. The syntax looks something like this:

>> _command_ [_options_] [_arguments_]

Things we should pay attention to:

* The command, options, and arguments must be separated by spaces.
* Short command options starts with `-`. They can be grouped and the order does not matter.
* Long command options starts with `--`.
* The command reads from left to right so _options_ and _arguments_ reference to the command on the left.
* The type of _options_ available and _arguments_ accepted will depend on the command.

---

## Command Table

Below is a list of some of the most commonly used commands to navigate Linux.

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

There are a number of commands we can use to navigate the Linux file system in the terminal. This instruction set will use some of the commands in the list above and teach you to be more familiar with navigating through your Linux system with the terminal.

---

**1.** Open up your terminal by right-clicking on your desktop and clicking *`Open Terminal`*.

>![Terminal open](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/navigation/directories/term.png?raw=true "terminal")

---

**2.** Input the following command into your terminal to display your current directory.

>**Note**: Linux directories behave similar to folders. In the background, directories are actually a special type of file used to store information about other files. It's contents are controlled by the Linux operating system and it includes things such as name, permission, type, size, and so on.

>```
>pwd
>```

>You should be able to see exactly which directory you are currently in.

>![Screen shot pwd](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/navigation/directories/pwd.png?raw=true "pwd")

---

**3.** Display the contents inside your current directory by inputting the following command.

>![Note icon](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/icons/note.png?raw=true "Note"){: style="float: left" } It is important to know what _path_ you are referencing when issuing a command. The `ls` command implicitly shows the contents, such as files and directories under your current directory.

>```
>ls
>```

>You will be shown everything inside your current directory.

>![Screen shot ls](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/navigation/directories/contents.png?raw=true "ls")

---

**4.** Create a new folder inside your current directory by using the following command.

>```
>mkdir testfolder
>```

>Let's check the contents of our current directory again by inputting the `ls` command once again.

>```
>ls
>```

>You will see that you have successfully created a new folder called *`testfolder`*.

>![Screen shot ls with testfolder](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/navigation/directories/contents2.png?raw=true "ls")

---

**5.** Change into the *`testfolder`* directory with the following command.

>**Note**: The input after `cd` will be the name of the directory you want to change into.

>```
>cd testfolder
>```

>Let's check to see which directory you are now currently in with the `pwd` command.

>```
>pwd
>```

>You will see that you are now inside the newly created *`testfolder`* directory.

>![pwd2](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/navigation/directories/pwd2.png?raw=true "ls")

---

**6.** Change back to the previous directory with the following command.

>**Note**: By adding `../`, you can jump back up one parent directory.

>```
>cd ../
>```

>You will see you have returned back to the previous directory that you were in.

>![Screen shot pwd](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/navigation/directories/pwd.png?raw=true "pwd")

---

## Conclusion

By reaching the end of this instruction set, you have learned how to open the terminal and input commands which allowed you to navigate through your system. 

You are now able to know exactly what files are contained in your directories as well as your current directory, allowing you to easily navigate through your system.
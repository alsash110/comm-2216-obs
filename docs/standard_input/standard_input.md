---
layout: default
title: Standard Input
nav_order: 7
has_children: true
permalink: /docs/standard_input
---

{: .fs-6 .fw-300 }

# Standard Input

---

Terminal and terminal emulators are software a user interfaces with to issue commands to the shell. The shell then parses the commands and sends it to the kernel.

The terminal reads and writes information as streams. The input stream is called _standard input_ (stdin) and the output stream is called _standard output_ (stdout). There is also something called _standard error_ (stderr) which is thrown when a problem occurs.

These streams can be redirected to other processes but the default is the terminal. This is why after you issue a command you can see the output displayed on the terminal.

A simplified explanation is the standard output from a command can be ‘piped’ as the standard input of another process. This can be chained an unlimited number of times but the final output will be either your terminal or a file.

---

### Table of contents
{: .no_toc .text-delta }
* TOC
{:toc}

---


## The `>` Operator

The `>` operator takes the _stdout_ from  `ls -la`  and writes it to a newly created file called `list.txt` in your current directory.
The `>` command is formatted as `command > filename`

>> *`ls -la > list.txt`*  >-->  **[Enter]**

![Screen shot of ls -la > list.txt](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/standard_input/stdout_1.png?raw=true ">")

We can see that the contents of the file is exactly the same as the terminal output of  ls -la. An interesting note is that the contents of list.txt actually contains the file list.txt itself.

---

## The `>>` Operator

The `>>` operator _appends_ the stdout to an existing file while the `>` always creates (overwrites) a file.

>> *`pwd >> list.txt`*  >-->  **[Enter]**

![Screen shot of pwd >> list.txt](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/standard_input/stdout_2.png?raw=true ">>")

If you reopen the file, the stdout of `pwd` is appended to the end of the file.

---

## The `|` Operator

The `|` is another operator that takes Standard Output from the left side and ‘pipes’ it as the Standard Input to the right side.

>> *`ls /etc | less`*  >-->  **[Enter]**

Piping something to `less` is rather pointless but it serves as a demonstration of how to use `|` to _pipe_ the stdout from one command to the stdin of another.

![Screen shot of ls /etc `|` less](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/standard_input/stdout_3.png?raw=true "`|`")

To exit, press **[q]**.

We can redirect _stdin_ as well with the `<` operator.

If you haven’t deleted the file `list.txt` or _changed directories_, if you run:

>> *`wc < list.txt`*  >-->  **[Enter]**

![Screen shot of wc < list.txt](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/standard_input/stdin_1.png?raw=true "<")

You will get a word count of the list.txt file.

The  `<`  operator is the same as the  `>`  operator but reversed.
It _redirects_ the _stdout_ form the _right side_ as the _stdin_ on the _left_.

---

Note, the  `|`  operator is one direction and is always from left to right.

---

## Another Example of `|` Operator

I have a file text file named `rockyou.txt`. It contains a list of the most common passwords used online.

![Screen shot of less rockyou.txt](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/standard_input/stdin_2.png?raw=true "rockyou.txt")

I can search the list to see if my password is on the list by using this command.

>> *`cat rockyou.txt | grep aaabbbcccddd`*  >-->  **[Enter]**

The command is formatted as `command  |  command`

![Screen shot of cat rockyou.txt `|` grep aaabbbcccddd](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/standard_input/stdin_3.png?raw=true "`|`")

Yes, *`aaabbbcccddd`* is in it and so it is a terrible password.

---

One important consideration when using the `|` operator is the command used on the _left_ side must output a  _stdout_. Likewise, the command on the _right_ side must be able to accept a _stdin_.

It makes no sense to pipe something to a command if the command does not take a stdin, and vice versa.

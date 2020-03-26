---
layout: default
title: Standard IO
nav_order: 7
has_children: false
permalink: /docs/standard_io
---

# Standard IO
{: .no_toc }

---

Terminal and terminal emulators are software a user interfaces with to issue commands to the shell. The shell then parses the commands and sends the commands to the kernel.

The terminal reads and writes information as streams. The input stream is _standard input_ (stdin) and the output stream is _standard output_ (stdout). There is also a _standard error_ (stderr) which is thrown when a problem occurs.

These streams redirect to other processes but the default is the terminal. This is why after you issue a command you can see the output displayed on the terminal.

A simplified explanation is the standard output from a command can be ‘piped’ as the standard input of another process. Pipes can chain an unlimited number of times but the final output will be either your terminal or a file.

---

### Table of contents
{: .no_toc .text-delta }
* TOC
{:toc}

---

## File Descriptor

A _File Descriptor_ is non negative a number used to represent stdin, stdout, and stderr associated with open files. This is how the operating system identifies and keeps track of inputs and outputs to files.

This guide does not go in to further details on this topic but shows you the base concept.

| type   | file descriptor |
| :----- | :-------------- |
| stdin  | 0               |
| stdout | 1               |
| stderr | 2               |

---

## Using Standard IO

You will be guided through this instruction set to make use of stdin and stdout. At the end of the set, you will have a deeper understanding of how these processes work.

---

### The `>` Operator

The `>` operator takes the _stdout_ from  `ls -la`  and writes to a new file called `mylist.txt` in your current directory.

The `>` command format is `command > filename`.

**1.**: Input the following command into your terminal to show the contents of the current directory.

>```
>ls -la
>```
<br />
<br />

>![Note icon](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/icons/note.png?raw=true "Note"){: style="float: left" }
>> **Note**: The results you get may not be exactly the same as the results shown in the screen shot below. Your current directory will most likely contain different files and directories.

>![contents](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/standard_input/std1.png?raw=true ">")
<br />
<br />

**2.** Input the following in a terminal to test out the `>` operator.

>This command will write the contents of your directory to a text file that you name *`mylist.txt`*.

>```
>ls -la > mylist.txt
>```
<br />

>Look at the contents of *`list.txt`* with the following command.

>```
>cat mylist.txt
>```

>You will see that the contents inside *`mylist.txt`* are identical to the output of the *`ls -la`* command.

> **Contents of the *`mylist.txt`* file.**
>![contents](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/standard_input/std2.png?raw=true ">")
>Input the *`ls -la`* command to see the contents of your current directory. 

> **Output from the *`ls -la`* command**
>![contents](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/standard_input/std1.png?raw=true ">")


>An interesting note is that the contents of *`mylist.txt`* actually contains the text `mylist.txt` itself.
<br />
<br />

### The `>>` Operator

The `>>` operator _appends_ the stdout to a file while the `>` always overwrites a file.

**3.** Input the following command to append a new line to `list.txt` with the `>>` operator:

>```
>pwd >> list.txt
>```
<br />

>Reopen the file to see that the stdout of `pwd` is appended to the end of the file.

>```
>cat mylist.txt
>```

> You will see that your current working directory has been appended to the bottom of *`mylist.txt`*.

>![Screen shot of pwd >> list.txt](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/standard_input/std3.png?raw=true ">>")
<br />
<br />

### The `|` Operator

The `|` is another operator that takes standard output from the left side and ‘pipes’ the left as the standard input to the right side.


>![Note icon](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/icons/note.png?raw=true "Note"){: style="float: left" }
>> **Note**: The  `|`  operator is strictly single directional and always 'pipes' from left to right.
<br />

The command is formatted as `command  |  command`

**4.** Input the following command to test the 'pipe' operator:

>```
>ls /etc | less
>```

>Piping something to `less` is rather pointless but serves as a demonstration of how to use `|` to _pipe_ the stdout from one command to the stdin of another.

>![Screen shot of ls /etc `|` less](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/standard_input/stdout_3.png?raw=true "`|`")

>Press **[q]** to exit.
<br />
<br />

### The `<` Operator

We can redirect _stdin_ as well with the `<` operator.

>The  `<`  operator is the same as the  `>`  operator but reversed.
>The `<` operator _redirects_ the _stdout_ from the _right side_ as the _stdin_ on the _left_.

**4.** Execute the following command to see the word count of the *`mylist.txt`* file.

>```
>wc < list.txt
>```
You can see a word count of the *`mylist.txt`* file.

>![Screen shot of wc < list.txt](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/standard_input/std4.png?raw=true "<")
<br />
<br />

### Hypothetical Use Cases for the `|` Operator

>![Note icon](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/icons/note.png?raw=true "Note"){: style="float: left" }
>> **Note**: I have a text file named *`rockyou.txt`* that contains a massive list of the most common passwords used online. If you wish to follow along with this part of the guide, [click here](https://www.kaggle.com/wjburns/common-password-list-rockyoutxt) to download the file. 

**1.** Open the file to what the first few lines looks like.

>![Screen shot of less rockyou.txt](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/standard_input/stdin_2.png?raw=true "rockyou.txt")

**2.** Search through the document to see if your password is on the list by using the `grep` command in the terminal.

>![Note icon](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/icons/note.png?raw=true "Note"){: style="float: left" }
>> **Note**: The `grep` command returns all matching results if the file is found.
<br />
<br />

>```
>cat rockyou.txt | grep aaabbbcccddd
>```

>You will receive an output which shows you that *`aaabbbcccddd`* is in the list of common passwords and you should not use it.

>![Screen shot of cat rockyou.txt `|` grep aaabbbcccddd](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/standard_input/stdin_3.png?raw=true "`|`")

>An important consideration when you use the `|` operator is that the command used on the _left_ side must output a _stdout_. Likewise, the command on the _right_ side must be able to accept a _stdin_.

>Piping makes no sense if you pipe something to a command when the command does not take a stdin, and vice versa.
<br />
<br />

You now have a better understanding of how Linux handles user input and output in the _terminal_.

Pipe (*`|`*) and redirect (*`>`*, *`>>`*, *`<`*) operators add a lot more functionality to commands and allows for _command chaining_. _Command chaining_ becomes a very powerful tool by giving you more power and flexibility to your commands.

This is the the last and final instruction set in our guide. We thank you for going through the complete guide and hope you leave with some new valuable knowledge.

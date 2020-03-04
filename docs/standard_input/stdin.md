---
layout: default
title: Concept of Standard Input
parent: Standard Input
nav_order: 1
---

{: .fs-6 .fw-300 }
## Understanding and using standard output


The Terminal and terminal emulators are the software a user interfaces with to issue commands to the shell. The shell then parses the commands and sends it to the kernel.

The Terminal reads and writes information as streams. The input stream is called _Standard Input_ (stdin) and the output stream is called _Standard Output_ (stdout). There is also something called _Standard Error_ (stderr) which is thrown when a problem occurs.

These streams can be redirected to other processes (programs) but the default is the Terminal. This is why after you issue a command you can see the result (output) displayed on the Terminal.

A simplified explanation is the Standard Output from a command can be ‘piped’ as the Standard Input of another process. This can be chained indefinitely but the final output will be either your terminal or a file.


### The ` > ` Operator

The `>` operator takes the _stdout_ from  `ls -la`  and writes it to a newly created file called `list.txt` in your current directory.
The `>` command is formatted as `command > filename`

>> `ls -la > list.txt`  >-->  **[Enter]**

![Screen shot of ls -la > list.txt](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/standard_input/stdin_1.png?raw=true ">")

We can see that the contents of the file is exactly the same as the terminal output of  ls -la. An interesting note is that the contents of list.txt actually contains the file list.txt itself.


### The ` >> ` Operator
The `>>` operator _appends_ the stdout to an existing file while the `>` always creates (overwrites) a file.




The `|` is another operator that takes Standard Output from the left side and ‘pipes’ it as the Standard Input to the right side.

>> `ls /etc | less`  >-->  [Enter]


Piping something to  less  is kinda pointless but serves as a demonstration to use  |  to redirect the output of one command to another command.

We can redirect stdin as well with the  <  operator.

If you haven’t deleted the list.txt or changed directories, if you run:

>> `wc < list.txt`  >-->  [Enter]


You will get a word count of the list.txt file. 

The  <  operator is the same as the  >  operator but reversed.
It redirects the stdout form the right side as the stdin on the left.

Note, the  |  operator is one director and is always left to right.


An example of the  |  operator in action

I have a file text file named rockyou.txt. It contains a list of the most common passwords used online. I can search the list to see if my password is on the list by using this command.

> `cat rockyou.txt | grep aaabbbcccddd`

The command is formatted as `command  |  command`
Here's the result:

Yes aaabbbcccddd is in it and so it is a terrible password.

One consideration when using the | operator is the command used must use stdin or stdout. It makes no sense to pipe something to a command if the command does not take a stdin, and vice versa.

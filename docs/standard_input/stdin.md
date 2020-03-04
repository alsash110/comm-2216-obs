---
layout: default
title: Using stdin
parent: Standard Input
nav_order: 2
---

{: .fs-6 .fw-300 }

## Using Standard Input
{: .no_toc }

---

### Table of Contents
{: .no_toc .text-delta }
* TOC
{:toc}

---

### The `<` Operator

We can redirect _stdin_ as well with the `<` operator.

If you haven’t deleted the file `list.txt` or _changed directories_, if you run:

>> `wc < list.txt`  >-->  **[Enter]**

![Screen shot of wc < list.txt](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/standard_input/stdin_1.png?raw=true "<")

You will get a word count of the list.txt file. 

The  `<`  operator is the same as the  `>`  operator but reversed.
It _redirects_ the _stdout_ form the _right side_ as the _stdin_ on the _left_.

---

Note, the  `|`  operator is one direction and is always from left to right.

---

### Another Example of `|` Operator

I have a file text file named `rockyou.txt`. It contains a list of the most common passwords used online.

![Screen shot of less rockyou.txt](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/standard_input/stdin_2.png?raw=true "rockyou.txt")


I can search the list to see if my password is on the list by using this command.

>> `cat rockyou.txt | grep aaabbbcccddd`  >-->  **[Enter]**

The command is formatted as `command  |  command`

![Screen shot of cat rockyou.txt `|` grep aaabbbcccddd](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/standard_input/stdin_3.png?raw=true "|")

Yes aaabbbcccddd is in it and so it is a terrible password.

---

One important consideration when using the `|` operator is the command used on the _left_ side must output a  _stdout_. Likewise, the command on the _right_ side must be able to accept a _stdin_.

It makes no sense to pipe something to a command if the command does not take a stdin, and vice versa.

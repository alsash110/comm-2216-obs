---
layout: default
title: Using stdout
parent: Standard Input
nav_order: 1
---

{: .fs-6 .fw-300 }

## Using Standard Output
{: .no_toc }

---

### Table of Contents
{: .no_toc .text-delta }
* TOC
{:toc}

---

### The `>` Operator

The `>` operator takes the _stdout_ from  `ls -la`  and writes it to a newly created file called `list.txt` in your current directory.
The `>` command is formatted as `command > filename`

>> *`ls -la > list.txt`*  >-->  **[Enter]**

![Screen shot of ls -la > list.txt](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/standard_input/stdout_1.png?raw=true ">")

We can see that the contents of the file is exactly the same as the terminal output of  ls -la. An interesting note is that the contents of list.txt actually contains the file list.txt itself.

---

### The `>>` Operator

The `>>` operator _appends_ the stdout to an existing file while the `>` always creates (overwrites) a file.

>> *`pwd >> list.txt`*  >-->  **[Enter]**

![Screen shot of pwd >> list.txt](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/standard_input/stdout_2.png?raw=true ">>")

If you reopen the file, the stdout of `pwd` is appended to the end of the file.

---

### The `|` Operator

The `|` is another operator that takes Standard Output from the left side and ‘pipes’ it as the Standard Input to the right side.

>> *`ls /etc | less`*  >-->  **[Enter]**

Piping something to `less` is rather pointless but it serves as a demonstration of how to use `|` to _pipe_ the stdout from one command to the stdin of another.

![Screen shot of ls /etc `|` less](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/standard_input/stdout_3.png?raw=true "`|`")

To exit, press **[q]**.
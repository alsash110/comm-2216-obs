---
layout: default
title: File CRUD Operations
nav_order: 5
has_children: true
permalink: /docs/files
---

{: .fs-6 .fw-300 }

# File CRUD Operations
{: .no_toc }

---

### Table of contents
{: .no_toc .text-delta }
* TOC
{:toc}

---

## What is CRUD

If you are in the technical field, often times you will need to create new files to work with. By being familiar with how to create and manipulate files in the terminal, you may save yourself a bit of hassle and time. 

_CRUD_ is an acronym that stands for create, read, update, and delete. These are the most basic actions that can be performed on files.

---

## CRUD Instructions

This instruction set will go over Linux commands that allows you to perform _CRUD_ actions directly in the terminal. You will be using the `touch` command to create new files, the `cat` command to read and update files, and the `rm` command to delete unwanted files.

 You will also learn how to copy and move files using the `mv` command.

---

**1.** Input the following command into your terminal to create a new file.

>```
>touch test.txt
>```
<br />

>Test if the *`test.txt`* file was actually created by listing the contents of our current directory with the following command.

>```
>ls
>```
<br />

>You should be able to see that the file named *`test.txt`* exists inside your current directory.

>![Root user](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/files/rootuser.png?raw=true "Root user")
<br />

**2.** Enter the following command to read the contents of our file.

>```
>cat test.txt
>```

>You will notice that nothing happened. That's because nothing has been input into the *`test.txt`* file!
<br />

**3.** Insert some text into your newly created file using the following command.
<br />

>![Note icon](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/icons/note.png?raw=true "Note"){: style="float: left" }
>>Ensure that *`>`* is added to the command this time to be able to insert text into the file.
<br />

>```
>cat > test.txt
>```
<br />

>You will be prompted with an empty space to insert some text. Enter in some text of your choice and hit return. I chose to enter the following text.

>```
>I am a test line in my test file
>```
<br />

**4.** Enter the `cat` command once again to check the contents.

>```
>cat test.txt
>```
<br />

>You will see that we did indeed modify the contents of the *`test.txt`* file.

>![Inserted text into test.txt](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/files/insert-text.png?raw=true "test.txt has contents")
<br />

**5.** Input the following command to rename our *`test.txt`* file into *`newname.txt`*.
<br />

>![Note icon](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/icons/note.png?raw=true "Note"){: style="float: left" }
>>When using the `mv` command to rename a file, enter the current file and then the new name.
<br />

>```
>mv test.txt newname.txt
>```
<br />

>Check your current directory again to see that the file name has been changed.

>```
>ls
>```
<br />

>You will notice that *`test.txt`* does not exist and has been renamed to *`newname.txt`*.

>![Renamed .txt file](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/files/renamed.png?raw=true "Renamed .txt file.")
<br />

**6.** Move your *`newname.txt`* file to a different directory with the following commands.
<br />

>![Note icon](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/icons/note.png?raw=true "Note"){: style="float: left" }
>>Use the `mkdir` command to create a new directory. You may notice that the `mv` command is used here again but this time the command is used to move a file into a different directory by entering the file name and then the directory name.
<br />

>Create a new directory first before moving the *`newname.txt`* file.

>```
>mkdir myfolder
>```
<br />

> Move *`newname.txt`* inside the new directory *`myfolder`*.

>```
>mv newname.txt myfolder
>```
<br />

>Check the contents of the directory *`myfolder`* that you just created.

>```
>ls myfolder
>```
<br />

>You should notice that *`newname.txt`* did indeed move inside of the *`myfolder`* directory.

>![Moved .txt file](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/files/moved.png?raw=true "Moved .txt file.")
<br />

**7.** Remove the *`newname.txt`* file and the *`myfolder`* directory using the `rm` command.
<br />

>![Caution icon](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/icons/caution.png?raw=true "Caution"){: style="float: left" } 
>>You need to first delete the contents before being able to delete the directory.
<br />
<br />

>Remove *`newname.txt`* from the *`myfolder`* directory by stating the directory and the file you want to remove with the following command.

>```
>rm myfolder/newname.txt
>```
<br />

>Remove the *`myfolder`* directory completely with the following command.

>```
>rmdir myfolder
>```
<br />

You will see that you have completely removed both the directory and its contents using the `ls` command. You should no longer see both the created .txt file and directory.

As you've noticed by now, you were able to do these things without the use of your mouse or a graphical user interface. You should be able to easily use these commands for your own future use in Linux when the need to create new file types and directories arise.

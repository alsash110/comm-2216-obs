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

This instruction set will go over Linux commands that allows you to perform CRUD actions directly in the terminal. You will be using the `touch` command to create new files, the `cat` command to read and update files, and the `rm` command to delete unwanted files.

 You will also learn how to copy and move files using the `mv` command.

---

**1.** Input the following command into your terminal to create a new file.

>```
>touch test.txt
>```


**2.** Enter the following command to test if you have a created a file called *`test.txt`*.

>```
>ls
>```

>You should be able to see that the file named *`test.txt`* exists inside your current directory.

>![Root user](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/files/rootuser.png?raw=true "Root user")


**3.** Enter the following command to read the contents of our file.

>```
>cat test.txt
>```

>You will notice that nothing happened. That's because nothing has been input into the *`test.txt`* file!


**4.** Insert some text into your newly created file using the following command.

>![Note icon](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/icons/note.png?raw=true "Note"){: style="float: left" } Ensure that *`>`* is added to the command this time to be able to insert text into the file.

>```
>cat > test.txt
>```

>You will be prompted with an empty space to insert some text.

>Enter in some text of your choice and hit return. I chose to enter the following text.

>```
>I am a test line in my test file
>```


**5.** Enter the `cat` command once again to check the contents.

>```
>cat test.txt
>```

>You will see that we did indeed modify the contents of the *`test.txt`* file.

>![Inserted text into test.txt](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/files/insert-text.png?raw=true "test.txt has contents")


**6.** Input the following command to rename our *`test.txt`* file into *`newname.txt`*.

>**Note**: When using the `mv` command to rename a file, enter the current file and then the new name.

>```
>mv test.txt newname.txt
>```


**7.** Check your current directory again to see that the file name has been changed.

>```
>ls
>```

>You will notice that *`test.txt`* does not exist and has been renamed to *`newname.txt`*.

>![Renamed .txt file](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/files/renamed.png?raw=true "Renamed .txt file.")


**8.** Move your *`newname.txt`* file to a different directory with the following commands.

>**Note**: Use the `mkdir` command to create a new directory. You may notice that the `mv` command is used here again but this time the command is used to move a file into a different directory by entering the file name and then the directory name.

>```
>mkdir myfolder
>```

>```
>mv newname.txt myfolder
>```


**9.** Check the contents of the directory *`myfolder`* that you just created.

>```
>ls myfolder
>```

>You should notice that *`newname.txt`* did indeed move inside of the *`myfolder`* directory.

>![Moved .txt file](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/files/moved.png?raw=true "Moved .txt file.")


**10.** Remove the *`newname.txt`* file and the *`myfolder`* directory using the `rm` command.

>**Note**: You may use the `rm` command to delete a file and `rmdir` to delete a directory. You need to first delete the contents before being able to delete the directory.

>```
>rm newname.txt
>```

>```
>rmdir myfolder
>```

>You will see that you have removed the directory and the contents.

---

### Conclusion

By reaching the end of this set of instructions, you have successfully created, read, modified, moved, and deleted files using the terminal. You will no longer see both the created .txt file and folder.

As you've noticed by now, you were able to do these things without the use of your mouse or a graphical user interface. You should be able to easily use these commands for your own future use in Linux when the need to create new file types and directories arise.

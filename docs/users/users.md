---
layout: default
title: Users, Groups, and Privileges
nav_order: 4
has_children: false
permalink: /docs/users
---

# User Accounts on Linux
{: .no_toc }

---

There are two types of user accounts in Linux, regular users and the _root user_.

Linux operating system supports _one root user_ (User Id 0) with additional users created following the initial setup. Linux can support up to 4294967296 users, each with their own home directory and permissions. By default, one user can not access another users files, unless they are the root user. These permissions can be altered through _user permissions_, _group permissions_, as well as _file permissions_.

The _root user_ has full privileges over the system so care must be taken when you are doing anything with the root user account.

This section goes over how to create a new user and assigning certain privileges to those users.

You are going to learn the `adduser`, `moduser`, and some `sudo` commands.

---

## Creating New Users and Assigning Groups

This instruction set shows you how to:
- add new users,
- assign privilege groups, and
- switch between different user accounts in your Linux system.

---

**1.** Switch to the root user by entering the following command into your terminal.

>![Note icon](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/icons/note.png?raw=true "Note")
{: style="float: left" } 
>> **Note**: Ensure that you enter the command below correctly before proceeding or you will not be able to successfully complete the other steps. You will also be prompted to enter your password.
<br />
<br />

>```
>sudo su -
>```

>Enter your current users password if prompted.

>![Root password](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/users/pass.png?raw=true "root password")

>If entered correctly, the bottom left of your terminal will display root as your user.

>![Screen shot of root user](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/users/rootuser.png?raw=true "Image of user on root account")
<br />
<br />

**2.** Enter the `adduser` command below to add a new user to your Linux system.

>![Note icon](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/icons/note.png?raw=true "Note"){: style="float: left" } 
>> **Note**: Replace newusername with the user you want to create.
<br />
<br />

>```
>sudo adduser newusername
>```
<br />

**3.** Set and confirm a password for the new user.

>![setpassword user](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/users/create1.png?raw=true "password set for new user")

>The terminal will show the following message once you input a password.

>![password success](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/users/create2.png?raw=true "Password success")
<br />
<br />

**4.** Follow and enter the prompts to set the new users information. 

>![Note icon](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/icons/note.png?raw=true "Note"){: style="float: left" } 
>> **Note**: You may leave the following fields blank for default values.  
<br />
<br />

>![Set user info](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/users/create3.png?raw=true "set user info")
<br />
<br />

**5.** Enter the `usermod` command with the newly created username to the sudo group.

>```
>usermod -aG sudo newusername
>```
<br />

**6.** Enter the following command to switch to the newly created user account.

>```
>su - newusername
>```
<br />

**7.** Enter the following sudo command to verify that the new user has sudo privileges.

>![Note icon](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/icons/note.png?raw=true "Note"){: style="float: left" } 
>> **Note**: The very first time you run a sudo command in a session, a password prompt will show up. Enter your current users password when prompted.
<br />
<br />

>```
>sudo ls -la /root
>```

>You can see the a list of contents that are normally accessible only by the root user once you assign the new user to the sudo group.

>![Screen shot of root directory](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/users/sudo-ss.png?raw=true "Root directory contents")
<br />
<br />

Once you are able to use the `sudo` command to display the list of contents at the root, the user belongs to the sudo group.

You may also find use for creating multiple new user accounts on your system for testing purposes or to have a clean slate to create or modify files in that account.

Now that you are able to create new users and assign privileges to those users, we recommend that you learn how to [create, modify, and delete files.](https://dl90.github.io/linux-basics/docs/files)

---
layout: default
title: Users, Groups, and Privileges
nav_order: 4
has_children: true
permalink: /docs/users
---

{: .fs-6 .fw-300 }

## Creating New Users Using the Command Line

---
While using Linux you may want to create new user accounts for a number of different reasons.

You may create as many users as you like as well as assigning certain privileges to those users.

This instruction set will introduce you to the *`adduser`*, *`moduser`*, and some *`sudo`* commands.

This instruction set will show you how to:
- able to add new users,
- assign privilege groups, and 
- switch between different user accounts in your Linux system.

---

1. Switch to the root user by entering the following command into your terminal.

    ![Note icon](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/icons/note.png?raw=true "Note") Ensure that you enter the command below correctly before proceeding or you will not be able to successfully complete the other steps. You will also be prompted to enter your password.

    *`sudo su -`*

    If entered correctly, the bottom left of your terminal should display root as your user.

    ![Screen shot of root user](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/users/sudo-ss.png?raw=true "Image of user on root account")


2. Enter the *`adduser`* command below to add a new user to your Linux system. 

    **Note**: Replace newusername with the user you want to create.

    *`sudo adduser newusername`*

    You will be prompted to enter your password for the current user.

    ```
    [sudo] password for currentuser:
    ```


3. Set and confirm a password for the new user.

    ```
    Enter new UNIX password:
    Retype new UNIX password: 
    ```

    Upon successfully creating a new user, the terminal will show the following message.

    ```
    passwd: password updated successfully
    ```


4. Follow and enter the prompts to set the new users information. You may leave the following fields blank for default values.  

    ```
    Enter the new value, or press ENTER for the default
        Full name []:
        Room Number []:
        Work Phone []:
        Home Phone []:
        Other []:
    Is the information correct? [Y/n]
    ```


5. Enter the *`usermod`* command with the newly created username to the sudo group.

    *`usermod -aG sudo newusername`*


6. Enter the following command to switch to the newly created user account.

    *`su - newusername`*


7. Enter the following sudo command to verify that the new user has sudo privileges.

    **Note**: You will be asked for your password the very first time you run a sudo command in a session.

    *`sudo ls -la /root`*

    You should see the a list of contents that are normally accessible only by the root user if you correctly assigned the new user to the sudo group.

    ![Screen shot of root directory](https://github.com/dl90/linux-basics/blob/gh-pages/docs/images/users/sudo-ss.png?raw=true "Root directory contents")


### Conclusion

Creating and modifying users is made extremely convenient through the use of the terminal and a few commands. 

You have successfully created a new user and assigned sudo privileges to that user by reaching the end of this instruction set. 

You may find use for creating multiple new user account son your system for testing purposes or to have a clean slate to create or modify files in that account.
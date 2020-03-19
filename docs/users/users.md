---
layout: default
title: Users, Groups, and Privileges
nav_order: 4
has_children: true
permalink: /docs/users
---

{: .fs-6 .fw-300 }

# Creating a New Sudo User

1. Switch to the root user by entering the following command.

    ```
    sudo su -
    ```


2. Enter the adduser command below to add a new user to your Linux system. 

    > Note: Replace newusername with the user you want to create.

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


5. Enter the usermod command with the newly created username to the sudo group.

    *`usermod -aG sudo newusername`*


6. Enter the following command to switch to the newly created user account.

    *`su - newusername`*


7. Enter the following sudo command to verify that the new user has admin privileges.

    >Note: the /root directory is normally accessible only by the root user and requires sudo privileges.

    *`sudo ls -la /root`*

    You should see the a list of directories if the user has been assigned to the sudo group.

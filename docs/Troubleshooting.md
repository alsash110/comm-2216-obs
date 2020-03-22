---
layout: default
title: Troubleshooting
nav_order: 9
has_children: false
permalink: /docs/troubleshooting
---

# Troubleshooting



| Symptoms | Probable cause | Action |
|----------|----------------|--------|
|Cannot remove a directory| The directory you want to remove is not empty | Verify that the directory using *`ls`* then delete contents using *`rm directory`*|
| Cannot run *`sudo`* command with newly created user| User not on root user when creating and assigning group privilege               | Change to root user with the command *`sudo su -`*|
| Process not showing up when using *`pgrep processname`*        | The process name does not exist | Verify that the correct keyword was used and spelled correctly |
| Cannot see a directory that was created |The *`touch`* command was mistakenly used | Verify that the *`mkdir`* command was used when creating directories
|Cannot modify contents of a file | Tried to modify non-existant file or used wrong command | Verify that *`>`* was included when using the *`cat > filename`* command
|Could not move my file into a different directory|User tried to move file to non-existant directory or to another file| Verify that the directory exists and is not a file with an extension. Correct syntax is *`mv file directory`*
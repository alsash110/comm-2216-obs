---
layout: default
title: Scenes and Sources
nav_order: 4
---

# [](#header-1) Choosing Scenes and Sources
### Table of contents
{: .no_toc .text-delta }
* TOC
{:toc}
---

## [](#header-2)What Are Scenes and Sources?
A **source** is an input from which the recording will take place. OBS allows users to have many different sources of input such as a browser window, a web camera, the whole screen capture and so on.

A **scene** is the preset of sources and their positioning. Switching between scenes allows the user to make different layouts of screen inputs in a single video.

---
## [](#header-2)How to Create a New Scene
1. Find **SCENES** and **SOURCES** tab in the bottom left corner of the main screen.
>![sourcebox](https://github.com/alsash110/comm-2216-obs/blob/gh-pages/assets/images/scenes_sourcebox.JPG?raw=true "source box"){: .d-inline-block	}

2. A scene is created for you by default. Right click on a scene to **Rename** it, or move on to next step.
>![rename](https://github.com/alsash110/comm-2216-obs/blob/gh-pages/assets/images/scenes_renamesource.JPG?raw=true "rename")

3. To add another scene click on the **‘+’** sign of the **SCENES** tab.
>![createscene](https://github.com/alsash110/comm-2216-obs/blob/gh-pages/assets/images/scenes_createscene.JPG?raw=true "createScene")

4. Enter the name of the new scene in the  popped up menu
>![namescene](https://github.com/alsash110/comm-2216-obs/blob/gh-pages/assets/images/scenes_namescene.JPG?raw=true "nameScene")

Now you've created your first scene! The next step is to select which sources you'll be capturing for your stream/recording.


---
## [](#header-2)How to Select Sources
At the bottom of your OBS window you’ll find a box that says **SOURCES**. Click on the **‘+’** to add a new source. (**Note:** Make sure you have selected and configured your audio and video sources before this step)

You’ll be greeted with this menu:


>![choices](https://github.com/alsash110/comm-2216-obs/blob/gh-pages/assets/images/scenes_choices.png?raw=true "choices")

From here you’ll select the **SOURCES** you want to **CAPTURE**. Once you’ve selected the sources, they’ll show up in the sources box. We’ll go over next which sources you will need to start your first recording or stream

If you’re using OBS for streaming video games or recording lectures or tutorials, you’ll likely want to capture some combination of the sources listed below. Outlined below are what each of these capture modules will be recording.

>![sources](https://github.com/alsash110/comm-2216-obs/blob/gh-pages/assets/images/scenes_sources.JPG?raw=true "sources")


### [](#header-3)Selecting the Sources You Need
1. **Video Capture Device** 
  - This source when added will attempt to find a video capture device to record such as a webcam
  - By right clicking the source once added and selecting Properties you can see a number of settings that can be changed with OBS. While you generally don’t need to touch these, you can press Configure Video to find some video properties that can be altered such as sharpness, contrast, brightness, and more. 

2. **Display Capture** 
  - This will record your entire screen, but can be taxing on the computer especially if your FPS and bitrate are set with high values
  - If you have multiple displays, you can select Properties in the Display Capture source where you will find a ‘Display’ dropdown, allowing you to select which display to record

3. **Audio Output Capture** 
  - This will record audio that is outputted to your device such as headphones or speakers, it will be set to your default audio device upon adding 

4. **Audio Input Capture**
  - This source will record your microphone input.

5. **Window Capture** 
  - This is preferable to Display Capture if you are only going to be recording one application or browser window

6. **Game Capture**
  - This mode is similar to window capture in that it only records one window, the window of the game that is open
  - When selected you will be prompted to pick which game to stream (you must have the game already open)
  - Note: some games will not be picked up by the Game Capture scene, in which case you should try Window Capture



---
As you add each source, you’ll see them appear in the sources box. You'll see video sources appear in the OBS preview menu. By clicking on these sources, a red border will appear around it which allows you to resize each video source to your liking. 

Now you're ready to start recording or streaming! But let’s say you’re a high functioning individual who wants to stream yourself both gaming and simultaneously working on an english essay.
 
You can easily do that with the addition of multiple scenes. When you add a scene you’ll be able to select different sources, or you can use it to quickly resize or current sources to fit your needs. Simply click on each scene in OBS to switch between them.

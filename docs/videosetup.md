---
layout: default
title: Video Setup
nav_order: 2
---

# Video Setup
{: .no_toc }


Setting up the video to record is one of the most important aspects of your video recording process. One of the key factors to consider when recording it is the quality of the video.

The main factors that affect the visual quality of a video are _frame rate_ (measured in frames per second) and the _resolution_ (the amount of pixels used to capture/replicate an image on the screen).

One of the many reasons why OBS is so popular is because it allows you to easily control these quality settings. 

### Table of contents
{: .no_toc .text-delta }
* TOC
{:toc}

---
## What is the Video's Frame Rate

Frame rate represents how frequently the image is being changed on the display of your computer. It’s usually measured in frames per second, or FPS. If a video is captured and played back at 60 FPS, that means each second of video shows 60 distinct still images.

Frame rate affects how smooth the video is for the human eye. If a video has an FPS of over 24, that video would look smooth to most people.

![Note Icon](https://github.com/alsash110/comm-2216-obs/blob/gh-pages/assets/images/note-icon.png?raw=true "note tab"){: style="float: left" }
>> **NOTE**: Lowering the framerate beneath 24 FPS may cause your video to become harder to follow, if things frequently move on screen.

## What is the Video's Resolution

Video resolution is a display device that refers to the number of distinct pixels that could be displayed in each dimension. It is usually quoted as width×height ratio. For example, the standard HD resolution has 1280x720 pixels aspect ratio.

The resolution of the video affects the crispness of the image: the higher the resolution is - the more detailed is the image.

![Note Icon](https://github.com/alsash110/comm-2216-obs/blob/gh-pages/assets/images/note-icon.png?raw=true "note tab"){: style="float: left" }
>> **NOTE**: If the input picture's resolution is lower than the resolution of the display, the quality presented will be of the input image. In other words, in most cases, if the input image is poor, it cannot be enhanced by a better display.

## Setting the Video’s Framerate and Resolution

In order to set the frame rate and resolution of the video you want to record, follow the next steps.

---


1) Open SETTINGS from the CONTROLS area in the bottom right of the OBS window

>![Settings open](https://github.com/alsash110/comm-2216-obs/blob/gh-pages/assets/images/vid-1-set.png?raw=true "settings tab")
>![Settings closeup](https://github.com/alsash110/comm-2216-obs/blob/gh-pages/assets/images/vid-1-set1.png?raw=true "settings tab closer")


2) Click on the **VIDEO** tab on the left of the **SETTINGS** window

>![Video open](https://github.com/alsash110/comm-2216-obs/blob/gh-pages/assets/images/vid-2-set.png?raw=true "video tab")

3. Adjust the values of Base Resolution, Output Resolution, and FPS values for optimal performance.

>![FPS Res open](https://github.com/alsash110/comm-2216-obs/blob/gh-pages/assets/images/vid-3-set.png?raw=true "settings tab")

The *Base (Canvas) Resolution* should always be set to the native resolution of your monitor. This setting should already be set to this by default, but it may need to be adjusted if this is not the case.

The *Output (Scaled) Resolution* is the resolution at which the video will be created. It's best to keep this at or above 1280x720, as this resolution is high definition enough to where it's unlikely for any elements on screen to be obscured due to a blurry image.

The lowermost option controls the framerate. It's best to keep this at above 24 FPS if there are many things which will move in the video, to ensure that any visuals are smooth and easy to follow. However, if the video is largely static, such as when recording a presentation, then it's safe to lower this value further.

If you want to record a video of lower quality which takes up less memory on your computer: lower the output resolution and/or framerate.
If you want to record a video of better quality which takes up more memory on your computer: increase the output resolution and/or framerate.

---

You now know how to change the framerate and resolution of your recordings. 

Now you will be able to change them if you want to increase or decrease the video quality to adjust quality to memory ratio.

The next step of recording a great video is setting up the audio.

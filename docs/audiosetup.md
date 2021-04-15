---
layout: default
title: Audio Setup
nav_order: 3
---

# Audio Setup
Correctly setting up the audio is important in ensuring that the video sounds exactly as it should. If you're speaking, but there's background noise which is too loud, the viewer may miss important chunks of information.

### Table of contents
{: .no_toc .text-delta }
* TOC
{:toc}

---
To tinker with the audio, first we'll need to get to the **AUDIO** section of the **SETTINGS**.

1) Navigate to the **SETTINGS** menu from the **CONTROLS** section in the bottom right hand corner of the window.

![Controls panel's settings](https://github.com/alsash110/comm-2216-obs/blob/gh-pages/assets/images/audio-controls-settings.png?raw=true "Control panel's settings button")

2) Move to the **AUDIO** tab.

![Settings' audio tab](https://github.com/alsash110/comm-2216-obs/blob/gh-pages/assets/images/audio-audio-tab.png?raw=true "Settings' audio tab")

---
In the **AUDIO** tab, you'll find many options related to adjusting sounds, but many of these can be ignored. The important area from here, however, is the *Devices* section, pointed out in the image below, with the two main components grouped out.

![Audio devices](https://github.com/alsash110/comm-2216-obs/blob/gh-pages/assets/images/audio-devices-area.png?raw=true "Audio devices")

You'll notice that there are two types of audio here: *Desktop Audio* and *Mic/Auxiliary Audio*.

You can think of the *Desktop Audio* as the output audio, meaning devices which are playing audio from your computer (headphones, speakers, etc.). The *Mic/Auxiliary Audio*, on the other hand, is the input audio. This is any audio that you are providing the computer, like a microphone, and also includes things such as a piano keyboard being plugged in.

By default, both *Desktop Audio* and *Mic/Auxiliary Audio* will be set to *Default*, which means that it will use your computer’s default output and input devices. If your audio is not being recorded properly, you may need to select a different device from the dropdown menu. Below is an image of an example dropdown menu from the “desktop audio” option.

![Audio dropdown menu](https://github.com/alsash110/comm-2216-obs/blob/gh-pages/assets/images/audio-desktop-audio-dropdown.png?raw=true "Audio dropdown menu")

![Note Icon](https://github.com/alsash110/comm-2216-obs/blob/gh-pages/assets/images/note-icon.png?raw=true "note tab"){: style="float: left" }
>>**NOTE**: Input and output devices vary from computer to computer, and as such, your computer will likely have different devices listed.

Both the *Desktop* and *Mic/auxiliary* audio options have multiple dropdown menus, with only the first of each being enabled. These extra dropdown menus are for cases in which, for example, you are using headphones as well as a speaker, or you’re using a microphone while also using a piano keyboard.

If you’re using a single audio input and output, you can safely keep these extra dropdowns on *Disabled*.

---
## Audio Mixer

Audio mixing is the balancing of different audio sources. A basic principle of this is to ensure that your voice is heard over any other noises which may be heard in the video.

The Audio Mixer can be found at the bottom of the main OBS window. Below is a marked up image pointing out the important parts of the Audio Mixer.

![Audio mixer](https://github.com/alsash110/comm-2216-obs/blob/gh-pages/assets/images/audio-audio-mixer.png?raw=true "Audio mixer")

1) These are the sources which you set up in the MICROPHONE AND DESKTOP AUDIO section. In this image, no additional sources were set up, so you may have additional items in this area.

2) This is a volume bar for a given source, and is used to control how loud the sounds from a given source are.

3) This bar, called a Volume Meter, indicates how loud the audio from a source is. When there are two bars directly next to each other, that indicates a stereo audio source, with the top being the left source and the bottom being the right source.

4) The settings icon contains many options for configuring a given source.

### Configuring the Audio Mixer


The primary goal of the audio mixer is to balance the audio shown in the various Volume Meters, to ensure that the most important sounds (like your speaking) are heard over less important sounds (like background music).
The easiest guideline to follow to allow for this is to make sure that the sounds coming from the less important audio sources stay in the green zone of the Volume Meter, while important audio sources stay mostly in the yellow zone, though it’s perfectly alright for it to reach the red zone occasionally.

![Volume meter](https://github.com/alsash110/comm-2216-obs/blob/gh-pages/assets/images/audio-volume-meter.png?raw=true "Volume meter")

An easy way to achieve this effect is by sliding the handle of the volume bar, seen below, to the left or right, until you’ve reached your desired volume levels. Try playing some music and talking while you’re adjusting it.

IMAGE HERE: THE VOLUME BAR WITH A SQUARE AROUND THE HANDLE THING THAT YOU DRAG
![Volume bar](https://github.com/alsash110/comm-2216-obs/blob/gh-pages/assets/images/audio-volume-bar-handle.png?raw=true "Volume bar")

---

The next step of the guide is to [configure scenes and sources](scenessources.md), to make sure that the viewers are seeing exactly what they need to see.

However, if you’re finding that, even with the volume bar all the way to the right, an audio source is still too quiet, please follow the steps below.

---

### Boosting Volume Beyond the Volume Bar


1) Click on the settings icon for the any source (it doesn’t have to be for the source you’re looking to adjust) and select *Advanced Audio Properties*.

![Advanced audio properties](https://github.com/alsash110/comm-2216-obs/blob/gh-pages/assets/images/audio_advanced_audio_properties.png?raw=true "Advanced audio properties")

2) In the *Advanced Audio Properties* window, increase the value under *Volume* for your desired source until it’s at the desired volume level.

![Further increase volume](https://github.com/alsash110/comm-2216-obs/blob/gh-pages/assets/images/audio_advanced_audio_volume.png?raw=true "Further increase volume")

It’s best to adjust this value by no more than 5dB at a time, as more than that may cause it to be too loud. Any adjustments are saved automatically and immediately, so you can monitor the Volume Meter as you’re adjusting the volume here.

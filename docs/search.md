---
layout: default
title: Troubleshooting
nav_order: 8
---

# Troubleshooting
---

These are some of the major issues when operating on OBS, the root causes of those issues and the potential measures to solve them.

## Buffering Issues

Buffering is when data is preloaded into a reserved area of memory called a _buffer_. For streamers, there are three main reasons why you may be experiencing buffering issues, ie. the stream lagging or constantly loading.

To troubleshoot buffering issues in OBS, **first and foremost**, confirm that the stream is experiencing _frame drops_. This is to make sure the issue isn’t with your own connection. To do this, check the counter at the bottom of the OBS Studio main window.

### [](#header-3)To check for frame drops:
  1. Open OBS and look to the bottom right of the primary window
  >![sourcebox](https://github.com/alsash110/comm-2216-obs/blob/gh-pages/assets/images/Dframes.PNG?raw=true "Dframes"){: .d-inline-block}
  2. Monitor this _fps_ value to check if it fluctuates between low and high

If you are not experiencing any dropped frames, the next most likely reason for your buffering issues is _bitrate_: you’ve used too much of it. While a higher bitrate can be an easy way to make your stream look a bit better, if your bitrate is too high, your viewers may have issues with downloading it. If you must raise the bitrate, make sure it is within reason of the internet connection speeds of the countries your viewers may be from.

### [](#header-3)To check/set your bitrate:
  1. navigate from the main OBS window to **File** -> **Settings** -> **Output**

  2. From here find **Streaming**, inside you'll see a value for **Video Bitrate**
  >![sourcebox](https://github.com/alsash110/comm-2216-obs/blob/gh-pages/assets/images/SecuritySteps0.PNG?raw=true "Security Steps 0"){: .d-inline-block}
    - Note: for most computers a bitrate of 2400Kbps is considered a __reasonable__ value.

If your bitrate is set to a reasonable number and you are not experiencing frame drops, then fixing the buffering issues can be more complicated. The third reason for buffer issues are with the _Provider_ (ie. Twitch, Youtube, Instagram) not balancing its streams. For example, Twitch does allow streamers access to all their streaming resources if they are not partnered with Twitch. 

Unfortunately, buffer issues are a tough fix. Unless you’re experiencing dropped frames, the stream is sent out and received at the server of your provider. From there it’s out of your control. The best way to keep the buffer issues away is to use reasonable bitrate values and keep a good internet connection. 

---
## Known Conflicts with 3rd Party Applications

If you are experiencing crashes while using OBS please check the list below and make sure the following apps are either closed or uninstalled:
  - Intel GPA
  - Alienware Respawn
  - Sendori
  - Astrill VPN Proxy
  - Warsaw
  - Adobe Dynamic Link
  - Personify
  - Nahimic Audio

Additinally, certain antivirus software and/or firewalls may interfere with OBS performance, preventing the capture from happening. To fix this issue, make sure to whitelist OBS in your computers settings. 
 
### [](#header-3)Follow these steps to whitelist OBS in your Windows Firewall
  1. In the **Start Menu**, search for **Windows Security**
   >![sourcebox](https://github.com/alsash110/comm-2216-obs/blob/gh-pages/assets/images/SecuritySteps1.png?raw=true "Security Steps 1"){: .d-inline-block}
  2. Once you are in the **Firewall & Network Protection** menu, find **Allow an app through firewall** and click on it
   >![sourcebox](https://github.com/alsash110/comm-2216-obs/blob/gh-pages/assets/images/Whitelist2.PNG?raw=true "Whitelist2"){: .d-inline-block}
  3. In the **Allowed Apps** menu, search for OBS, if found make sure it is checked and then press **OK**. Otherwise, click on **Allow another app**
   >![sourcebox](https://github.com/alsash110/comm-2216-obs/blob/gh-pages/assets/images/Whitelist3.PNG?raw=true "Whitelist3"){: .d-inline-block}  
  4. From the **Add an app** menu, you will go to the **Path** field and select browse
  >![sourcebox](https://github.com/alsash110/comm-2216-obs/blob/gh-pages/assets/images/Whitelist4.PNG?raw=true "Whitelist4"){: .d-inline-block}
  5. Navigate to the folder where you downloaded OBS, and find and select the **.exe** file for OBS. This is usually located in __obs-studio -> bin__. Then press **OK**
  >![sourcebox](https://github.com/alsash110/comm-2216-obs/blob/gh-pages/assets/images/Whitelist5.PNG?raw=true Whitelist5"){: .d-inline-block}
  6. Now we're back to **Add an app** you should see OBS in the **Apps** list. Select **Add*
  >![sourcebox](https://github.com/alsash110/comm-2216-obs/blob/gh-pages/assets/images/Whitelist6.PNG?raw=true "Whitelist6"){: .d-inline-block}
  7. Now you've whitelisted OBS in your firewall.


---
## Game Capture Troubleshooting

If you’re having trouble with game capture, please check to make sure that you’re not experiencing one of the known conflicts OBS has with other apps.

If the issue persists the following resolutions could be useful:

  - Try running OBS as admin. This is a requirement for some games. 
  - If your game is set to full-screen mode and you switch windows from the game, the rendering will stop. 
  - Since OBS has compatibility issues with certain games in full screen mode it is recommended to stream your game on borderless full screen or windowed mode.

---
## GPU Overload Issues

GPU overload is caused by a computer’s graphics card being unable to keep up with the production your system demands. If you are experiencing them, FIRST try running OBS as administrator. This will allow OBS reserve additional GPU capacity for use through the operating system. 
There are a number of ways you can reduce the load on your graphics card. 
**Within OBS**:
  -	Our first recommendation is to build simpler scenes.
      - OBS will drain additional resources from your GPU for all the scenes you have in your current collection.
      - If you are not using all the scenes currently, consider splitting them up into collections, this will allow OBS to use fewer resources while you stream.
  -	Use fewer filters.
    - While filters can be useful for certain scenes, they can be very taxing on your GPU’s resources. Removing a few if not all filters will help with GPU overloading issues. 
**In System**:
  -	Beware of the browser! Browsers like Google Chrome will contribute to your GPU overload issues since it has to render all that text, audio, imagery, and video.
    - Consider using only a few tabs or closing chrome while you stream video games or other resource heavy activities.
  -	Lower the settings of the game you are playing.
    - While this may not be an optimal solution, by lowering the settings in the game this reduces the amount of work your GPU will need to do, in some cases preventing GPU overload.

If you're still having issues with any of the above, please check out the OBS forum or the OBS Discord!


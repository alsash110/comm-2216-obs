---
layout: default
title: Troubleshooting
nav_order: 8
---

# Troubleshooting
{: .no_toc }

---

These are some of the major issues when operating on OBS, roots of the issue and the potential measures to solve the issues

## Buffering Issues

Buffering is when data is preloaded into a reserved area of memory called a _buffer_. For streamers, there are three main reasons why you may be experiencing buffering issues, ie. the stream lagging or constantly loading.

To troubleshoot buffering issues in OBS, **first and foremost**, confirm that the stream is experiencing _frame drops_. This is to make sure the issue isn’t with your own connection. To do this, check the counter at the bottom of the OBS Studio main window.

If you are not experiencing any dropped frames, the next most likely reason for your buffering issues is _bitrate_: you’ve used too much of it. While a higher bitrate can be an easy way to make your stream look a bit better, if your bitrate is too high, your viewers may have issues with downloading it. If you must raise the bitrate, make sure it is within reason of the internet connection speeds of the countries your viewers may be from.

If your bitrate is set to a reasonable number and you are not experiencing frame drops, then fixing the buffering issues can be more complicated. The third reason for buffer issues are with the _Provider_ (ie. Twitch, Youtube, Instagram) not having or not balancing its streams. For example, Twitch does not fully use its CDN unless the streamer is partnered. Viewers of non-partnered streamers may experience issues if the route between them and the provider is too long or overloaded. 

Unfortunately, buffer issues are a tough fix. Unless you’re experiencing dropped frames, the stream is sent out and received at the server of your provider. From there it’s out of your control. The best way to keep the buffer issues away is to use reasonable bitrate values and not drop frames via poor connection. 

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


## Game Capture Troubleshooting

If you’re having trouble with game capture, please check to make sure that you’re not experiencing one of the known conflicts OBS has with other apps.

If the issue persists the following resolutions could be useful:

  - Try running OBS as admin. This is a requirement for some games. 
  - If your game is set to full-screen mode and you switch windows from the game, the rendering will stop. 
  - Since OBS has compatibility issues with certain games in full screen mode it is recommended to stream your game on borderless full screen or windowed mode

## GPU Overload Issues

GPU overload is caused by a computer’s graphics card being unable to keep up with the production your system demands. If you are experiencing them, FIRST try running OBS as administrator. This will allow OBS reserve additional GPU capacity for use through the operating system. 
There are a number of ways you can reduce the load on your graphics card. 
**Within OBS**:
  -	Our first recommendation is to build simpler scenes.
      - OBS will drain additional resources from your GPU for all the scenes you have in your current collection
      - If you are not using all the scenes currently, consider splitting them up into collections, this will allow OBS to use fewer resources while you stream
  -	Use fewer filters
    -While filters can be useful for certain scenes, they can be very taxing on your GPU’s resources. Removing a few if not all filters will help with GPU overloading issues. 
**In System**:
  -	Beware of the browser! Browsers like Google Chrome will contribute to your GPU overload issues since it has to render all that text, audio, imagery, and video.
    - Consider using only a few tabs or closing chrome while you stream video games or other resource heavy activities
  -	Lower the settings of the game you are playing
    - While this may not be an optimal solution, by lowering the settings in the game this reduces the amount of work your GPU will need to do, in some cases preventing GPU overload

If you're still having issues with any of the above, please check out the OBS forum or the OBS Discord!


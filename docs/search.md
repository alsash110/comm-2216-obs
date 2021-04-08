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

If you are experiencing crashes while using OBS please check the list below to ensure you’re not using one of these following applications:

Alienware Alien Respawn:
_This software is found on Dell Alienware systems. It will crash OBS_

Game Capture Issues
GPU Overload Issues
Disabling Windows 10 Gaming Features
Enabling/Disabling Aero in Windows 7
Known Conflicts
Black Screen/Laptop Performance
MacOS Virtual Camera Compatibility Issues
Performance and Encoding Issues


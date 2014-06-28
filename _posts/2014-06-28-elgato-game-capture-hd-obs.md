---
layout: post
title: How to setup the Elgato Game Capture HD in OBS
description: "How to setup the Elgato Game Capture HD in OBS"
tags: [OBS, Elgato, game capture hd, game,capture, hd]
comments: true
draft: true
---
Welcome to this guide which will show you how to setup your [Elgato Game Capture HD](www.gamecapture.com) in [OBS](www.obsproject.com).  

Before we continue, please make sure you have each of these: 

* Your [Elgato Game Capture HD](www.gamecapture.com) plugged in and setup with your console
* The [Game Capture HD software/drivers](www.gamecapture.com) installed.
* [OBS](www.obsproject.com) 32 bit installed. 

---

###**Step 1: Open OBS 32Bit, and go to the settings.**

<figure>
 <a href="/images/elgato_hd/1.png"><img src="/images/elgato_hd/1.png"></a>
</figure>

---
###**Step 2: General**

* Make a new profile. For the purpose of this tutorial, we'll call it "Game Capture HD", then click "add"  

<figure>
 <a href="/images/elgato_hd/2.png"><img src="/images/elgato_hd/2.png"></a>
</figure>

---
###**Step 3: Encoding**

* Leave the encoder on "X264". 
* Leave both CBR and VBR checked. These are Twitch requirement.
* Run a [speedtest](www.speedtest.net) to find out your approximate upload speed. Now you have some options. Depending on your upload speed, you can do a few things. 

If 75% of your upload speed equates to 3400kbps, (which is the maximum Twitch will take), then you can set your upload speed to that.  

<br>Be warned however that many people cannot watch a stream with that high bit rate. For new streamers, a good balance between quality and watchability is 2000kbps. You will also need to take into consideration your own internet upload speed. If your maximum is 2mbps(2000kbps) then you may want to set your upload to 1500kbps.
 
* For audio encoding, select AAC, set the format to 48kHz and select a bit rate. Remember, audio bit rate will **ADD to the total bit rate** being streamed to Twitch and your viewers. A good balance between quality and bit rate is 96. As for Mono or Stereo, the option is up to you, but we recommend stereo.  

<figure>
 <a href="/images/elgato_hd/3.png"><img src="/images/elgato_hd/3.png"></a>
</figure>

---
###**Step 4: Broadcast settings**

* For mode, choose "Live stream"
* Streaming service is of course Twitch/Justin.tv(don't worry, you will only stream to Twitch)
* Server should be the closest one to you. If you are not sure, we recommend you use [JTVPing](http://www.teamliquid.net/forum/tech-support/326034-jtvping-find-your-best-twitchtv-server) to find the closest one to you. 
* Your Pathkey/Stream key can be found by going to [Twitch](www.twitch.tv) then your dashboard, and then the "Stream key" tab. Hit "show", and copy and paste the full stream key, including any letters, into OBS. **(Note**: Never show your stream key publicly or give it to anyone you don't trust.**)**
* Keep "Auto reconnect" checked. This is useful when there is a sudden disconnect or network error, OBS will automatically try to start up the stream again. 
* You should not need to touch "Minimize network impact". If you do have network issues, ask on the [OBS forums](https://obsproject.com/forum/list/questions-and-help.5/) first. 
* Save to file is a very useful option. What this does is it will save an EXACT copy of your stream to a folder of your choosing. This can be useful for cutting out stream highlights for YouTube later. If you decide to use this feature, the naming of the files is a little weird. If you name the file **%**, then the name of the saved file will be date_time.mp4. If you name the file ""Stream recording", the first time you stream, it will be "Stream recording", and the next time it will be "Stream recording1". Hopefully in [OBS Studio (OBS 2.0)](https://obsproject.com/forum/threads/obs-redux.7736/) there will be a more graceful solution. 
* Hotkeys, who doesn't like hotkeys. If you choose to use hotkeys, make sure they are not close to any keys you use often. You don't want to accidentally start and/or stop your stream. 
* Ignore any warnings OBS is giving you, we will fix them.   

<figure>
 <a href="/images/elgato_hd/4.png"><img src="/images/elgato_hd/4.png"></a>
</figure>

---
###**Step 5: Video**

* Do not touch "Video Adapter". This will be set to your graphics card.
* Base resolution should be set to "Custom" and 1080p. 
* To get a nice looking stream, and reduce OBS's CPU usage, downscaling the stream by 1.50x to 1280x720p is recommended. 
* Set the filter to "Lanczos". 
* Set the FPS to 30, this is a limitation from the Game Capture HD. If the Game Capture HD receives 1080p video from the console, the maximum recording/streaming FPS is 30. 

<figure>
 <a href="/images/elgato_hd/5.png"><img src="/images/elgato_hd/5.png"></a>
</figure>

---
###**Step 6: Audio**

* Desktop audio device will be whatever your computer audio is playing through. In most cases, this will be your headphones. 
* Microphone is pretty self explanatory. Keep it on default to use your default computer mic for OBS. If you have a headset mic and a USB mic like a Blue Yeti connected, you may need to manually select the Blue Yeti. 
* "Show only connected devices" should be checked. This makes sure you don't select anything that isn't actually there, which can cause problems. 
* If you want to use Push-to-talk, that is up to you. 
* We now need to change "Mic time offset". There is about a 1.4-1.5 second delay from what happens on your TV/Monitor to when the Game Capture HD shows it on your computer. For this reason, we need to delay the mic by the same amount of time so that the video and audio is synced. A good offset time to start at is 1500ms. You might need to change this to 1450ms or 1550ms or even higher or lower depending on your experience. There is currently a bug in OBS where the delay from the Game Capture HD increases over time. This may not be resolved in this version of OBS. 

<figure>
 <a href="/images/elgato_hd/6.png"><img src="/images/elgato_hd/6.png"></a>
</figure>

---
###**Step 7: Advanced**

* Multithreaded optimizations: Keep this checked
* Process priority class: Do not change unless issues arise, in which case you should ask on the [OBS forums](https://obsproject.com/forum/) first. 
* Leave all other settings in the **General** box as they are
* X264 preset: Next to bit rate and resolution, changing this settings can effect the quality of your stream a lot, as well as much CPU OBS uses. The slower the preset, the better the video quality, but the more CPU OBS will use. This list can help you determine which preset you can use:  

**Intel:**  

* Dual core Intel i3 23XX or higher: ultrafast/superfast
* Quad core Intel i5 25XX or higher: Veryfast/Faster
* 8-core Intel i7 26XX or higher: Fast/Medium
* 12-core Intel i7 3930k or higher: slow

**AMD:**  

*Due to the low speed/IPC(Instructions per clock) of AMD CPU's, it is generally not recommended to stream with a dual core or lower.*  

* AMD FX series: 
* AMD FX 4100 or higher: Ultrafast/Veryfast
* AMD FX 6100 or higher: Veryfast/Faster
* AMD FX 8320 or higher: Fast/Medium

**NOTE:** Any X264 preset beyond slow will provide for very little image quality gain and exponential CPU usage increase. We do not recommend going above Medium unless you have a monster CPU or extreme over clock.  

* Encoding profile: Set this to main. If you set it to high there will be a marginal video quality increase, but some phones/tablets may not be able to view your stream. 
* Keyframe: Set to 2. This is a Twitch requirement.
* Use CFR: Keep this checked.  

Do **NOT** touch any of the other settings unless you have extensive knowledge of X264, OBS and video encoding, or if you are having issues and have been instructed so on the OBS forums.  

---

###**Step 8: Noise gate**

* This is something you can play around with on your own, but simply, it will mute your microphone when you are not talking. This may be useful for people with a lot of background noise. 

---

###**Step 9: Adding a scene**

* Now that you have configured your settings, we can start setting up the Elgato Game Capture HD in OBS. 
* In the left hand box at the bottom, right click to "Add scene"

<figure>
 <a href="/images/elgato_hd/7.png"><img src="/images/elgato_hd/7.png"></a>
</figure>
---
###**Step 10: Name your scene**

* For the purpose of this tutorial, we will name the scene "Elgato Game Capture HD". 

<figure>
 <a href="/images/elgato_hd/8.png"><img src="/images/elgato_hd/8.png"></a>
</figure>

---
###**Step 11: Global Sources**

* Now lets add your Game Capture HD as a source. 
* Click on "Global Sources"

<figure>
 <a href="/images/elgato_hd/9.png"><img src="/images/elgato_hd/9.png"></a>
</figure>

---
###**Step 12: Add a video device**

* Click on "Add" 
* Click on "Video capture device"

<figure>
 <a href="/images/elgato_hd/10.png"><img src="/images/elgato_hd/10.png"></a>
</figure>

Step 13: Name the Video capture device

* For easy remembering, name the source "Elgato Game Capture HD"

<figure>
 <a href="/images/elgato_hd/11.png"><img src="/images/elgato_hd/11.png"></a>
</figure>

---
###**Step 14: Select the device**

* By default, the Game Capture HD should be selected. If not, go to the drop down menu at the top, and select the Elgato Game Capture HD. 
* Under Audio, in the drop down menu, choose "Use device audio"
* Under Audio, set the device to "Output to stream only"
* Under video, check the box that says "Use buffering" and set the time to 0. 
* Now click ok, and the window should close. 

<figure>
 <a href="/images/elgato_hd/12.png"><img src="/images/elgato_hd/12.png"></a>
</figure>

---

###**Step 15: Add the Game Capture HD in the scene**

* Right click in the box to the right of the scenes box. 
* Click "Add"
* A menu will come up. Go to "Global sources"

<figure>
 <a href="/images/elgato_hd/13.png"><img src="/images/elgato_hd/13.png"></a>
</figure>

---

###**Step 16:** 


* You should see the Elgato Game Capture HD. 
* Click on it, and it will prompt you for a name.

<figure>
 <a href="/images/elgato_hd/14.png"><img src="/images/elgato_hd/14.png"></a>
</figure>

*  Notice the name is already Elgato Game Capture HD. Just click ok

<figure>
 <a href="/images/elgato_hd/15.png"><img src="/images/elgato_hd/15.png"></a>
</figure>

---

###**Step 17: TEST**

* Congratulations, everything should be setup and working now. 
* Click on the "Preview button". 
* The OBS preview window will come up, and you should see this: 

<figure>
 <a href="/images/elgato_hd/16.png"><img src="/images/elgato_hd/16.png"></a>
</figure>

* After a few seconds, you should see your game on screen. You TV may flicker at this time as well. 
* If you do not see your game, you may need to select a different input. To do this, right click on the Game Capture HD source, click on properties. Once you have the device window open, click on "Configure" (**NOTE**: To configure the Game Capture HD device, the preview must be on).
* The Game Capture HD device option panel should come up, allowing you to change settings like resolution(Which feeds to OBS) and input.  


---

###**Step 18: Moar testing!**

* Keep the preview open and running, and play a couple minutes. Keep an eye on OBS. If it shows warnings like "Taking to long to encode", you have to lower the X264 preset. 
* If other errors come up, don't be afraid to ask on the [OBS forums](https://obsproject.com/forum/)
* This is also the time to test your mic volume, add a webcam, add overlays and more.  


---

###**Step 19: Stream**

* Once you have setup the scenes and sources, stop the preview, and click on stream. 
* You are now live on Twitch! happy streaming.  

---

This guide was written by Phil, Community Coordinator at Elgato Gaming. If you require support for your Elgato Game Capture HD please contact [@ElgatoSupport](www.twitter.com/ElgatoSupport) or open a ticket via the [Elgato Help Desk](http://help.elgato.com/customer/portal/emails/new).
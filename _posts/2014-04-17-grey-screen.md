---
layout: post
title: Grey Screen Issue
description: "Got the issue where you can only see a grey screen with the Twitch logo centered in the middle? Well, here's how to fix that issue!"
tags: [twitch,grey,screen,bug,issue,javascript,malware]
comments: true
image:
  feature: gray-feature.png
---

Got the issue where you can only see a grey screen with the Twitch logo centered in the middle? Well, here's how to fix that issue!

<br>The reason(s) you may be getting this issue is due to one of the following;

* Javascript being disabled
* Extension causing javascript errors
* Firewall and / or Security software blocking JS execution
* Malware
* DNS Issues

Let's start with the simple stuff, depending on the browser you're using follow the relevant instructions below:

## Disabled Javascript

### Google Chrome
Go to: Settings > Privacy > Content settings > Javascript  
<br>From here make sure "Allow all sites to run JavaScript" is selected  
<br>Once you're sure, click "Done"  

### Mozilla Firefox
In the URL / Address bar type: about:config and proceed to press enter   
<br>You may see a "warranty" screen, simply click the button saying "I'll be careful, I promise!"  
<br>Once you're in, type "javascript.enabled" into the search bar below the URL bar   
<br>Once you see the "javascript.enabled" preference, make sure the assigned value is "true" and not "false". If it's false simply right click and hit the "toggle option". 

## Extensions
Once you've made sure JavaScript is enabled on your browser and you're still getting the grey screen, its time to check extensions!  
<br>Firstly, lets test something - in your browser open up an incognito window (don't lie, you know what that is) and try loading Twitch. Do you still get the same error?  
<br>If so your problem isn't likely to be an extension (make sure by checking extensions the browser allows to run in incognito mode - if you see no active extensions in incognito move down to the next section).  
<br>If you did manage to load Twitch successfully then your perpetrator is likely an extension, go to your extension listings and make sure to disable all extensions.  
<br>Now try to load Twitch again, if it works you can begin to enable extensions one by one until you find the one that is causing the issue and remove it from your installed extensions.  
<br>**Still not working, lets move onto anti-virus / security software potentially blocking JS from being executed etc**  

## Anti-Virus / Security Software

There's hundreds of anti-virus and security software programs out there so it's practically impossible for me to list every single one with detailed instructions on what to do.  
<br>Simply, you're looking for browser, network or web protection that allows you to configure the level of security the software will attempt to abide by.  
<br>If you can, try to disable any firewall or web protection for a couple of minutes and try loading Twitch, still getting the issue? If not then you're perpetrator is somewhere within those security settings, fiddle around and let us know how you fixed it so we can keep others up to date!  

## Malware

The part we all didn't want to get to; Malware can be very annoying, sophisticated and a general pain in the ass to deal with. However, we have some wonderful tools available to us!  
<br>My advice is to install AdwCleaner and Malwarebytes and scan for any malware / adware or general horribleness lurking on your PC.  
<br>Below are links to said tools, please let us know in the comments if you do manage to find anything so we can keep others up to date!  

* [MalwareBytes - Free Anti-Malware & Internet Security Software](https://www.malwarebytes.org/)
* [[Bleeping Computer] AdwCleaner](http://www.bleepingcomputer.com/download/adwcleaner/)

## DNS Issues

Recently its been noted that DNS issues on the user end may cause an issue reaching the CDN for Twitch. If you already know how to altar your DNS you can simply change to either of the following DNS providers.<br>

##### Google

8.8.8.8
<br>8.8.4.4<br>

##### OpenDNS

208.67.222.222
<br>208.67.220.220

<br>If you're not sure on how to change your DNS settings simply follow guide provided on Twitch's help desk located [here](http://help.twitch.tv/customer/portal/articles/1444294-how-to-switch-your-dns).

## Conclusion

Hopefully you managed to get the problem dealt with using this blog post, if not - keep trying. You may of just missed something simple. Let us know how you get on in the comments.   

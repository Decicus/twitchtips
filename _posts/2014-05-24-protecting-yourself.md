---
layout: post
title: Protecting Yourself Online 
description: "Learn how to protect yourself online from attacks including DDoS and personal attacks."
tags: [twitch,ddos,protect,yourself,online,honeypots,ip,address]
comments: true
---

## Introduction
Many or most of you will of heard of a DDoS attack during your time on the internet, whether it be on Twitch, a news site, reddit etc. DDoS stands for: Distributed Denial of Service. In its basic form it's essentially a group of nodes (computers) sending useless data to your network and causing issues.

<br>Believe it or not there are other users out there that will attempt to attack you with said method in order to generally annoy and harass you. Such attacks can cause your connection to drop (for extended periods or continously dropping ever x seconds depending on the strength of the attack).

## Why are you telling me this?
In some communities DDoS'ing is widely used and we want to help you ensure you protect yourself as best as possible with what resources are available to you.

<br>In theory this guide cannot guarantee you'll be safe from said attacks, but it'll teach you how to prevent them as best as possible. 

## So how do I do this?
So, essentially for someone to attack you or your network they'll need an IP address, think of it like your internet street address - it's unique to you (unless you're using a public accessible WiFi etc).

<br>Now generally, users IP addresses are supposed to be hidden or out of the general public view however there is multiple "exploits" throughout online services that allow others to extract the information they need, some of the popular methods are listed below:

* Peer-to-peer / VOIP (Some Games, Skype etc)
* Dumped Databases / Server Logs
* Honeypots (IP Grabbing websites)

<br>There's also more methods but they're generally not much of an issue in the gaming community etc. For now we'll go over the 3 listed on how they work and how you can best protect yourself.

## Peer-to-peer (P2P) / VOIP
Some services such as Skype are known as VOIP applications, it basically means voice over the internet (IP). Now you may think due to Skype being such a big name you'd be safe - you're not.

<br>Skype has a tendency to allow users to resolve your Skype handle and return an IP address. In the past this was extremely easy to do to anyone since anyone could query any handle and return an IP address - however since then they have added in a feature that disallows direct connections to users not on your Skype friends list. 

<br>Generally this enough for most people if they keep their Skype extremely private. But of course some people like to add anyone and everyone and even with the direct connection blocking enabled users on your friends lists can still resolve your IP address by simply querying it. 

<br>What's the fix to this you may ask? There's no real fix - you simply add an extra line of defense, in this case a HTTP / SOCKS5 proxy (you'll want to prioritize SOCKS5 > HTTP).

<br>**Okay, so how do I setup this proxy?** Firstly you'll want to direct yourself to Skype and click the Tools drop down, from there click Options and head to Advanced > Connection. You should see a screen like what is show below:

<figure>
    <a href="/images/skype_connections.png"><img src="/images/skype_connections.png"></a>
</figure>

<br>Firstly you're going to want to go ahead and enable "Allow direct connections to your contacts only". This will present users outside of your Skype friends lists from querying your IP address.

<br>If you'd like to know how to set up  a proxy for your Skype account or other internet services, simple follow [this guide](http://imgur.com/a/NpFdW) written by [Fire](https://twitter.com/IncendiaryMedia).

<figure>
    <a href="/images/skype_warning.png"><img src="/images/skype_warning.png"></a>
</figure>

<br>If you don't wish to set up a proxy for Skype or other services you use we highly recommend you keep your contacts absolutely limited to people you **know** you can trust. If you add them to your contacts and they have malicious intentions there's no stopping them from resolving your handle if you don't have a proxy set up.

<br>It is also noteworthy you can use a VPN (virtual private network) to mask your actual IP address however VPN's generally mask **all of your traffic** rather than just Skype for example. A lot of VPN services have been banned through other users abusing them.

## Dumped Databases / Server Logs
Unfortunately it happens, there are people out there that will exploit, abuse and hack into services which you may use, there's almost nothing you can do about it - it's just part of the internet in general.

<br>Unfortunately individuals that do decide to follow such activities also release privately held information on a regular basis such as databases and server logs which may contain your account details (username, e-mail, password hash, last used IP address, IP address registered with etc).

<br>This information can and will be abused by individuals that stumble upon it. The best ways to combat this are listed below:

* If you can help it, never use the same username or alias on multiple websites that aren't related to your online streaming persona.
* Use different passwords for every website, **never** use the same password for multiple websites - if it's compromised via one website, it's compromised for the rest you use.
* Invest into a VPN or proxy service, this way websites you use will never actually see your real IP address therefore if they're compromised you aren't exposed.

<br>Other than the tips stated above, there's not much else you can do - be careful what information you share and who you share it with. Knowledge is power and people will abuse that if they can.

## Honeypots (IP Grabbing websites)
Honeypots in their purest form are websites, servers and services used to bait users into using them and then recording what they do, their information etc.

<br>Essentially Honeypots are entities which you don't want to be on the wrong side of. Their sole intention is information gathering.

<br>Why is this important to me you may ask? Well, unfortunately again there are users out there that will set up such services and attempt to bait you into clicking / using them such as IP grabbing websites, phishing websites and just general malicious services.

<br>If someone you don't know (or in some cases do know) asks you to visit a website, connect to a server that you don't recognize, think twice. What they're sending you could be a trap, do some research beforehand if you're curious but again, be careful.

<br>I'm not trying to suggest you be 100% paranoid about anything and everything people send you, but think twice before following through. It only takes one mistakes for them to cause you a tonne of grief.

## Conclusion
The Internet can be a scary place and as a streamer you may be targeted for whatever reason is humanly possible to comprehend. Yes, it sucks and it's unfortunate - but don't get too down on it.

<br>Stay safe online, protect yourself and if you're having problems with someone harassing you on Twitch send a report of them [following this method](http://help.twitch.tv/customer/portal/articles/725568-how-to-file-a-report).

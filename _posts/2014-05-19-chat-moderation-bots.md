---
layout: post
title: Chat moderation bots
description: "Learn how to chose between and use various twitch moderation bots."
tags: [twitch,chat,bots,xanbot,moobot,nightbot]
comments: true
---
## 1. Bots - what are they?
While having moderators in chat is nice, they are, in fact, human.   
They make mistakes, have a reaction time that massively exceeds the time a computer takes to react to messages written in chat and occasionally need some sleep.  
<br>
For this reason, so called “Chat moderation robots” or simply “bots” have been created by third party developers.  
<br>
These can perform basic moderation tasks, such as timing out users automatically if they use offensive words in chat, as well as custom chat commands, which make the bot respond with information if a command is posted in chat.

<figure>
    <a href="/images/bot_guide/image1.png"><img src="/images/bot_guide/image1.png"></a>
    	<figcaption>Example of a built-in command to create a custom command.</figcaption>
</figure>

## 2. When and why should I get a bot?
For very small channels, with low amount of viewers, a bot is not necessary.   
Having a bot in a channel that is live once a week and averages 3 viewers just wastes resources on the bot- and chat servers.  
<br>
If you do not have a lot of viewers, you will probably not be in the need of a bot – consider expanding your viewership and getting a bot when it becomes a necessity, for example, if spammers keep posing a problem, or people keep asking the same questions over and over, that is a definite sign you want a bot.  
<br>
Be careful with repeated commands however, if you are in a channel with 5 viewers and a bot keeps posting social media info every 2 minutes, that just gets obnoxious as time passes on.

## 3. What bots are there? Which should I choose?
These questions are important to answer, yet impossible to answer completely.  
There is a wide range of bots and reasons why you want a bot.  
<br>
To address the first question, I will try to give an overview over the 3 most commonly used bots:  

* Xanbot, developed by Aaron ‘Xangold’ Clay, who is Twitch Staff as well
* Moobot, developed by Moocat, a Twitch Admin
* Nightbot, developed by the NightDev team, the makers of BetterTTV

These bots are all similar, yet optimized for different use cases.   
Every channel can use each of the bots, but properly deciding which bot to use can make your life on Twitch a lot easier.  

### The Basics
While this does not hold true for every bot, most bots (including these three bots) can be controlled with commands that are posted in chat. 
These commands usually take the form of
{% highlight html %}
!<commandname> <parameters>
{% endhighlight %}
  
For any bot, there are predefined commands, which allow you to make changes to commands and other settings the bot might provide.   
<br>
Additionally, most bots allow for the creation of custom commands, which make the bot post a certain message in chat (see image below) and even have the bot automatically repeat the command to create a repeat the command every so often.  
<br>
<figure>
    <a href="/images/bot_guide/image2.png"><img src="/images/bot_guide/image2.png"></a>
    	<figcaption>Example of a bot, reacting to a custom command.</figcaption>
</figure>

The exact commands available differ greatly between the bots covered here, which is why I will not go into full detail about them - there are help pages and command lists for all of these bots.  
<br>
Additionally, some bots even have a graphical interface (“GUI” or “dashboard”) to control the bots.  
It simplifies the process of making changes to the bot without needing to know all the commands and how they work, since commands have to be entered exactly as they should to work properly, “something similar” will not be understood correctly by the bot.


### Nightbot
Nightbot is a bot that specializes in ease of use and fun features, and thus is especially useful for small channels, but there is no limit to the size of channel that can use Nightbot (the second biggest stream on Twitch even uses Nightbot).  
<br>
It uses a freemium model, providing basic functionality for free and removing limitations if you donate to the NightDev team.  
A full command list is found in the Nightbot dashboard.  
<br>
**Most prominent features:** 

* A dashboard, which allows you to edit settings via [http://nightbot.tv](http://nightbot.tv)
* Automated  moderation, consisting of timeouts for spammers and offensive chatters, with a wide range of settings for each type of spam
* Custom commands, with variables that allow you to put dynamic content to the commands, even trigger external URLs
* Raffles – These allow you to select a random viewer for giveaways, viewer battles and similar
* Votes/Polls – Have the viewers decide what game to play next, guess the winner of a game you are spectating or vote on which their favorite food is, or anything else that viewers should decide on 
* The ability to allow other users (for example, some of your chat moderators) to access your dashboard. These people are called “Sub users” and have almost full access to your Nightbot dashboard

You can get Nightbot by creating an account at the Nightbot dashboard and clicking the “Join” button after logging in. Make sure to make Nightbot a moderator in your chat with  
{% highlight html %}
/mod Nightbot
{% endhighlight %}



### Moobot
A bot designed for ease-of-use, with a high-level dashboard from which you can edit all of the bots settings.  
<br>
One of the biggest benefits is its extreme speed and reliability, built to prevent spam by timing out users fast enough that users don't even get to see bad messages, instead of removing them after a short duration.  
<br>
It is free to use, but certain features and restrictions require payment.  
<br>
**Partial list of features:**

* A dashboard, comparable to Nightbot's dashboard at [http://twitch.moobot.tv](http://twitch.moobot.tv) that not just allows you to change the bot, but even allows you to run commands remotely
* Automated moderation tools, with lots of settings that allow you to customize how the bot reacts to all kinds of spam
* Custom commands, with the ability to display information about your steam username, current game, League of Legends runes and masteries, XBL gamertags, currently playing song, and much more
* Raffles, Polls
* The ability to allow other users (for example, some of your chat moderators) to access your dashboard. These people are called “Editors” within Moobot and have almost full access to your Moobot dashboard
* Welcome messages to new viewers
* Features such as changing the bots username in chat, however at a price

To get Moobot, connect your Twitch account to the Moobot dashboard at [http://twitch.moobot.tv/](http://twitch.moobot.tv/)

<br>A command list is found in the Moobot dashboard - however, you dont need that! Moobot can be entirely controlled via the dashboard. To use Moobot, you have to type
{% highlight html %}
/mod Moobot
{% endhighlight %}

### Xanbot
Out of the 3 bots covered in this article, Xanbot is the only one that does not have a dashboard at the time of this write-down and is completely controlled by chat commands.  
<br>
However, it excels at moderation thanks to its support for regular expressions, which make it harder to use and therefore, more focused on advanced users, providing them with the most powerful tools to keep spam low.  
<br>
Xanbot is completely free to use for all users.  
<br>
**Some of Xanbot's features:**

* Sophisticated spam removal via the support of regular expressions on top of the basic spam filters that it essentially shares with Nightbot and Xanbot
* Custom commands and autoreplies, allowing the bot to react to messages that aren’t In the form of “!command”
* Raffle, Polls
* Several utility commands, allowing you to display information on LoL runes, masteries, the weather and much more.

You can get Xanbot by going to [http://twitch.tv/xangold](http://twitch.tv/xangold) and typing `!join` in chat. Afterwards, add Xanbot as a moderator in your channel with
{% highlight html %}
/mod Xanbot
{% endhighlight %}
<br>A complete command list for Xanbot can be found at [http://xangold.tv/help/](http://xangold.tv/help/)

## 4. Which Bot to Choose?
Now that we have covered the most common bots on Twitch, what bot should you use? Does it need to be one of these 3?  
<br>
Both of these questions cannot be answered definitively. All of these bots are under constant development, improving their stability and feature set. If you have the necessity to add a bot to your stream, you can try them out, or just use whatever bot you know best.  
<br>
If you are new to bot usage, it is definitely suggested to use Nightbot or Moobot, which have a lot of similarities in their usage.   
<br>
Nobody can tell you which bot to use in general, it completely depends on what you what the bot to do for you. But all of the bots above are great if used correctly.  
<br>
Alternatively, there are other bots which have not been handled here, examples would be DeepBot, Ackbot, and custom made bots, often just made for a single channel.  
In a lot of cases, these aren’t provided free of charge however or pose the problem of hosting – they require a server to be run on.

## 5. Getting Support
Using a bot can be complicated and hard to people who are new to moderation.   
Thankfully, there are a lot of people giving support for the bot you decide to use! In the case of the 3 bots listed above, you can find support for  
<br>
**Nightbot:** Tweet at [https://twitter.com/theNightbot](https://twitter.com/theNightbot) or use the support form on the Nightbot dashboard: [http://nightbot.tv/support](http://nightbot.tv/support)  
<br>
**Moobot:** Tweet at [https://twitter.com/MoobotApp](https://twitter.com/MoobotApp) or ask in [http://twitch.tv/Moobot](http://twitch.tv/moobot), I sometimes read that chat  
<br>
**Xanbot:** Tweet at [https://twitter.com/Xangold](https://twitter.com/xangold), [https://twitter.com/XanbotUpdates](https://twitter.com/xanbotupdates) or just ask in [http://twitch.tv/Xangold](http://twitch.tv/xangold), I usually stick around.  

<br>
However, keep in mind: we are all volunteers and may not have time to help at all points in time. Rule no.1 about getting support is patience. Leaving a support channel after a minute will most likely not give you an answer.  
<br>
I myself give a lot of support for the bots I know well, mainly Xanbot and Moobot. Feel free to PM me on Twitch if you have specific questions!  

## 6. The DOs and DON'Ts
<figure>
    <a href="/images/bot_guide/image3.png"><img src="/images/bot_guide/image3.png"></a>
    	<figcaption>Example of a poorly configured bot.</figcaption>
</figure>

While the image above might be slightly overdone, it is a common thing that I regularly see in a lot of streams - people overuse a bots features, in a way that makes chat dominated by a bot.  
<br>
This is one of the key reasons why it is recommended not to use a bot for small channels.  
A good rule you can apply to autoreplies and similar: if more than one automatically repeated bot message is visible at a single point in time, you are overdoing it.

#### DO:
**Keep spam by the bot low.**  
<br>
Have it post social media info if you feel like it, but do not overdo it.  
<br>
**Create custom commands!**  
<br>
If a certain question gets asked very frequently, just make a command that provides the answer.  
<br>
**Get support!**  
<br>
If you are unsure or new to bots and need help setting one up, there is always people with more experience than you who can help you out. (See part 5)

#### DON'T:
**Make your chat dominated by a bot (or several bots).**  
<br>
People coming your channel want to interact with you, not some computer program.  
<br>
**Rely on the bot for moderation.**  
<br>
As soon as your stream gets going, make sure to (at least almost) always have moderators in your channel.  
<br>
While well-tweaked bot settings can essentially automatically moderate chat as well as you might like, there is always things that might not be caught.  
<br>
Certain situations might require someone to adjust bot settings. For most bots, these settings can be changed by moderators, which makes having a moderator available very important at times.  
<br>
**Have too restrictive settings on the bot.**  
<br>
Why would a channel with 20 viewers have every person who posts a link timed out?  
If there ever is a wave of spambots going on, the bot settings can be easily changed.  
<br>
**Make all commands mod-only, unless you are a huge channel.**  
<br>
Why?  
<br>
If you have a command that displays important information and someone asks for that info, a commonly seen thing is that channel regulars will ask the moderators to post the command!  
<br>
In what way would that be less annoying than giving them the ability to post the command themselves? A good solution to conquer bot spam in large channels is to make commands subscriber only.  

---	

This article was written by CBenni.  
<br>**You can find CBenni on:**

* [Twitter](https://www.twitter.com/CBenni_o)
* [Twitch](http://twitch.tv/Cbenni)

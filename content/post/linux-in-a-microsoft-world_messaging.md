---
title: "Linux in a Microsoft World (Messaging)"
date: 2018-07-18T21:49:13-04:00
tags: ["Linux in a Microsoft World","skype_for_business","pidgin","youtube",]
categories: ["Linux in a Microsoft World",]
---

Welcome to part three of our journey to an open source workflow in a Microsoft loving company. In the [first installment](/post/linux-in-a-microsoft-world_email) we looked at the evolution mail client and how to configure it to talk properly with you Office 365 account and pull in your mail, contacts, and calendars. In [part two](/post/linux-in-a-microsoft-world_onedrive) we walked through setting up the basics of syncing local files to OneDrive using rclone. Here in part three we are going to tackle replacing Skype for Business with Pidgin.

Pidgin has been around for quite sometime now and is another app that has been in every distro I have ever installed. While Pidgin can replace nearly all of the functionality of Skype for Business, except for screen sharing of course, it can replace literally everything else about it. Since I am running Solus 3 with the Budgie desktop let's hop into the software center and download Pidgin and the Sipe library, shown below:

Here is a [link](https://youtu.be/kEo821R7Sis?t=8m48s) to the video at the time code I began talking about Skype for Business / Pidgin specifically on YouTube.<br /> <br />

![Pidgin / Sipe in Software Center](/screenshots/linux-in-a-microsoft-world_messaging/software-center-pidgin-sipe.png)
<br /> <br />
The reason that the Sipe library is important is because that is the original protocol that way back when in the days of Office Communicator, which became Lync, which eventually became Skype for Business uses for the chat protocol. Clearly this is black magic.<br /> <br />

![Pidgin add accounts](/screenshots/linux-in-a-microsoft-world_messaging/pidgin-accounts-screen.png)
<br /> <br />
Once you opened pidgin above go ahead and click on Add and let's begin actually configuring your account.<br /> <br />

![Pidgin basic tab](/screenshots/linux-in-a-microsoft-world_messaging/pidgin-basic-tab-screen.png)
<br /> <br />
So the above should be pretty self explanatory since you are selecting the Office Communicator protocol, thanks Sipe library, and enter you name@company.com account which would likely be your Office 365 email account.<br /> <br />

![Pidgin advanced tab](/screenshots/linux-in-a-microsoft-world_messaging/pidgin-advanced-tab-screen.png)
<br /> <br />
In the above you need to add **sipdir.online.lync.com:443** in the Server[:Port] field. You also need to change your User Agent string to the following **UCCAPI/16.0.6965.5308 OC/16.0.6965.2117**. Some folks I have spoken with are able to leave the Server[:Port] field blank and let Pidgin auto discover the server but I have had inconsistent results in the past which is why I recommend adding the above to that field.<br /> <br />

![Pidgin proxy tab](/screenshots/linux-in-a-microsoft-world_messaging/pidgin-proxy-tab-screen.png)
<br /> <br />
Go ahead and leave the defaults as shown above here.<br /> <br />

![Pidgin voice and video tab](/screenshots/linux-in-a-microsoft-world_messaging/pidgin-voice-and-video-tab-screen.png)
<br /> <br />
Same deal with the above the defaults are just fine.<br /> <br />

At this point you will be able to click on Add and you will be prompted for your Office 365 account password. Assuming the above was correctly configured and you enter your credentials correctly you should be up and running.

Pidgin does not have an ability I am aware of to add entire email distributions as groups so you will have to search for other employees using the contact search found in **Manage Accounts > Click on the account you just added > Click on Contact Search** to look people up. I have noticed that sometimes for no obvious reason it will not find colleagues when searching by their first and last names but have yet to have it fail when searching by email address. The only other functionality that is a little hit or miss is file sharing but otherwise you should be good to go. Group chats also work without issue so if there is some big emergency and your boss needs to pull you into a quick chat you are ready for action.

There are numerous ways to get around the screen sharing issue but I have also heard that they are working to try and integrate screen sharing directly into the libpurple library [itself](https://developer.pidgin.im/wiki/SoCIdeas). Needless to say that would be fantastic and more or less finish off Pidgin having feature parity with Skype for Business.

Well done! You have conquered setting up a basic open source workflow. I have at least one or two more ideas to improve on this workflow I will be writing up in the near future but again well done, pat yourself on the back, and go enjoy that delightful open source breeze hitting your face about now :) .

If you would like to watch the video covering the entire workflow click on the image below.<br /><br />

[![Open Source And Awesome Preview](/screenshots/linux-in-a-microsoft-world_email/osaa-preview.png)](https://youtu.be/kEo821R7Sis)

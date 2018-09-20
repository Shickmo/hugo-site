---
title: "Linux in a Microsoft World (Messaging Part 2)"
date: 2018-09-19T21:22:51-04:00
tags: ["Linux in a Microsoft World","skype_for_business","pidgin","youtube","screen_sharing",]
categories: ["Linux in a Microsoft World",]
---

Part four of our journey to an open source workflow in a Microsoft embracing company. The curtain draws open to reveal a most critical piece of the puzzle, how to screen share with other colleagues using Skype for Business.

Very few people seem to have stumbled upon the fact that this can be achieved and for no cost to you the awesome open source software wielder.

If you haven't checked out the previous article [part three](/post/linux-in-a-microsoft-world_messaging) now would be a really good time to do that before moving forward. That will get you setup with Pidgin and lay down the basic configuration that we are only going to tweak slightly here.

To quickly recap in [part two](/post/linux-in-a-microsoft-world_onedrive) we walked through setting up the basics of syncing local files to OneDrive using rclone and in [part one](/post/linux-in-a-microsoft-world_email) we looked at the evolution mail client and how to configure it to talk properly with your Office 365 account and pull in your mail, contacts, and calendars.

One more curve ball in this part of the article I will be showing you how to setup screen sharing running [Pop!_OS](https://system76.com/pop) since this bit of black magic, for the moment, seems to require Ubuntu / Deb based distributions. Fortunately, Pop is running 18.04 Ubuntu LTS under the hood so this will do nicely for our purposes.

First you will want to navigate to the following [sipe-collab](https://launchpad.net/~sipe-collab/+archive/ubuntu/ppa?field.series_filter=bionic) dev page on launchpad's site. Notice I mention this is a development page so your mileage may vary, though I have had almost no issues at all. I would also make sure to close Pidgin if it is running before moving on to the next step.<br /> <br />

Now open your favorite terminal emulator and run the following commands from the above page:
<br /><br />

    sudo add-apt-repository ppa:sipe-collab/ppa
    sudo apt-get update
    sudo apt-get upgrade
<br />
Okay so the above commands from top to bottom are adding the repository for the development sipe-collab library, the second command is telling your distro to update your list of packages, including those cool new ones you just added from the cool new repository, and the third is saying "Hey actually go get the updated libraries please." to which you will have to enter y, for yes do that, or n, for no don't do that. <br /> <br />

>*Side Note: Since Pop is a smarter than your average distro after you run the sudo apt-get update command the Pop Shop app installer will likely notify you that you have updates to apply that you can simply click Update All to apply them, in case the terminal may scare some folks.*

<br />
At this point let's go ahead and fire up Pidgin so we can actually take a look at how to use your new found super powers.

Let's start simple and open a chat window with one of your colleagues. Once that chat window is open click on **Conversation**, hover over **More**, and click **Share my desktop**. At this point your are sharing your desktop, well done!

Now let's say you have to join a meeting that someone scheduled for you or your team using Skype for Business. From the buddy list click on **Accounts**, then **hover over your account**, than click **Join scheduled conference..**. You will be greeted with the below. .<br /> <br />

![Join A Scheduled Converence](/screenshots/linux-in-a-microsoft-world_messaging_part_2/join-scheduled-conference-pidgin.png)
<br /> <br />
Every Skype for Business meeting invite has a meeting location URL in it. Simply copy that link and paste it in the **Meeting Location** field and click **Join**. A new window will open called chat#1, this will increment each time you open a new meeting like this during your current Pidgin session, and list the members of the chat room.

>*If you need to share your screen in this meeting just follow the same directions I just provided for the single person chat.*

### Troubleshooting Tips

Okay now let's say for some reason your in a meeting and for some reason the person sharing their screen's desktop doesn't show up. No problem of course! In the chat#1 window click on **Conversation**, hover over **More**, and click **Show presentation**. The person who is sharing their desktop's presentation should now show up! This little pro tip also will work if for some odd reason the screen share freezes and stops refreshing the person sharing their screen's desktop.

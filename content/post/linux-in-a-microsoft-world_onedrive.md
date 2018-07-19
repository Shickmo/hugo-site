---
title: "Linux in a Microsoft World (OneDrive)"
date: 2018-07-17T22:47:38-04:00
tags: ["Linux in a Microsoft World","onedrive","rclone","youtube",]
categories: ["Linux in a Microsoft World",]
---

Continuing our journey towards an open source workflow in a Microsoft based company we pull up to the intersection of rclone and awesome.

Rclone for those of you not familiar with it is an incredible free tool that is in just about every distro repository I have ever looked through. Rclone can sync local files with an impressive and growing list of services. Fortunately for you and I OneDrive, both personal and business accounts, can be synced as well.

Now if you are afraid of the command line or the mere thought of opening a terminal gives you hives, fear not dear friends as [rclone](rclone.org) has incredibly detailed and easy to follow documentation. As a matter of fact the following screenshots from my presentation on this are directly from [rclone.org](rclone.org) so all credit and the like goes to them of course.

As mentioned in my previous article on setting up [email](/post/linux-in-a-microsoft-world_email) since I am running Solus 3 with the Budgie desktop the below screenshots will reflect that fact.

Here is a [link](https://youtu.be/kEo821R7Sis?t=23m18s) to the video at the time code I began talking about OneDrive / rclone specifically on YouTube.

As usual we begin by opening the software center and searching for rclone.<br /> <br />

![Rclone in Software Center](/screenshots/linux-in-a-microsoft-world_onedrive/software-center-rclone.png)
<br /> <br />
Now that you have clicked on rclone and have it installed lets have a look at the rclone documentation for OneDrive with step by step instructions of what to do next.<br /> <br />

![Rclone Docs OneDrive 1](/screenshots/linux-in-a-microsoft-world_onedrive/rclone-docs-onedrive-1.png)
<br /> <br />

![Rclone Docs OneDrive 2](/screenshots/linux-in-a-microsoft-world_onedrive/rclone-docs-onedrive-2.png)
<br /> <br />

![Rclone Docs OneDrive 3](/screenshots/linux-in-a-microsoft-world_onedrive/rclone-docs-onedrive-3.png)
<br /> <br />

![Rclone Docs OneDrive 4](/screenshots/linux-in-a-microsoft-world_onedrive/rclone-docs-onedrive-4.png)
<br /> <br />
Really that wasn't that bad was it? I imagine that you are beginning to understand just how powerful of a tool that rclone actually is and can be for you.

I could spend quite a large amount of time going into commands to use to run the sync and how to automate that task to run on a schedule but that is outside the scope of this article. There are so very many different ways to accomplish that task and they will vary a little bit based on the distribution you are running as well. However, the instructions in the last screenshot above will give you the basics to get your first sync running.

From a scheduled task point of view I would either run a cronjob to have the sync command run however often you deem necessary but I would stay away from systemd timers if you can for this job as they are a bit more complicated and in my opinion require much more work to setup.

If anyone is interested in me doing a more in-depth article on this topic drop me an email at ray@shickmo.io and let me know.

Congratulations by the way on taking another step towards having a fully open source workflow. In the next article we will be tackling the topic of how to replace, for the most part, Skype for Business. If you would like to watch the video covering the entire workflow click on the image below.<br /><br />

[![Open Source And Awesome Preview](/screenshots/linux-in-a-microsoft-world_email/osaa-preview.png)](https://youtu.be/kEo821R7Sis)

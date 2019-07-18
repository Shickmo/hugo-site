---
title: "Linux in a Microsoft World Microsoft Teams"
date: 2019-07-18T08:30:17-04:00
tags: ["Linux in a Microsoft World","ms_teams","unofficial_client","youtube","screen_sharing",]
categories: ["Linux in a Microsoft World",]
---

Part five of our continuing journey to be able to use open source tools we want in companies that use Microsoft tool chains. This is going to be a brief update I will update I will expand on in more detail in the future. That said today we take aim on using an unofficial Microsoft Teams client on [Pop!_OS](https://system76.com/pop). So let's just dive right in!

Let's begin with navigating to the client's github page [here](https://github.com/IsmaelMartinez/teams-for-linux). Huge thanks and shout out to Ismael Martinez for the incredible diversity of ways you can install the client, flatpak / appimage / snap / rpm / deb, very impressive! If you go directly to the releases page [here](https://github.com/IsmaelMartinez/teams-for-linux/releases) you can look at all the install options you have, pick one and download it. I prefer the deb since we are running pop at the moment.

Once you install the deb and login to you Office 365 account basically you are done. Yeah it's that simple. In my limited testing so far screen sharing works to and from Linux and non-Linux based systems, notifications work correctly (even if you have the window minimized) and it's nearly a parity experience as the MS Teams client on Windows!

If you need to get fancy or change how the this client operates in some way you can hop over [here](https://github.com/IsmaelMartinez/teams-for-linux/blob/develop/app/config/README.md) and check out all the cool parameters you can add either using a cli based on [yargs](https://www.npmjs.com/package/yargs) or simply drop it in a config.json you create at the following location: vim ~/.config/Teams\ for\ Linux/config.json . I would highly recommend closing the client before trying to add the config file and making changes of course.

For example if you wanted to say change the chromeUserAgent you could simply create the file in the above location and drop the following into the file:

  {
  "chromeUserAgent": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/70.0.3538.77 Safari/537.36"
  }

That's it and so effectively the above would make it look like you are accessing MS Teams on a Windows 10 machine from Chrome.

As I said before I will very likely be updating this as I continue my testing but so far this client is looking extremely promising.

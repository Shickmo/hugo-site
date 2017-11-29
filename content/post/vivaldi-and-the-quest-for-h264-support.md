---
title: "Vivaldi and the Quest for H264 Support"
date: 2017-11-28T23:17:14-05:00
tags: ["vivaldi","browser","h264","youtube","scripts","hacks",]
categories: ["Browsers",]
---

Some say that Antonio Lucio Vivaldi was a pretty bitching Italian Baroque-ian composer, violinist, teacher, and cleric. For the record that is not the Vivaldi we will be discussing today.

I will go into more details about the [Vivaldi browser](vivaldi.com) in a future post but what I want to touch on today is how to setup full media codec support for it. Out of the box when running vivaldi on linux depending on your distro of choice you won't be able to watch h.264 based videos on YouTube.

Solus 3, which is the distro I am running as I write this article, happens to be on of the distros that does not have that codec support baked in. Below is a quick dirty hack to get this working for vivaldi-stable, which is available in the Solus 3 software center, and will get things working if you need this support immediately. Also just to clarify thanks to ruario over on github for putting this together and full credit to him on this script I am linking to below. Okay enough talk let's hack some stuff:

* Navigate to [ruario's github page](https://gist.github.com/ruario/bec42d156d30affef655)

* Once there and you have reviewed the script click Download ZIP.

* Extract the .zip wherever you like and open a new terminal.

* Navigate from the new terminal to the directory you just extracted the zip to in the last step.

* Now run sudo chmod +x latest-proprietary-media.sh.

* Now that the script is executable run ./latest-proprietary-media.sh.

* Once the script completes it will tell you to restart vivaldi if it was running and gives you a URL to follow to test that everything worked.

* Bonus step: Here is a link to a [JayzTwoCents](https://youtu.be/rc9y4zaJcXI?list=WL) video that I wanted to watch that wouldn't play before I took the above steps. If this video plays than congratulations h.264 support is yours.

During my little adventure above I was corresponding on twitter with Josh Strobl who is a core member of the Solus Team, and happens to be their Communications Manager, and he shared some pretty timely and cool insights with me.

Josh mentioned that one of the Solus community members, Joe, is working on finishing chromium. Once that work is completed the Solus Team will break out it's, chromium's that is, ffmpeg into chromium-ffmpeg and make it a run dependency of both vivdaldi-stable and vivaldi-snapshot in Solus's software center. At that point regardless of which version of vivaldi your running stable or snapshot you will get all of the h.264 codec support goodness automagically.

In short Solus and our awesome community is on the case and working towards fixing this problem properly and with style.

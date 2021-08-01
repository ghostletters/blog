---
title: "Making Programming Screencasts"
date: 2021-06-27T15:01:10+02:00
draft: false
tags: ["lessons", "learned", "retrospective"]
description: "What reduces the quality of a conversation?"
ogImage: tunnel.jpg
---

### Lessons Learned While Producing my First Screencasts

This article contains my personal notes, about things I learned, while doing my first screencast series on youtube. My initial goal was to practice my skill of presenting a problem and showcase a solution. Both parts should be somewhat 'entertaining' (given that one is into the very special topic of programming) and also be educational.

> Notice, I produced two playlists on the very same topic. The second one is already an iteration, or a version 2 release. You find the playlists on youtube [version 2 here](https://www.youtube.com/watch?v=CY4Xqy2DQog&list=PLxkAEgr9RgPe7e5EhdPpaGP21M0F5ExpO) and [version 1 here](https://www.youtube.com/watch?v=CY4Xqy2DQog&list=PLxkAEgr9RgPc6WBfOZqxZeoq357f7FfPP).

{{<img src="tunnel.jpg" alt="a glass tunnel" loading="lazy">}}

#### The IDE/Editor

The IDE is the crucial part in my screencasts, because I spent most of the time there writing and talking about code. I learned the following things:

- increase the font size. This sounds kind of obvious, but just keep increasing the font size when you think it is enough. If you feel like asking 'Is this big enough?', the answer is 'No, it isn't'
- hide all distractions. Again this sounds obvious, but there is a lot of stuff on the screen that your viewer is not interested in and that waists your [screen real estate](https://youtu.be/bFcaO1pXzws?t=695). For instance
  - make the IDE/editor full screen, so you get rid of all task bars, window titles and other decorations. This gives you also more room for a bigger font
  - hide all file trees, terminals, IDE goodies, etc if you do not use them. 
  - in case of bootstrapping a project with a command (common in JS and newer Java frameworks), delete/hide all the cruft you don't use. In IntelliJ I use a [custom scope](https://www.jetbrains.com/help/idea/settings-scopes.html), that hides everything except `src/main/java`, `src/main/resources` and `pom.xml`.
- do you actually need line numbers? If you never mention them, hide them.
- don't waist time on typing. Watching people type is mostly boring. If you are like me a rather slow typer, don't worry, just speed the typing scenes up in post-production of the video. This means you should not talk during typing, otherwise the speedup will distort your voice

I use the [ZEN mode in IntelliJ](https://blog.jetbrains.com/idea/2020/01/intellij-idea-2020-1-eap-2/#zen_mode) which provides fullscreen and most hiding automatically.

#### Equipment

- Invest into a decent microphone. The whole internet will thank you, really.

That's all for equipment

#### Recording Software

- I am pretty happy with [OBS](https://obsproject.com). It is easy to get started and has a lot of advanced features. So far I did not need any of them. It is available for Windows, MacOS and Linux

#### Post Processing Software

- Whatever software you choose here, learn how the basic cutting workflow works (meaning: learn at least the shortcut), because you will spend a lot of time cutting (or you are a natural talent and produce one takes right from the start :D)
- I use [ShotCut](https://shotcut.org), and I am pretty happy with it. Again, it is available for the big three OSes
- prefer speed up instead of cutting out parts. Hard cuts make it harder for the viewer to follow what you are doing. Even a jumping mouse cursor, because you just cut 2 seconds can be disturbing. Speeding up the video is more subtle
  - speeding up for more than 3x can also feel weird for the viewer. Try to not overdo it with speed-ups

#### Youtube

- Provide a custom thumbnail, it helps potential viewers to find your video and increases your professional appeal. In contrast, the auto thumbnail - usually an unreadable view on the editor - carries close to zero information for your potential viewer
- provide chapters for the video. [Chapters on youtube](https://support.google.com/youtube/answer/9884579?hl=en) are timestamps in the description that show the viewer the agenda and enable jumping to relevant sections
- add videos to playlists if they belong together
- customize your channel a bit, so it looks decent. Setting a picture and banner image will already bring you a long way
- write a short summary what this is about. 
- link to other resources like your github, blog, additional resource like docu, etc.

#### Supporting Resources

Try to provide links to resources you used or created for/during the video, for instance a link to:
- the code you produced during the video is a good start
- a blog post you created in support of the video
  - the blog post of course links back to the video
- link to official documentations, blog posts or other videos can help your viewer to understand how everything works together. Each brain processes information different, so providing multiple angles is helpful

I might update this post in the future (or write a follow up) as I continue to do videos and learn more. A general thing I learned, that did not fit in any category so far, is to continuously streamline the video content. Meaning: it is totally fine to start with a very rough version. It is easier to improve a rough version than it is to plan a smooth one. Then shovel away all the distractions till it feels like a smooth ride from problem to solution. :)
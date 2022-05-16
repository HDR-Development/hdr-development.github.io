---
title: Mad Villain's Testing Guide
author:
  name: Mad Villain, techyCoder81
  link: https://github.com/HDR-Development
date: 2022-05-15 09:00:00 -0700
categories: [Guide, ProjectInformation]
tags: [guide]
---

## Welcome (techy)
Today's Development Blog is written by our leading tester Mad Villain, on how to get into helping out with the project via testing! In case you also missed it, there is now an @testing role which you can go get in #welcome channel in the discord to be informed when contributors or devs really need something specific tested. Read on to learn how to contribute to the project, whether a little or a lot, by testing early builds and helping us find issues before they make their way into betas.

# Testing Guide (Mad Villain)

Greetings fellow humans, my tag is Mad Villain and I'm the self appointed lead playtester for HDR. If you're like me and enjoy labbing upcoming changes or wish to contribute to playtesting new characters, features, or engine changes, you've come to the right spot. I'll be providing you with a general outline on how you can setup your switch console for playtesting potential changes to HDR.

## Why is testing needed in the first place?

As with any new project, the appearance of bugs and other oddities is unavoidable. These issues can end up ruining the user experience or in worse cases, cause a game crash. Hence, it's imperative to try to resolve any issues before patch updates occur. As HDR is still in beta, play testing is an essential tool for our developers to have to stamp out any unforeseen problems. Not only does playtesting serve as a tool for weeding out bugs, but it's immensely helpful for  developers to have user feedback on possible engine/character changes as well as it helps in deciding what may or may not be implemented. With that out of the way, we'll move on to the most important form of testing... 

## Nightlies

Typically once a day (or every  few days), when changes get merged, a nightly update is built and uploaded to HDR's github repository. This patch is known as a "Nightly" and contains the most recently approved changes to the base game of HDR. It is within this patch that most testing should occur. 

The simplest way to test out a nightly is by updating to it from the HDR launcher page. Follow this visual guide through the process: 

[Nightly Installation Image Guide](https://imgur.com/a/g4n5tEy)

And with that, you should be able to test out the newest experimental builds. 

## How should you test?

Mainly, the best form of testing is to simply play the game. Playing it with another person offline/online or even against CPUs can help you find any oddities that may occur as a result of the newest changes. Most changes in the patch will come in the form of system or character alterations so directly playing with them is the most effective method of testing. Take note of anything that doesn't seem to function as intended, especially if it causes some sort of crash to the game. You can also give feedback on the changes, including voicing any concerns with system or character changes. You can report your findings/feedback on the [Issues page on Github](https://github.com/HDR-Development/HewDraw-Remix/issues).

To make it easier for the developers to sift through your issues, please use the following format in the title header:

`[Nightly ver. XX.XX] Character/System Change - General Description of Issue`

For example, if you'd like to report an issue about wavelanding it would be written as:

`[Nightly ver. 06.35] Waveland ECB Change - Certain characters can't waveland properly on these stages`

*(In the comment area, please provide specific details of the issue and provide image/video links if possible)* 

Once you're done writing out the issue, click on the submit issue button. 

And that's it! If you have any other questions in regards to nightly testing feel free to post ask in the [#testing channel](https://discord.com/channels/659964948365049887/950979417004466196) in the server.

*(If you want to switch back to the public beta build, go back to the launcher page and click on "Options" and then choose "Switch to Beta")*

# Advanced Testing Guide

While testing the nightly patch is the most recommended form of testing, some users can opt to test individual changes instead. You can do so by adding files from a Pull Request (which I will abbreviate as PR). A PR is a type of submission done by developers that is "requesting" the permission of other developers to be approved and added to the Nightly. That is to say, the changes done in a nightly patch is simply a culmination of PRs . The PRs normally aim to change one particular aspect of HDR such as stage parameters, cameras, UI, and character balancing, among many others. Reviewing PRs made by the developers can help them iron out any kinks within their changes before it is approved and reaches the nightly build. If you're interested in testing PRs please follow the instructions below.

First begin by going to the [Pull Requests page.](https://github.com/HDR-Development/HewDraw-Remix/pulls) This page contains all the pull requests that are available for review by other developers and testers. From here you can choose any of the PRs you would like to test out. For this example, we'll take a look at the Dr. Mario Changes PR. The following guide will demonstrate how to test this change.

[Sample PR Change Image Guide](https://imgur.com/a/3LKUF1j)

Just like playtesting the nightly patch, the developers appreciate any feedback on the changes they are working on. You can leave that feedback by writing a comment on the individual PR's page by scrolling towards the bottom of the page. 

It can also be helpful to look at the [Issues page](https://github.com/HDR-Development/HewDraw-Remix/issues). Most PRs should include a link to an issue - they will say something like `Fixes #234`, which indicates that this PR is meant to address that linked issue. Sometimes the useful discription for a PR is not on the PR itself, but rather in a linked issue. Keep this in mind.

*Elaboration from techy: We actually *REALLY* appreciate having pull request builds tested before they get merged. In the past, though rare, we have merged things into the nightly which were not tested by someone other than the developer, and the result was a lot of headache (by me or blujay) to go back and figure out at what point the crash started. If we had more nightly players, this may have been caught sooner, but the biggest impact on this is people taking a moment to play a PR build and say "yep, it doesn't crash, and it seems to function more or less as written." Even just this kind of very basic feedback is priceless.*
#
## Training Mode Visualizer

One of our esteemed developers (blujay) has created an experimental hitbox/hurtbox visualizer for HDR, which can be very helpful while testing. If you'd like to use it alongside your testing, here's a quick guide on how to install it. 

First download the visualizer from the following link:
[Visualizer download link](https://cdn.discordapp.com/attachments/950977159088975883/954634337297498122/HDRvisualizer.7z)

After extracting the file, follow the instructions on the link below:

[HDR Visualizer Installation Image Guide](https://imgur.com/a/DMqxoJ2)
#
## ROMFS Changes (super advanced testing)

In some of the PRs created by the developers, their is a possibility that they require downloading extra files other than the "hdr-switch" file. The file being referred to here is known as **ROMFS**. The developer will indicate if this file is necessary in their description of the PR. ***Please note that this isn't necessary for most changes and only do this step when it is explicitly written on the PR description.*** 

To get this file you'll have to go to the page containing in-development [romfs releases](https://github.com/HDR-Development/romfs-release/releases).

 1. Download the latest ROMFS file available by clicking on "romfs.zip"
 2. Extract the files inside the ROMFS Zip
 3. Click on the ultimate folder and rename the file "hdr-assets" and "hdr-stages" to "hdr-pr-assets" and "hdr-pr-stages"
 4. Drag the ultimate folder to the root of your SD card
 5. Open the mod manager and make sure to disable the "hdr-assets" and "hdr stages", and enable "hdr-pr-assets" and "hdr-pr-stages"

If you are not careful, and do not follow the above steps, you may "break" your installation according to the launcher. Follow the steps above closely if you plan on testing romfs changes.

*(Note: You can switch back to base HDR by reenabling "hdr-assets" and "hdr-stages" and disabling the "hdr-pr-assets" and "hdr-pr-stages" on the mod manager)*


## And thats it!
There are a lot of ways people can help out testing, and we hope that with this guide and the newly available @testing role, more people will get involved!
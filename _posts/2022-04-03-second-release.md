---
title: HewDraw Remix's Second Public Beta and State of the Game
author:
  name: techyCoder81, blujay
  link: https://github.com/HDR-Development
date: 2022-04-03 07:00:00 -0700
categories: [Release, ProjectInformation]
tags: [release]
---

# Welcome

Hey guys, today we have another public beta release! There are a lot more changes in here than you would probably expect, so read on! First we have a high level overview of the major new changes, and then after that we have the development commentary and news.

# Whats new?
A full changelog should be posted in the coming days, but in the mean time here's a high level view of what's new.

## Big new stuff:
* We have a **launcher/updater** now! See the launcher section below where we talk about it! The goal is to make hdr updates as fast and seamless as possible. This is just the first version (though we have tested it a lot ourselves), so there may be some hiccups here and there. ![](https://cdn.discordapp.com/attachments/950979381654855701/960194166523052063/2022040308081300-0E7DF678130F4F0FA2C88AE72B47AFDF.jpg)
* A whole new stage select screen, courtesy of JoBen's hard work! This has been in the works for a while, and now its finally here! ![](https://cdn.discordapp.com/attachments/950979381654855701/960104035980038184/2022040303495500-0E7DF678130F4F0FA2C88AE72B47AFDF.jpg)
* A new arena UI, courtesy of Kalomaze! ![](https://cdn.discordapp.com/attachments/950977159088975883/959936310506819604/2022040216542100-0E7DF678130F4F0FA2C88AE72B47AFDF.jpg)
* **prcxml!** Our params files are now all stored as `.prcxml` files in our `/ultimate/mods/hdr` folder. These can be edited much more easily because of this, and public contributors can finally make pull requests and contributions that change params!
* **Packaging improvements!** Our automatic packaging infrastructure now creates *full* installations of HDR automatically. The [switch-package.zip](https://github.com/HDR-Development/HDR-Releases/releases/download/v0.5.12/switch-package.zip) on our [Releases page](https://github.com/HDR-Development/HDR-Releases/releases) contains *everything* you need besides atmosphere. If you have a modded switch (IE, you have atmosphere), extracting that zip to the root of your SD is all you need to install HDR. Alternatively, you can use our awesome launcher's `Install` button, and the launcher will install HDR for you!
* As a result of packaging updates, this beta does not come with a dedicated ryujinx installation zip. This is something we care about, and we will be finding time to add dedicated ryujinx installation folders in the near future, probably by next beta. However, we are told that you can potentially extract all of the normal switch package to the `sdcard` folder in Ryujinx and it will "just work."


## Engine
* Jab locks now function similarly to PM. Your tech option is locked in the moment you get jab locked.
* Double traction was fixed in this beta, so characters should not feel as slippery in states where they shouldn't be.
* Ledge occupancy was fixed! In the last beta, performing ledge actions didn't actually hold ledge occupied. Now, ledge actions will actually continue to occupy ledge, but this time only for 75% of the animation's length.
* Parry window was reduced from 5f to 3f
* Drift DI was reduced at combo kb levels, to make followups more consistent at low knockback

## Character changes
* Marth
    * This guy was an atrocity! We spent a bunch of time in a call a few days ago to straighten him out. Some of his hitboxes were made smaller, and some of his moves, such as fair and uair and utilt, had their active frames reduced to be more reasonable. Additionally, the vfx were updated to more appropriately convey where his hitboxes are actually placed. Additionally, all of his tipper hitboxes were adjusted to be more consistently placed between moves. Details can be found [here](https://github.com/HDR-Development/HewDraw-Remix/pull/420), as well as in the eventual full changelog.
* Falco
    * Falco had a fair few changes as well! Most of the Falco work this time around was contributed by TeamPear! The biggest change is his dair being reworked. As it turns out, his HDR dair stronger, faster, laster longer, and had less endlag than melee dair by about 25% across the board! After the changes, the move is overall more like a nerfed ntsc dair, but with less endlag overall and more reasonable active frames.
* Duck Hunt
    * This character had a few nice changes this time around as well! The changes for this character were contributed by Sejong, and among a few other things, its biggest change was in making gunman a move which has a gimmick timer (meaning you cannot use it until 10-15 seconds until you last used it), and the gunman firing is now triggered with a down special input while the gunman is out.
* Palutena
    * If you know, you know. Palutena's wall was really something else. We had reports of matches against Palu going practically to timeout consistently, and this was one of the most complained about moves we've seen in a while. There were a fair few changes made to this move to make it a lot more reasonable to deal with, and you can read the details [here](https://github.com/HDR-Development/HewDraw-Remix/issues/309).
* This change (though relatively simple) is funny enough that we felt it necessary to include it here. If you pummel with wario, a coin vfx and sfx is played, ala Mario up special. This minor change was contributed by Spawn_32.
* Other minor changes
    * Many other minor changes and fixes were made to various characters, which you'll want to stay tuned for an updated changelog for. Or, go try them yourself! The overall list of changes is available (at the high level) on the [Releases page](https://github.com/HDR-Development/HDR-Releases/releases)


# New Contributors
This time around, we've had some new contributors joining the contributor list! Our development process has been improving as always, and more people are slowly learning how to make moveset changes and help contribute bugfixes. If you want to get more involved with this, we still intend to write a more comprehensive contributing guide at some point. Also, in the near-ish future, Techy intends to host a sort of contributing workshop where we work through the process from start to finish on stream of setting up a fresh pc, to having made a public contribution/fix to HDR, so stay tuned for that.
We would love it if our contributors who have a different github username than on discord would please add their github username to their server nickname, such as `@techy (techyCoder81)`. If its close enough, then that's fine, but some of you guys have *very* different usernames on the two platforms. Here are our new contributors this time around. If your name is not here, please let us know and we will get you added.
* Sejong - Duck Hunt rework
* TeamPear - Falco rework
* Kalomaze - New Arena!
* Bede - A new Sonic fair animation
* Stabb - Mario fair doc-esque "sourspot" removal
* Mini - Dark Pit down special improvements
* Mythril - Kirby's Sonic homic attack fix
* Spawn_32 - Numerous changes to characters

# Coming Soon
Stay tuned for the new things coming up soon:
* Development commentary blogpost for this update
* Contributing guide
* Contributing workshop
* [Serpent Showdown!](https://twitter.com/HewDrawRemix/status/1510267811137957896) This upcoming online tourney in the HDR discord should be a blast, and you should go sign up.

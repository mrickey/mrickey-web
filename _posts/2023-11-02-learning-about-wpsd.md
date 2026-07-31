---
id: 2165
title: 'Learning about WPSD'
date: '2023-11-02T13:02:11-07:00'
author: af6fb
excerpt: ''
layout: post
guid: 'https://mrickey.com/2023/11/02/learning-about-wpsd/'
permalink: /2023/11/02/learning-about-wpsd/
footnotes:
    - ''
    - ''
categories:
    - 'Amateur Radio'
tags:
    - Wpsd
format: false
---

I recently interviewed Chip W0CHP to learn about WPSD, how it got started and where it is going.

#### What is WPSD?

WPSD is a tool for digital voice enthusiasts to manage their digital communications. It is a progression of the Pi-Star and MMDVM projects. It was originally created for power users to experiment with the latest updates in MMDVM, but has progressed to a point where all users can take advantage of what it offers.

Chip is a long time supporter and developer of Free Open Source Software (FOSS) and values what it brings to ham radio operators. If is wasn't for open source software we wouldn't have many of the programs and modes we have today. One of those packages is Pi-Star, created by Andy MW0MWZ, has become a valuable resource for hotspots by a variety of manufacturers. It creates a nice user interface for people to setup and configure their hotspots.

There was a point were Pi-Star wasn't keeping up with updates from the MMDVM project and it was becoming dated. This is when Chip decided to make wholesale changes to the user interface and implemented new functionality and features in WPSD. This included newer modes like M17, AX.25, and FM. WPSD images have been updated to include the current Raspberry Pi operating system.

With these changes, WPSD has become very popular recently both with users and volunteers. The project has attracted a wide variety of volunteers to help with the project. But, more help is always welcome. It would be helpful to have more volunteers interested in testing/QA and documentation (code commenting and documentation). There is sub-project that could use some attention as well. This is translations. The code needs to be updated to support more robust and updated localization, then additional language files need to be created. If you have experience with PHP libraries like GNU gettext, please contact Chip. He is looking for people to translate the language files.

To get involved with writing code for the project your best avenue is to submit a pull request in the WPSD code repository or become active on the WPSD Discord server. A [WPSD Contributor Guide](https://w0chp.radio/articles/how-to-contribute-to-wpsd/) is available to help get you started.

#### What as changed?

As mentioned there are many changes between Pi-Star and WPSD. There are some things that have been removed. In most cases these things won't impact most people. For completeness, here is the list from the WPSD website:

- DSTARrepeater mode/controller type removed: WPSD operates in the more modern and updated/supported MMDVM mode only. You can still run WPSD as a D-Star hotspot/repeater, of course.
- Upgrade notice/nag in header has been replaced by an update notifier; displayed in the upper-right hand side of the top header.
- “Upgrade” has changed to “Update” and the command line "`pistar-update`" takes care of all upgrades and updates.
- hostname is displayed in the browser title instead of taking up space on the screen.
- “GPS” link in Call Sign column of dashboard (superfluous and unreliable).
- CPU Temp. in header only shows color when the CPU is running beyond recommended temps. It will show as orange or red depending on how far outside the norm it is.
- No reboot/shutdown nag screen from admin page (it will reboot/shutdown without warning).
- Yellow DMR Mode cell in left panel when there’s a DMR network password/login issue (poor/inaccurate and taxing implementation, and can confuse power users that utilize my Instant Mode Manager, where the default cell is amber colored for paused modes \[color is user-configurable\].). Instead, the actual network name is highlighted in red when there’s a login issue.

There is also a lot of new functionality as well, again, straight from the WPSD website:

- Full APRSGateway Support: Selectable APRS Data Sharing with specific modes.
- Full DGId Support (YSF).
- “Live Caller” screen; similar to a “virtual Nextion screen”; displays current caller information in real-time.
- Current/Last Caller Details on Main Dashboard (name/location, when available).
- Talkgroup Names display in target fields (Brandmeister DMR, NXDN and P25 support only).
- YSF/NXDN/P25/M17 link managers gives the ability to change links/rooms/reflectors/TGs on-the-fly, rather than going through the configuration page.
- DMR Network Manager allows instant disabling/enabling of configured DMR networks/masters; and fast switching of XLX reflectors and modules. Handy for “pausing” busy networks, talkgroups, timeslots, etc.
- Full M17 Protocol Support.
- BrandMeister Manager revamps galore:
    - Now displays connected actual talk group names.
    - Connected dynamic talk groups now display idle-timeout time (due to no TX).
    - Added ability to mass-drop your static talk groups; and mass re-add the previously linked static talk groups.
    - Added ability to batch add/delete up to 10 static talk groups at a time.
- “Instant Mode Manager” added to admin page; allows you to instantly pause or resume selected radio modes. Handy for attending nets, quieting a busy mode, to temporarily eliminate “mode monopolization”, etc.
- “System Manager” added to admin page; allows you to instantly:
    - Disable / Enable the intrusive and slow Pi-Star Firewall.
    - Disable / Enable Cron, in order to prevent updates and Pi-Star services restarting during middle-of-the-night/early AM operation.
- Ability to configure POCSAG hang-time from the config page.
- Native Nextion screen support built-in; no futzing around with Nextion drivers/scripts.
- Selectable DMR Roaming Beacon Support: Network or Interval Mode (or disabled) - for actual repeaters only.

A change not talked about too much in the list above is the move to DMRGateway instead of the older internal DMR code. DMRGateway was available on Pi-Star, but it was not the default and many people didn't understand how to use it. DMRGateway is the ONLY way supported way to configure and use DMR now. The advantage of DMRGateway is that it supports the operation of multiple, simultaneous DMR networks. For more information about this look for a later article or the WPSD website.

On the DSTAR side the changes are minor, both in configuration and functionality. The biggest difference is a lack of support for terminal mode.

#### Let's talk about M17

For those that don't know, M17 is a digital voice and data mode that is fully open source. This means it is available for hobbyists to experiment with. It can also be implemented on fairly small processors, think STM32 chips. Some of the benefits include no central registration (like RadioID.net), fully open source, and open hardware.

WPSD is also tightly coupled with M17 having recently announced a combination of efforts and leadership. This partnership will allow both to accelerate their development and hopefully get radios into the hands of users sooner.

#### How to get started with WPSD

Getting started with WPSD is much like getting started with Pi-Star. You will download the image, burn it onto an SD card and boot up the hardware. It is recommended you start with a new MicroSD card, keep your Pi-Star card as is until you are comfortable with WPSD, just in case you need to switch back.

Spend some time exploring the user interface. It is different and will take you some time to become familiar with it. Everything is there, it has just moved around. You shouldn't be afraid to make changes...worst case you will just need to hit reset and start again; or, revert to a working, previously-created profile using the WPSD Profile Manager.

When setting up DMR, there are multiple networks on the page. You only need to setup the networks you plan to use. Leave the others blank. Also, be aware that if you are using networks other than BrandMeister you will have to use a prefix on the talkgroup ID. See [this page](https://w0chp.radio/articles/dmr-operation-on-wpsd/) for details on the prefixes.

Profiles will allow you to create a configuration and save it. This is different than a backup because you can have several saved profiles and switch between them. For example, your default profile might have several modes enabled. You could also create a profile with just a single mode enabled...for a net or special event. Profiles are also useful for instantly reverting back to working configurations, after making adverse configuration changes.

From the author: Load up WPSD, poke around and try it. I have been using it for a while and like the new menus. You should join the communities for support and ideas.

It is time for some screen shots. Here is the dashboard, this is the first screen you will see when you visit your hotspot.

<figure class="wp-block-image size-large">![](https://mmdvm.com/wp-content/uploads/2023/11/WPSD-Dashboard-778x1024.png)</figure>Live Caller is a new screen, this is something similar to what you would see on a nextion screen.

<figure class="wp-block-image size-large">![](https://mmdvm.com/wp-content/uploads/2023/11/WPSD-Live-Caller-1024x389.png)</figure>Up next is the Admin screen, this has changed a lot. It is no longer similar the the dashboard, rather it allows you to administrate your hotspot.

<figure class="wp-block-image size-large">![](https://mmdvm.com/wp-content/uploads/2023/11/WPSD-Admin-1024x714.png)</figure>Another interesting addition here is the Instant Mode Manager. You can come to this page to pause or resume a mode. Let's say you are trying to talk to someone on P25 and there is a D-STAR net that keeps interrupting. This would let you pause or deactivate D-STAR until you are done. When suspended, the mode will show as orange on the dashboard.

<figure class="wp-block-image size-large">![](https://mmdvm.com/wp-content/uploads/2023/11/WPSD-Mode-Manager-1024x714.png)</figure>And finally, there is the Advanced page. This capability was available in Pi-Star, but I think it has become much more useful in WPSD. The links are arranged in menus for easier access.

<figure class="wp-block-image size-large">![](https://mmdvm.com/wp-content/uploads/2023/11/WPSD-Advanced-1024x714.png)</figure>Links:

- [WPSD Homepage](https://w0chp.radio/)
- [WPSD Source Code Repositories](https://repo.w0chp.net/explore/repos)
- [Discord](https://discord.gg/b8Hv5ygPdF) for community support and contribution collaboration
- [Facebook](https://www.facebook.com/groups/w0chppistardash) for community support
- [MMDVM](https://mmdvm.com) Project
- [M17](https://m17project.org/) Project

This article first appeared on [MMDVM.com](https://mmdvm.com/learning-about-wpsd/)
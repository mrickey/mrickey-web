---
id: 2121
title: 'From Pi-STAR to WPSD'
date: '2024-08-06T13:27:35-07:00'
author: af6fb
excerpt: ''
layout: post
guid: 'https://mrickey.com/?p=2121'
permalink: '/?p=2121'
footnotes:
    - ''
categories:
    - Uncategorized
format: false
---

If you have a digital hotspot, like a ZUMspot, there are changes coming. If you already have a hotspot, this change is not required. New hotspots from ZUMradio and Bridgecomm will have software that is not Pi-STAR.

Several years ago, around the beginning of the pandemic, a project called WPSD was started in earnest. This is a fork of Pi-STAR that has grown and changed to improve the user interface and take advantage of newer capabilities on the underlying MMDVM software.

I recently interviewed Chip W0CHP to learn more about WPSD and how it affects users. Here is a summary of what I learned.

## What us WPSD?

WPSD is a tool for digital voice enthusiasts to manage their digital communication. It was originally created for power users. In its current form, WPSD is a replacement for Pi-STAR. As more people started looking at it the user base evolved and changes were made to make WPSD more accessible for all users.

## Why do we need a new version of Pi-STAR?

The community was happy with Pi-STAR, but, and developers were helping the project with code submissions (pull requests). Some of the new features and code fixes were ignored and Pi-STAR stared to slow down on issuing updates. The operating system in the Pi-STAR images is now old and no longer supported with updates.  
  
Moving to a new platform allowed Chip to use a current operating system and fix some functional problems as well as add new features. For example, MMDVM now supports M17, WPSD supports this but Pi-STAR does not.

Chip is satisfied with the project and proud of creating something a large number of people are using. He has learned a lot in the process and excited for the future. The project has attracted a wide variety of volunteers to help. Primarily developers and power users that are helping others. He could use help in the areas of testing/QA and documentation (code comments and manuals).

A future project that will require a number of volunteers is localization or translating WPSD for multiple languages. This will involve two steps with different skills. First will be updating all of the code to pull message, like the text on the screen, from a file. Second is translating this file to other languages. If you have these skills and would like to help, please jump on one of the forums and speak up.

Developers can, and are encouraged to, submit pull-requests if they find an issue with the software. And everyone should participate in the forums (more on those later).

## WPSD is Different than Pi-STAR

WPSD is a bit of a restart when compared to Pi-STAR. The user interface is different, the menus are different and some of the functionality is different.

There are some things about Pi-STAR that have been retired. They are listed on the website if you want more detail:

- DSTARrepeater mode/controller type removed: WPSD operates in the more modern and updated/supported MMDVM mode only, you can still run WPSD as a D-Star hotspot/repeater, of course.
- Upgrade notice/nag in header (unnecessary and a hacky implementation). This has been replaced by my own unobtrusive and configurable dashboard update notifier; displayed in the upper-right hand side of the top header.
- “Upgrade” feature via the dashboard and command line (`pistar-upgrade`) is removed. The “Update” feature via the dashboard and command line (`pistar-update`) takes care of all upgrades/updates.
- Custom `BannerH2` (etc.) text options have been removed (added clutter and I never used it). Instead, the hostname is displayed in the browser title.
- “GPS” link in Call Sign column of dashboard (superfluous and unreliable).
- CPU Temp. in header; when CPU is running “cool” or “normal” recommended temps, the cell background is no longer colored green. Only when the CPU is running beyond recommended temps, is the cell colored orange or red.
- No reboot/shutdown nag screen/warning from admin page (Superfluous; you click it, it will reboot/shutdown without warning.).
- Yellow DMR Mode cell in left panel when there’s a DMR network password/login issue (poor/inaccurate and taxing implementation, and can confuse power users that utilize my Instant Mode Manager, where the default cell is amber colored for paused modes \[color is user-configurable\].). Instead, the *actual* network name is highlighted in red when there’s a login issue.

There are welcome updates and new features as well. For starters the user interface has been updated to make it a little simpler, but things have moved around so it will take some time to get used to everything. There is now an instant mode manager, this allows you to pause modes. This is handy if you are going into a net and you don't want other modes to bother you.

Configuration has changed a fair bit. The main config page has remained very similar, but other areas are very different and easier to navigate.

The Admin page is now more useful as it is actually an administration page instead of looking very much like the dashboard. The new Admin page allows you to manage the different mode connections, like changing reflectors. It also shows the status of all the running services.

A new an interesting feature is Live Caller. This is a simplified page that shows something similar to the display on the hotspot...nice when you can't see the hotspot directly.

I won't go into all of the details on new and changed features, but I hope this gives you an idea of the changes.

Now let's move to changes on DMR and D-STAR. In Pi-STAR DMR operated using what is called Direct Mode. Meaning it would connect to a single server. That has been removed and DMR is now running DMRGateway. This was available before, but it looked complicated and many people decided not to try it. What is the benefit? As you probably know there are multiple DMR networks (Brandmeister, HBLink, XLX, FreeDMR, TGIF, and I'm sure there are others), DMRGateway allows you to connect to all of them, at the same time.

You can setup one, some, or all of these. The way you direct to the correct gateway is by putting a prefix on the talkgroup number.

If you use only Brandmeister, you won't notice any differences.

For D-STAR, the change removes DstarRepeater. This is old and no longer supported software. WPSD is now using <mark class="has-inline-color" style="background-color:#fcb900">FixMe</mark> instead.

Pi-Star stopped pulling new versions of the MMDVM software stack a while back. This means it can't support newer features like M17, AX.25, and FM. WPSD supports all of these.

If you haven't heard about it yet, M17 is an open source digital voice and data mode. It has no central registry (for things like radio
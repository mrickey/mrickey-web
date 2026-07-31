---
id: 488
title: 'Talker Alias on BrandMeister'
date: '2018-02-07T20:46:13-08:00'
author: af6fb
excerpt: ''
layout: post
guid: 'http://mrickey.com/?p=488'
permalink: /2018/02/07/talker-alias-on-brandmeister/
image: /wp-content/uploads/2020/09/8a5b9-dmr-logo.jpg
categories:
    - 'Amateur Radio'
tags:
    - brandmeister
    - hytera
format: false
---

Talker Alias allows a radio to receive contact information from the transmitting radio. Much like D-STAR and Fusion, this removes the need to have a large contact list. Additionally, BrandMeister helps the process by creating a Talker Alias string if the transmitting radio doesn't send one. ![](/wp-content/uploads/2020/09/ed0de-mvimg_20180207_1938323357814867462972305.jpg)Talker Alias was added to the DMR ETSI spec in June 2016. To date, the only radios to support Talker Alias are Hytera and the MD Tools software (MD-380, MD-390, and maybe the MD-2017). Additionally, Talker Alias is only passed through Hytera repeaters, MMDVM-based repeaters and most hotspot devices (OpenSpot, MMDVM/Pi-Star, etc). With those limitations in mind, this is still a great feature. Hytera and TYT covers a large chunk of DMR users worldwide. BrandMeister as included the ability for you to modify the text sent via Talker Alias, this is done through the Selfcare page using the ***APRS Text*** field. BrandMeister always adds your call sign in front of the APRS Text field. ![](/wp-content/uploads/2020/09/e2d97-talker-alias-selfcare.png) In the last heard list you can see which users have set this text and which have not. The default value is "DMR ID:3106xxx". Here is an example of some people with APRS Text, and some without. I'm not trying to call anyone out here, just providing an example. ![](/wp-content/uploads/2020/09/9a0d5-talker-alias-last-heard.png?w=300&h=184)For the benefit of those using Talker Alias, please modify your APRS Text to have your name. This also gives you some control over how your name is shown... More information about Talker Alias and how it is supported on BrandMeister, please visit the wiki at https://wiki.brandmeister.network/index.php/Talker\_Alias. There is also a link to the ETSI specification for more information about how Talker Alias was implemented in the protocol.
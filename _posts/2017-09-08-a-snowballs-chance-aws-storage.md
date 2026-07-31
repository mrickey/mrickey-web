---
id: 318
title: 'A Snowballs Chance &#8211; AWS Storage'
date: '2017-09-08T15:38:27-07:00'
author: af6fb
excerpt: ''
layout: post
guid: 'http://35.202.40.146/?p=318'
permalink: /2017/09/08/a-snowballs-chance-aws-storage/
image: /wp-content/uploads/2020/09/a0388-ie_sb_device_4.png
categories:
    - Technology
tags:
    - aws
format: false
---

You've decided to move your hosting to Amazon Web Services (or AWS), but you have amny gigs of data to move up there. Do you upload it or send a hard drive? Or do you have enough data that you need to send multiple hard drives? What if you have 40 GB to send? How do you shard your data across multiple hard drives? AWS has the answer and it's called Snowball. This is a rugged device you can order through your AWS console. It arrives as you see it below. No box, just the device. You plug it into a 110v outlet and connect it to your network, it supports up to 10 GB speeds. Did I mention it weighs 50 pounds? Bring a friend to help you lift it. There is an e-ink display that is used for configuration and as a shipping label. Once connected you can copy your data to the Snowball. It support 50 terabytes of storage. All of your data is protected by a 256-bit encryption and a 25 character unlock code that you set. As part of the process you create a job manifest that tells Amazon how to ingest your data into S3. The cost is $200 per job and you can take up to 10 days to copy your data to the device before shipping it back. Source: \[[AWS Blog](https://goo.gl/VBqOui)\]
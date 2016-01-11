---
layout: post
title:  "Machine Types - Google Cloud"
date:   2016-01-11 08:15:00 -0800
categories: tech update
---

Since the beginning of cloud computing, platform providers have been looking for various ways to overcome the limitation in customizations available. For Google Cloud, it started with providing App Engines, which are still one of the best starting points for any app deployments, as it handles the platform for you.

But this was never enough, Google launched Compute Engine along side and has been improving on various offering, be them in the segment of Big Data services, Storage or Monitoring. The cloud ecosystem has matured and we are witnessing new features and products every now and then.

If you use Compute Engine, or its equivalent offerings by other providers, you should have noticed that there are already specified [machine types](https://cloud.google.com/compute/docs/machine-types?hl=en_US) that you can select from. These machine types are expansive in nature and have multiple configurations based on your primary use case of the machine.

Even then, at times you can feel limited by the offerings at times, since you might require best of both worlds, CPUs and RAM size. If you had a custom requirement for the machine size, you would always end up using extra resources on at-least one of these. For example, if one of my deployments needs are 8 CPUs and 15G RAM, the closest offering to that is n1-standard-8 which has an excess of 15G RAM that I won’t be using, yet have to pay for cause of the machine type.

With the launch of the new customize feature in the Compute Engine launch platform, now you can customize a machine as per your requirements. You can go up to 32 vCPUs and 208G of RAM. Just so you don’t go over the limits of common sense in hardware configurations, depending upon your CPU, it shows you the max amount of usable RAM.

This is one of the minor updates which bring major changes in the way we use the machines. Now you can build your own custom machine type, and launch it with Container Engine using Docker, as many iterations and copies as your need be. Increased flexibility means more power to the end developer and thus better cloud ecosystem.

> [Originally published on Medium](https://medium.com/@Vikram_Tiwari/machine-types-google-cloud-ba3486b4d747)

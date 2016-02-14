---
layout: post
title:  "API Manager — Know Your Quotas"
date:   2016-02-13 09:00:00 -0800
categories: tech update
---

Google has various services which can be accesses via API, and for each of these services to have their own API page is not sensible in the terms of maintaining access to those APIs. Hence all of them were collected and maintained in a central location. Earlier this used to be Google Code platform where you could get API keys for any of their services. But when Google Cloud Console started to become more mature it made sense to move APIs and authentication in general to be a part of the Console.

Hence in order to access an API, create a project on Cloud Console, go to API manager and there you get access keys, supporting authentication and documents for all APIs. It helps you make better decisions on choosing an API by giving you a single portal for discovery of other APIs you might not be familiar with. Also, you get the ability to test any APIs before starting integration with your app/server code.

Moreover as soon as you enable an API, monitoring for that specific API is also provided for you. This gives insights into various response based errors that you might be making while consuming API, your usage stats and potentially an insight into product features that you can put more work on. Also in the same panel you can get information about Quotas for that specific API.

Almost all of the APIs are available freely with an associated set quota to prevent misuse of the API/platform. If your applications are exceeding the quota limits, you can edit it from the panel and if the need be apply for higher quota limits. Higher quota limits might require you to pay, but you pay only for the exceeding quota over free range.

Keep calm and ❤ APIs!

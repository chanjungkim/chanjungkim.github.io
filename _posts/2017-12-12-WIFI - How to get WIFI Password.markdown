---
layout: post
title:  WIFI - How to get WIFI Password
date:   2017-12-12 09:32:00
author: C-an
categories: WIFI
---

<!-- Contents -->

It works on the Wifi that you already has been accessed before.
1. open terminal or command(cmd)

2. type **netsh wlan show profiles**
3. netsh wlan show profiles WIFI_NAME key=clear
4. 'Key Content' property is the one you want to find in the list.
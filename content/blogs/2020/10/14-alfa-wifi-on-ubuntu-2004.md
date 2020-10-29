---
title: "Alfa AWUS036ACH on Ubuntu 20.04 LTS"
date: 2020-10-14
tags: ["linux","wifi"]
author: sweemeng
---
So recently I bought a new USB WiFi device. It is the the the Alfa AWUS036ACH. There's a reason why I this, this device is using the rtl8812au which have linux drivers. 

![Alfa Wifi](https://res.cloudinary.com/dty81dwqf/image/upload/v1603976430/121679029_10158959536054319_2994756001624892964_o_hjz9zz.jpg)

But as it turns out, the rtl8812au driver on Ubuntu repo at least for 20.04 LTS don't actually work. Here's how I get this to work. 

First use the driver from Aircrack-ng, https://github.com/aircrack-ng/rtl8812au/

`git clone https://github.com/aircrack-ng/rtl8812au/` 

Then you need to edit the makefile. Do the following. 

1. Edit Makefile in the directory. Find the following line

`DRIVER_VERSION = $(shell grep "#define DRIVERVERSION" include/rtw_version.h | awk '{print $$3}' | tr -d v\")`

2. Change to, essentially add a `\` to `#` escape the character

`DRIVER_VERSION = $(shell grep "\#define DRIVERVERSION" include/rtw_version.h | awk '{print $$3}' | tr -d v\")`

Then run the following command

`sudo make dkms_install`

Reboot you're in business! Now enjoy your 5GHz wifi with 802.11ac on your ubuntu box. Also

![Speed Test!](https://www.speedtest.net/result/10245650776.png)





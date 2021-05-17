---
title: "VIM Escape Key"
date: 2021-05-17
tags: ["arduino", "embedded", "ESP32"]
image: https://res.cloudinary.com/dty81dwqf/image/upload/c_scale,h_741/v1621253185/20210312_092241_pncar6.jpg
---

{{< youtube ikUehFEQnk4 >}}

So one of the first thing I do after getting the [M5stack atom]({{<ref "blogs/2021/05/17-m5atom-matrix.md">}}). Is to build a bluetooth keyboard. I have a few idea, here I describe what I ends up getting. 

I choose to use Arduino over micropython, because ESP32 port of micropython don't have bluetooth implemented. I can potentially the Atom as a HID device, but I was hoping to use this with a small power bank. The point is not really to use this to escape vim, but to do more things say a presentation controller etc. 

With platform choosen, set up arduino based on instruction on M5Stack [docs](https://docs.m5stack.com/en/arduino/arduino_development). It should be straight forward. 

Next one is the extra library to get. In this case it is simply a bluetooth keyboard library. A google search lead me to [ESP32 BLE Keyboard library](https://github.com/T-vK/ESP32-BLE-Keyboard). This is a featureful library that can handle many thing. You can see the supported Keystroke [here](https://github.com/T-vK/ESP32-BLE-Keyboard/blob/master/BleKeyboard.h). I can't get it to send multiple character reliabily. I find out the reason later. Instruction to install also on the page. 

Last thing, the M5stack LED function is set with a C Array with height, width, and hex value for pixels. The library support scrolling too. It is easier to create the array using the provided windows app. Which I am coding this on Ubuntu, so I opt to work on the [FastLED library](http://fastled.io/) directly. 

The end result is the github [gist](https://gist.github.com/sweemeng/17d8d24549109e8d5592bfcc23018f07#file-escape-ino). The delay is to attempt to stop them to drop key to be sent. 

{{< gist sweemeng 17d8d24549109e8d5592bfcc23018f07 "escape.ino" >}}

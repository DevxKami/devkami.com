---
title: "M5Stack Atom matrix"
date: 2021-05-17
tags: ["arduino", "embedded"]
author: sweemeng
image: https://res.cloudinary.com/dty81dwqf/image/upload/c_scale,h_741/v1621253185/20210312_092241_pncar6.jpg
---
![](https://res.cloudinary.com/dty81dwqf/image/upload/c_scale,h_741/v1621253185/20210312_092241_pncar6.jpg)

I got this M5Stack module just for the fun of it. As audience of devkami knows, I am a fan of M5stack for their line of embedded development kit. It is a ESP32 SoC packaged with a set of default sensors. Also it is in a case. 

The atom is one of the smaller devkit from M5stack. This is a development kit that based on ESP32-PICO-D4. It have a 4MB Spi flash, bluetooth, wifi, 5x5 RGB LED, IR LED, a Grove connector and extra GPIO. 

You can program the device with arduino, micropython and UI Block which is M5stack version of block programming tool. They provide an arduino [library](https://github.com/m5stack/M5Atom) to make to use on arduino environment.

![GPIO](https://res.cloudinary.com/dty81dwqf/image/upload/v1621253185/20210312_092232_xzxfyi.jpg)

The GPIO you have is available at the Grove connector, which can be used for I2C, UART and just IO. Also the GPIO below the device. Because of their size, it don't have as much GPIO than a full size ESP32, but this is a very small device. 

You can see the capability using the [examples](https://github.com/m5stack/M5Atom/tree/master/examples) on the arduino library. It is a reasonably capable devkit with that size that cost RM60.  

Here is an example what I have [done](https://gist.github.com/sweemeng/17d8d24549109e8d5592bfcc23018f07#file-escape-ino), a bluetooth keyboard that close vim. 

{{< youtube ikUehFEQnk4 >}}

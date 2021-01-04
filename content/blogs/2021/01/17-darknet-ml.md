---
title: "Darknet - A deep learning tool"
date: 2021-01-17
tags: ["deep learning", "machine learning", "AI"]
image: https://res.cloudinary.com/dty81dwqf/image/upload/v1609743026/Screenshot_from_2020-12-03_20-29-59_gqpeg6.png
author: sweemeng
---
![](https://res.cloudinary.com/dty81dwqf/image/upload/v1609743026/Screenshot_from_2020-12-03_20-29-59_gqpeg6.png)

One of my favorite tools for people to dive into deep learning is Darknet. Not this [one](https://en.wikipedia.org/wiki/Darknet). This is a neural network framework in c. But despite that, this is nice in a way that it can function as an application. 


Before you use it, you need the weights file, it is linked in the [repository](https://github.com/AlexeyAB/darknet#how-to-evaluate-fps-of-yolov4-on-gpu). The command is, `darknet detector test <labels> <config> <weights> <image path>`. Example of usage is the following. 
`./darknet detector test cfg/coco.data cfg/yolov4-tiny.cfg yolov4-tiny.weights data/person.jpg`

By default it recognize 80 objects listed [here](https://github.com/AlexeyAB/darknet/blob/master/data/coco.names). It works with image and video.

While it can function as a commandline application, it is also a research tools. You can also train with your own dataset. An example of it is at my [project](https://colab.research.google.com/drive/12r6_WsIwlYiO2IvzJTt0QoK4MJgqK3Y3#scrollTo=vq1wTYmyuZ2Q), which is not about kuih anymore. 

In training darknet save the weight in a weight file, which is a binary. If you want to deploy to tflite, you may use this [tool](https://github.com/theAIGuysCode/tensorflow-yolov4-tflite/blob/master/convert_tflite.py). The converstion tools also have example to use for android app. Still trying to figure out deployment to browser. 

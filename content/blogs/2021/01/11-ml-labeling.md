---
title: "Computer Vision The Boring Part - Labeling with LabelImg"
date: 2021-01-11
tags: ["tools", "machine learning", "AI", "computer vision"]
author: sweemeng
image: https://raw.githubusercontent.com/tzutalin/labelImg/master/demo/demo3.jpg
---

So let say you want to training a neural networks to identify something in image. The first step is not actually code it. The first step is data gathering. The next step is labeling. You may also want to identify multiple objects in your image, if so you also need to label the items in the image. 

What we do in the case for object detection is, we essentially draw a square or a region and set a name. We save it to a file in text file format, can be plain text, xml, json. It will contain coordinate of the object with it's label. To do this is where various tools exist. The one I have experience is [labelImg](https://github.com/tzutalin/labelImg). 

LabelImg is a python app that use PyQT. It support Pascal VOC and YOLO Format. Different implementation of the object detection system use different format. For example [darknet](https://github.com/AlexeyAB/darknet) use YOLO format. 

To use it, is a matter of defining the objects, as described [here](https://github.com/tzutalin/labelImg#steps-yolo). And draw the square and save it. The end result is a set text files that you can use. 

But if the pretrained network need other format, there's other annotator for example [COCO Annotator](https://github.com/jsbroks/coco-annotator) for COCO format. Or you can write code to convert the annotation to one format to another. It is in a readable format for a reason. 

p.s I try to add more of the things I have done in my misadventure in deep learning. As done at [here](https://colab.research.google.com/drive/12r6_WsIwlYiO2IvzJTt0QoK4MJgqK3Y3?usp=sharing). I list various tools and steps. So more to come

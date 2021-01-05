---
title: "Computer Vision The Boring Part - Open Image Dataset"
date: 2021-01-11
tags: ["tools", "machine learning", "AI", "computer vision"]
image: https://res.cloudinary.com/dty81dwqf/image/upload/c_scale,w_1020/v1609814169/Screenshot_2021-01-05_Open_Images_Dataset_V6_rulr3l.jpg
author: sweemeng
---
![](https://res.cloudinary.com/dty81dwqf/image/upload/c_scale,w_1020/v1609814169/Screenshot_2021-01-05_Open_Images_Dataset_V6_rulr3l.jpg)

We have shown how one can create your own {{<ref "/blogs/2021/01/11-ml-labeling.md" >}}. Another way to get dataset is the [Google Open Image Dataset](https://storage.googleapis.com/openimages/web/visualizer/index.html?set=train&type=segmentation&r=false&c=%2Fm%2F015p6).

This is a dataset that have 1.5 million annotations for 600 categories. It covers some common thing that trained in YOLO. You can have a shot at trying to see if the category exist. 

To use this, I suggest that you use a tools, the one I use is the OID Toolkit, I use the [fork](https://github.com/theAIGuysCode/OIDv4_ToolKit) by The AI Guy a youtuber talking about these. The annotations is likely not in a format you want. The reason I use the fork is the creator of the fork have a converter that convert into YOLO format. 

While 600 category seems a lot, they also don't have everything. Like rice and all that. Which is why it is still worth it to learn to label your own image. Even if it is slow

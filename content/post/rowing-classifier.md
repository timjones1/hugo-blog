---
date: 2020-10-10T10:58:08-04:00
description: " "
featured_image: "images/sculler-rowing-unsplash.jpg"
tags: ["fast.ai","deep learning","Projects"]
title: "  Rowing Classifier with fast.ai"
---
I have wanted to create and deploy a toy deep learning image classification model for a while and [fasti.ai](fast.ai) gets straight into the nitty gritty in lesson 2 of their deep learning for coders course. You can adapt the code in the fast book notebooks and get a model up and running quickly and easily. I decided to create a rowing boat classifier, as it is my first DL model I kept the classification relatively simple, classifying single sculls(one person in the boat with two blades) from quads (four people rowing, each with two blades)  
my classifier performed significantly worse than the fast.ai grizzly/black/teddy bear classfier initially, this was mainly because:

 - rowing images are not well classified on Bing image search, there were a lot of incorrectly classified images and drawings / pictures of empty boats that were bringing down the accuracy scores. 

- Initial accuracy was only approx 75% between single sculls and quads, something very simple to tell the difference between by counting the number of people in the boat also by the number of oars. 

- The Azure bing image download api demo is only 7 days so I had to regroup and locate other sources of images. I subsequently managed to download approximately 400 additional images using a custom api from the fast.ai forums, and tidied them up by running a baseline model, checking the top losses, re-categorizing and deleting where appropriate. This definitely helped me get a better handle on file system manipulation in python to shoe horn the extra images into the fast.ai datablock for training.

Final accuracy was 90% on my validation set, you can upload a rowing image for classification at the site below:
[https://mybinder.org/v2/gh/timjones1/rowing-classifier/master](https://mybinder.org/v2/gh/timjones1/rowing-classifier/master?urlpath=%2Fvoila%2Frender%2Frowing_classifier.ipynb), it may take a while for the binder image to be loaded up if the site hasnt been used in a while: 


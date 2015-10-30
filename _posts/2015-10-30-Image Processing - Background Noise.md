---
layout:     	post
title:      	Image Processing - Background Noise
date:       	2015-10-30 13:25
author:     Peter Griffiths
tags:        
---

The first step in the image processing actually happens after the scan are taken by the CT  machine and they are outputted as TIFs.  Preliminary theresholding is done by the software to eliminate material densities not in the range of interest. However, there are still several problems with the data that must first be fixed before the state matrix can be created: 

![Grayscale image](https://github.com/Materials-Informatics-Class-Fall2015/MIC-Microparticle-distribution/blob/gh-pages/img/Image%20Processing/grayscale.jpg?raw=true)

Above is how the images appear when first outputted by CT software. There is low contrast between the background, the   
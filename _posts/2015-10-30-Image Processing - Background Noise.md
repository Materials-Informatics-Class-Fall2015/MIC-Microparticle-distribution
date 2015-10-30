---
layout:     	post
title:      	Image Processing - Issues
date:       	2015-10-30 13:25
author:     Peter Griffiths
tags:        
---

The first step in the image processing actually happens after the scan are taken by the CT  machine and they are outputted as TIFs.  Preliminary thresholding is done by the software to eliminate material densities not in the range of interest. However, there are still several problems with the data that must first be fixed or worked around before the state matrix can be created:

 1. Low image contrast
 2. Background noise of similar intensity to the materials of interest
 2. Empty space/orientation of image
 3. Elimination of fixtures/contaminants from image
Contrast
--------
The first major issue is the low contrast of the images. The figure below is how the images appear when first outputted by CT software. The low contrast between the background, the membrane material, and the fixturing (tape and backing plastic) makes it difficult to separate out the membrane from the other regions that are not of interest.

![Grayscale image](https://github.com/Materials-Informatics-Class-Fall2015/MIC-Microparticle-distribution/blob/gh-pages/img/Image%20Processing/grayscale.jpg?raw=true)

For grayscale images, the intensities range from 0 (black) to 255 (white).  To help with visualization, the image intensity was linearly scaled so that the lowest value is set to 0 and the highest to 255. The scaled image is shown below.

![Contrasted image](https://github.com/Materials-Informatics-Class-Fall2015/MIC-Microparticle-distribution/blob/gh-pages/img/Image%20Processing/contrast.jpg?raw=true)

While the linear scaling does not help us numerically to segment the image, it does help highlight some of the other issues.
Background Noise
----------------

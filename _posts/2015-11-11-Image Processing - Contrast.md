---
layout:     	post
title:      	Image Processing - Contrast
date:       	2015-11-11 08:55
author:     Peter Griffiths
tags:         
---

As discussed in previous post, one of the major issues has been segmenting the membrane from the fixture material in the CT images is the low contrast due to similar densities in the materials. 

![Contrast comparison for sample 5](https://github.com/Materials-Informatics-Class-Fall2015/MIC-Microparticle-distribution/blob/gh-pages/img/Intensity%20Comparison/sample5_combined.jpg?raw=true)

On the left in the figure above is a slice from one of the data sets after the background noise has been eliminated, the image has been partially closed (there are still some pores that have not been filled), and the contrast as has been increased for visibility. On the right is a plot of the intensity values associated with the blue line in the image. The intensity values range from a low of 42 associated with a pore to a high of 50 within the tape. Within each of the three solid components (membrane, tape, plastic fixture) there is a range of intensity values and since that the ranges overlap, simple thresholding cannot be used to segment the image. 

A second possible solution is to use the gradients to identify the edges associated with the transitions. For the image above there is large gradient associated with the transition to the tape. This is due to an air gap between the membrane and the tape. However, as shown in the figure below, when the tape and membrane are in contact, the gradient is smaller or not as clearly defined. In this case there are two intermediate pixels of just slightly higher intensity at the tape boundary causing a step. The gradient here is similar to the noise seen in the membrane and plastic fixturing.

![Contrast comparison for sample 5](https://github.com/Materials-Informatics-Class-Fall2015/MIC-Microparticle-distribution/blob/gh-pages/img/Intensity%20Comparison/sample5b_combined.jpg?raw=true)

A third possible solution is to look at how uniform image is from left to right. Because of the orientation of the membrane and its associated pores, there should be more variation in the intensities from the left to right as opposed to the tape and plastic fixturing which are of uniform composition. This is shown in the image below (note that the range pore intensities are more extreme since the was not completely closed).

![enter image description here](https://github.com/Materials-Informatics-Class-Fall2015/MIC-Microparticle-distribution/blob/gh-pages/img/Intensity%20Comparison/sample5c_combined.jpg?raw=true) 

This is currently the major issues we are having, so any thoughts or ideas are appreciated.
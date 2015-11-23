---
layout:     	post
title:      	Avoiding Future Imaging Problems
date:       	2015-11-22 23:08
author:     Ethan Hilton
tags:         
---

In a previous post, we discussed the difficulties we have faced in image processing to use an automated program to find the edges of each membrane.  As discussed, we eventually settled on manually marking the edges for each sample. This is, for many obvious reasons, an inefficient way to determine these edges. While the MATlab program can and will be improved itself, this post focuses primarily on how the process of creating the images can be changed to allow for the edge finding program to work more consistently.

![Fig1](https://github.com/Materials-Informatics-Class-Fall2015/MIC-Microparticle-distribution/blob/gh-pages/img/creating%20CT%20image%20post/Fig%201.jpg?raw=true)
Figure 1 - Sample setup got Micro-CT scanner
 
For the data collected in this project, the setup using a plastic holder and two-sided tape shown in Figure 1 was used. The Micro-CT scanner uses the density of and object at different points to generate the images being used for data. However, the densities of the membrane, tape, and plastic are all very similar. Therefore the objects are difficult to differentiate between in the CT scans. This leads to the edge-finding program being unable to determine where the membrane ends and the tape begins. To correct this for further data-collection after the class, we will use a setup with clamps suspending the membranes in place as seen in the diagram in Figure 2.
 
![Fig2](https://github.com/Materials-Informatics-Class-Fall2015/MIC-Microparticle-distribution/blob/gh-pages/img/creating%20CT%20image%20post/Fig%202.png?raw=true)
Figure 2 - Diagram of future scanner setup

Another issue was the inconsistency of the placement of the membranes in the CT scanner. This can be seen in the CT scans shown in Figure 3.

![Fig3](https://github.com/Materials-Informatics-Class-Fall2015/MIC-Microparticle-distribution/blob/gh-pages/img/creating%20CT%20image%20post/Fig%203.png?raw=true)
Figure 3 - Micro-CT scans 
 
This causes difficulty in creating a program that consistently finds edges as the edges are always in a different location on the image. Some of the edges are also cut off by the CT-scanner, which limits how much data can be gained from the image. By having a fixed apparatus in the center of the Micro-CT scanner platform, the CT scans will be more consistent images which will allow for quicker processing of a large amount of data.


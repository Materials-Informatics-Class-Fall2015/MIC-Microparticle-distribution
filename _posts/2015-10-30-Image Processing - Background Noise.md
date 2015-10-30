---
layout:     	post
title:      	Image Processing - Background Noise
date:       	2015-10-30 16:16
author:     Peter Griffiths
tags:         
---
As discussed in the previous image processing post, the background noise presents a problem when trying to segement the image due to the intensity level being similar to that of the membrane and variation causing the detection of false edges. A MatLab script was created to eliminate the background from the images in a systematic way which can be automated and applied to 3 dimensional images.

Thresholding
------------

The first step in this process was to create a histogram of the intensities found in the image. Since the majority of the image is the background, this helped determined the which intensities it is mainly comprised of.  As shown in the figure below, there is a very large spike in the number of voxels of intensities in the mid-30s. From interrogating the images in MatLab, it was found that the membrane typically has an intensity in the mid to high 30s. The intensities below that belong to the background and the pores in the membrane. 

![Intensity Histogram](https://github.com/Materials-Informatics-Class-Fall2015/MIC-Microparticle-distribution/blob/gh-pages/img/Image%20Processing/histogram.jpg?raw=true)

This information was used to smooth out the background to eliminate possible false edges. A lower threshold was set to the value of the largest intensity bin. All intensity values below this threshold were changed to this value. The figures below show how the background was smoothed.

![Original Intensities](https://github.com/Materials-Informatics-Class-Fall2015/MIC-Microparticle-distribution/blob/gh-pages/img/Image%20Processing/original.jpg?raw=true) 
![Lower Threshold](https://github.com/Materials-Informatics-Class-Fall2015/MIC-Microparticle-distribution/blob/gh-pages/img/Image%20Processing/thresholded.jpg?raw=true)

Edge Detection
--------------

The next step was to attempt to determine the location of the edges in the 3 dimensional image. MatLab's built in function for this will only work on 2D images, so a rountine using  the *imfilter* function was created. Edges were checked for in six directions using simple filters where the target pixel intensity was subtracted from its neighbor. The values for each direction was saved in a matrix and if the value was less than 1 is was set to zero since the background is generally of lower intensity than the solids. The six directions were then summed into a single edge matrix.

![Edges](https://github.com/Materials-Informatics-Class-Fall2015/MIC-Microparticle-distribution/blob/gh-pages/img/Image%20Processing/edges.jpg?raw=true)

False Edge Elimination
----------------------

A large number of false edges were found outside of the solids. To determine which edges were in the background and eliminate them, a binary matrix was created from the edge matrix by setting all of the values greater than 0 to 1. 

![Binary Edge Matrix](https://github.com/Materials-Informatics-Class-Fall2015/MIC-Microparticle-distribution/blob/gh-pages/img/Image%20Processing/edgesBinary1.jpg?raw=true)

If a voxel identified as an edge is actually on a surface, there should also be voxels around it identified as an edges. Depending upon the size of a search radius around a voxel, a minimum number of edge voxels should be found if it is actually on a surface. For example if a voxel is on a flat surface and you search the voxels with in the 3x3x3 cube centered on the voxel, 8 additional suface voxel should be found. This principle was used to eliminate the false edges.

Starting with a search radius of 1, the number of edge voxels surrounding a target edge voxel was found. If the sum was less than 4, the edge voxel was eliminated from the binary edge matrix.

![Edge search](https://github.com/Materials-Informatics-Class-Fall2015/MIC-Microparticle-distribution/blob/gh-pages/img/Image%20Processing/maskedAverage.jpg?raw=true)

This process was repeated increasing the search radius, until no edges were eliminated. It was then decreased incrementally down to 1 to eliminate voxels near actual surfaces (due to the large number of edges found inside the solids, if the search radius is large enough it will not eliminate voxels just off the surface).

![Edge search final](https://github.com/Materials-Informatics-Class-Fall2015/MIC-Microparticle-distribution/blob/gh-pages/img/Image%20Processing/maskedAverage2.jpg?raw=true)

Closing
-------

With the edges confined to the solids (a few
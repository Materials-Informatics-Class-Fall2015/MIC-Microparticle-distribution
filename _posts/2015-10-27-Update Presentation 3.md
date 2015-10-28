---
layout:     	slide
title:     	Update Presentation 3
date:      	2015-10-27 21:42
author:     	Peter Griffiths and Ethan Hilton

theme:		solarized # default/beige/blood/moon/night/serif/simple/sky/solarized
trans:		default # default/cube/page/concave/zoom/linear/fade/none

horizontal:	</section></section><section markdown="1" data-background="http://ahmetcecen.github.io/project-pages/img/slidebackground.png"><section markdown="1">
vertical:		</section><section markdown="1">
---
<section markdown="1" data-background="http://ahmetcecen.github.io/project-pages/img/slidebackground.png"><section markdown="1">
## {{ page.title }}
### Image Processing

<hr>

#### {{ page.author }}

#### {{ page.date | | date: "%I %M %p ,%a, %b %d %Y"}}

{{ page.horizontal }}
<!-- Start Writing Below in Markdown -->
In our last presentation...
![pic1.1](https://github.com/Materials-Informatics-Class-Fall2015/MIC-Microparticle-distribution/blob/gh-pages/img/Pres3%20pics/Picture2.2.jpg?raw=true)
<!-- End Here -->
{{page.vertical}}
<!-- Start -->
![pic1.1](https://github.com/Materials-Informatics-Class-Fall2015/MIC-Microparticle-distribution/blob/gh-pages/img/Pres3%20pics/Picture2.0.jpg?raw=true)
<!-- Stop -->

{{page.vertical}}
<!-- Start -->
![pic1.1](https://github.com/Materials-Informatics-Class-Fall2015/MIC-Microparticle-distribution/blob/gh-pages/img/Pres3%20pics/Picture2.1.jpg?raw=true)
<!-- Stop -->

{{page.vertical}}
<!-- Start -->
![pic1.1](https://github.com/Materials-Informatics-Class-Fall2015/MIC-Microparticle-distribution/blob/gh-pages/img/Pres3%20pics/Picture2.3.jpg?raw=true)

<!-- Stop -->

{{page.vertical}}
<!-- Start -->

##About the Data
5 datasets (membranes)

 - ~50 grayscale TIFs
 - Each pixel = 6.2 microns
 - Each image is 6.2 microns (one pixel) apart
	 - Combine into one 3D matrix

<!-- Stop -->

{{page.horizontal}}
<!-- Start -->

###Difficulties Processing Data

 - Background scatter
 - Empty space
 - Fixture touches sample
 - Low contrast!
	 - Small range of intensities between:
		 - membrane
		 - background
		 - fixture
 - Difficulty detecting edges

{{ page.vertical }}
Before and after linear contrasting

![img](https://github.com/Materials-Informatics-Class-Fall2015/MIC-Microparticle-distribution/blob/gh-pages/img/Pres3%20pics/Picture3.1.jpg?raw=true)

{{ page.horizontal }}
##Intensity Range Histogram
![img](https://github.com/Materials-Informatics-Class-Fall2015/MIC-Microparticle-distribution/blob/gh-pages/img/Pres3%20pics/Picture4.jpg?raw=true)
{{ page.horizontal }}
##Thresholding

 - Set limits to upper and lower values
 - Helps smooth data in background
	 - Less edges detected

![img](https://github.com/Materials-Informatics-Class-Fall2015/MIC-Microparticle-distribution/blob/gh-pages/img/Pres3%20pics/Picture5.1.jpg?raw=true)
{{ page.vertical }}

![img](https://github.com/Materials-Informatics-Class-Fall2015/MIC-Microparticle-distribution/blob/gh-pages/img/Pres3%20pics/Picture5.2.jpg?raw=true)
{{ page.horizontal }}

##Edge Detection

 - Found edges in all three directions
 - Summed gradient values
 - Create separate binary edge matrix

![img](https://github.com/Materials-Informatics-Class-Fall2015/MIC-Microparticle-distribution/blob/gh-pages/img/Pres3%20pics/Picture6.1.jpg?raw=true)

{{ page.vertical }}

![img](https://github.com/Materials-Informatics-Class-Fall2015/MIC-Microparticle-distribution/blob/gh-pages/img/Pres3%20pics/Picture6.2.jpg?raw=true)

{{ page.horizontal }}

##Noise Elimination

 - Sum of edge in spherical kernel around voxel
 - Threshold based upon surface value (R = 1, <5)
 - Update binary edge matrix
 - Increase then decrease radius

![img](https://github.com/Materials-Informatics-Class-Fall2015/MIC-Microparticle-distribution/blob/gh-pages/img/Pres3%20pics/Picture7.1.jpg?raw=true)

{{ page.vertical }}

![img](https://github.com/Materials-Informatics-Class-Fall2015/MIC-Microparticle-distribution/blob/gh-pages/img/Pres3%20pics/Picture7.2.jpg?raw=true)

{{ page.horizontal }}

##Closing around Solids

 - Large amount of edges found in solids
 - Closing image to highlight solids
 - Working on statistical means to determine proper radius

![img](https://github.com/Materials-Informatics-Class-Fall2015/MIC-Microparticle-distribution/blob/gh-pages/img/Pres3%20pics/Picture8.1.jpg?raw=true)

{{ page.vertical }}

![img](https://github.com/Materials-Informatics-Class-Fall2015/MIC-Microparticle-distribution/blob/gh-pages/img/Pres3%20pics/Picture8.2.jpg?raw=true)

{{ page.horizontal }}

##Masking Image

 - Use binary matrix to mask data
 - Highlight the solids (membrane and fixture)

![img](https://github.com/Materials-Informatics-Class-Fall2015/MIC-Microparticle-distribution/blob/gh-pages/img/Pres3%20pics/Picture9.0.jpg?raw=true)

{{ page.horizontal }}

##Next Steps
Issues with some of the data files...

 - Orientation
 - Cropping
 - Containments

![img](https://github.com/Materials-Informatics-Class-Fall2015/MIC-Microparticle-distribution/blob/gh-pages/img/Pres3%20pics/Picturez10.1.jpg?raw=true)

{{ page.vertical }}

##Other issues to address

 - Filter out Fixtures
 - Phase identification
 - Corrections for curvature

![img](https://github.com/Materials-Informatics-Class-Fall2015/MIC-Microparticle-distribution/blob/gh-pages/img/Pres3%20pics/Picturez10.2.jpg?raw=true)

{{ page.horizontal }}

#Thank you!
 Please look for the "Presentation as Post for Comments" post to add comments or ask questions! 

##[Print]({{ site.url }}{{ site.baseurl }}{{ page.url }}/?print-pdf#)

##[Back]({{ site.url }}{{ site.baseurl }})

</section></section>

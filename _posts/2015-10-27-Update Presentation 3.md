---
layout:     	slide
title:     	Update Presentation 3
date:      	2015-10-27 21:42
author:     	Peter Griffiths and Ethan Hilton

theme:		sky # default/beige/blood/moon/night/serif/simple/sky/solarized
trans:		default # default/cube/page/concave/zoom/linear/fade/none

horizontal:	</section></section><section markdown="1" data-background="http://ahmetcecen.github.io/project-pages/img/slidebackground.png"><section markdown="1">
vertical:		</section><section markdown="1">
---
<section markdown="1" data-background="http://ahmetcecen.github.io/project-pages/img/slidebackground.png"><section markdown="1">
## {{ page.title }}

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
## About the Data

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

{{ page.horizontal }}

#[Print]({{ site.url }}{{ site.baseurl }}{{ page.url }}/?print-pdf#)

#[Back]({{ site.url }}{{ site.baseurl }})

</section></section>

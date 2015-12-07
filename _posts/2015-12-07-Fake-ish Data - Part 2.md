---
layout:     	post
title:      	Fake-ish Data - Part 2
date:       	2015-12-07 13:39
author:     Peter Griffiths
tags:         
---

Since only two of the five data sets gave satisfactory results after image segmentation, as shown below, additional sets are needed to finish the data pipeline. The challenge is creating fake data that is realistic enough to be meaningful and that will provide insight into how to process real sets. 
![Sample 1 State Matrix](https://github.com/Materials-Informatics-Class-Fall2015/MIC-Microparticle-distribution/blob/gh-pages/img/Fake%20Data/Sample1_state.jpg?raw=true)
![Sample 5 State Matrix](https://github.com/Materials-Informatics-Class-Fall2015/MIC-Microparticle-distribution/blob/gh-pages/img/Fake%20Data/Sample5_state.jpg?raw=true)
As discussed in earlier posts, we already have code that will determine particle locations based roughly on processed parameters during casting and particle sizes based on batch statistics. How do we create realistic pores? The easiest solution is to use the pore data from the two "good" sets, samples 1 and 5, after they have been realigned and trimmed.
![Sample 1 pores](https://github.com/Materials-Informatics-Class-Fall2015/MIC-Microparticle-distribution/blob/gh-pages/img/Fake%20Data/Sample1_pores.jpg?raw=true)
![Sample 5 pores](https://github.com/Materials-Informatics-Class-Fall2015/MIC-Microparticle-distribution/blob/gh-pages/img/Fake%20Data/Sample5_pores.jpg?raw=true)
The previous code was modified to determine particle locations in 3D and a MatLab script was created to vary the volume fraction of particles and the height ratio (H/h) of the die. Particles were placed such that they were contained with in the polymer matrix of the membrane. If a particle location was found that was within a pore, the height of the particle was held and the location with in the depth and width of the membrane was varied randomly until it was in a valid location (the first iteration of the code found all new coordinates and ended up giving an almost even distribution of particles since the pores are mainly in the center of the membrane). 
![Case 1 Sample 1](https://github.com/Materials-Informatics-Class-Fall2015/MIC-Microparticle-distribution/blob/gh-pages/img/Fake%20Data/Case1Sample1_state.jpg?raw=true)
![Case 16 Sample 1](https://github.com/Materials-Informatics-Class-Fall2015/MIC-Microparticle-distribution/blob/gh-pages/img/Fake%20Data/Case16Sample1_state.jpg?raw=true)
The results are new data sets with varying particle distributions that we can use for principle component analysis.
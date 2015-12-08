---
layout:     	post
title:      	Executive Summary
date:       	2015-12-08 12:33
author:     	Materials Innovation
tags:         result
---

## Background

Polymer mirco/nano particle composite membranes and films have multiple applications ranging from water filtration to catalysts to paints. The particle distributions within these membranes can have critical importance to their properties and performance.
Slot-die extrusion is one industrial scale process that is commonly used to manufacture films. The benefit of this method is that the film thickness is a function only of the mass flow rate of the solution to be coated and the substrate velocity on to which it is coated. The die geometry and material properties determine the range of velocities which defect free film can be manufactured and the main thrust of research is usually at improving the maximum speed of production.

For more information on the motivation behind this project, read our Background post [here](http://materials-informatics-class-fall2015.github.io/MIC-Microparticle-distribution/2015/09/08/background/ "Background").

![Fig1](https://github.com/ehilton3/Microparticle-distribution/raw/gh-pages/img/Slot-die.png?raw=true "Slot Die Diagram")
##### Fig. 1 - Slot Die Diagram

## Project Plan

The goal of this project is to establish a process-structure link between the geometric settings during casting to the final micro particle distribution of polymer particle composite membranes manufactured using slot-die extrusion. 
The first step is to design an experiment in which the die geometry is changed to see the impact upon particle distributions. To keep the initial experiments simple only a single parameter will be changed the gap height of die from the substrate (H). We plan on varying the gap height while keeping the film thickness (h), substrate velocity (U), volumetric flow rate (Q’) constant along with the fluid and the particle size and volumetric loading. The ratio between the film thickness and gap height (h/H) has a large influence on the velocity flow profile underneath the die and consequently the equilibrium position of particles in the fluid. 

For more information on our initial Project Plan, read our post [here](http://materials-informatics-class-fall2015.github.io/MIC-Microparticle-distribution/2015/09/08/Project_Plan/ "Project Plan").
You can also read about our Project Workflow [here](http://materials-informatics-class-fall2015.github.io/MIC-Microparticle-distribution/2015/09/26/Mowrkflow/ "Workflow").

## Process

Cellulous acetate (CA) dissolved into N-Methyl-2-pyrrolidone (NMP) is a commonly used solution in the casting of water filtration membranes. It has several advantages for this experimental application as there are only two materials, it is easily synthesized, processed, and cured, and has a high enough consistency index to limit particle migration after casting.
The slot-die process allows for a high control of the film thickness by changing parameters such as the volumetric flow rate, substrate speed, and gap height as described in the process plan. However, there are restrictions on the parameters due to physical limitations resulting in films with a high amount of defects. The region in which defect-free production can occur is known as the casting window and is shown below. The experimental data collected for this project all occurred within this window.

![Fig 2](https://github.com/ehilton3/Microparticle-distribution/blob/gh-pages/img/velocity_profile.png?raw=true)
###### Fig. 2 - Casting Window

For more information about the Material Synthesis, read the post [here](http://materials-informatics-class-fall2015.github.io/MIC-Microparticle-distribution/2015/09/22/Material_Synthesis/ "Material Synthesis").
For more information about the Process Parameters, read the post [here](http://materials-informatics-class-fall2015.github.io/MIC-Microparticle-distribution/2015/09/29/Process/ "Process - The P in PSP").

## Setbacks and Responses

Our setback had two major set-backs we had to overcome.

The first set-back came in the form of a severe delay in data collection as we waited on Micro-CT images. To make the most of this time, we prepared ourselves to evaluate the eventual data by creating “fake” data using MATLab files that randomly distributed particles in a matrix of a membrane with some forced biases towards the top or bottom of the membrane based on fluid dynamics. An example of one of these fake images is shown below (black=membrane, white=particles).

![Fig 3](https://github.com/Materials-Informatics-Class-Fall2015/MIC-Microparticle-distribution/raw/gh-pages/img/Presentation2/h_H_050_state.jpg?raw=true)
###### Fig. 3 - Simulated Data

We then ran two-point statistics on the fake data to ensure our files were generating accurate results in a hope to streamline data analysis once we received data. However, we ran into our second setback when we finally received data. This setback is discussed in the next section.

To read more about creating fake data, read the post [here](http://materials-informatics-class-fall2015.github.io/MIC-Microparticle-distribution/2015/10/15/Waiting/ "Working While We Wait").
To read more about validating the fake data with two-point statistics, read the post [here](http://materials-informatics-class-fall2015.github.io/MIC-Microparticle-distribution/2015/10/15/Validation/ "Validation of 'Fake' Data").

## Image Processing

Image process became the large bulk of time was spent on image processing as the Micro-CT scan images were not as clear as we hoped. The contrast between the membrane and the background, and the fixture was very low. This lead to a long process of image cleaning attempting to use a variety of image-processing techniques to go from the original in Figure 4 to the cleaned image in Figure 5 below.

![Fig 4](https://github.com/Materials-Informatics-Class-Fall2015/MIC-Microparticle-distribution/raw/gh-pages/img/Image%20Processing/grayscale.jpg?raw=true)
###### Fig. 4 - Raw CT Image (before processing)

![Fig 5](https://github.com/Materials-Informatics-Class-Fall2015/MIC-Microparticle-distribution/raw/gh-pages/img/Painting%20post/Fig%201.png?raw=true)
###### Fig. 5 - CT Image after Processing

To read more on our many attempts in image-processing, read the posts [here](http://materials-informatics-class-fall2015.github.io/MIC-Microparticle-distribution/2015/10/30/Image%20Processing%20-%20Issues/ "Image Processing - Issues"), [here](http://materials-informatics-class-fall2015.github.io/MIC-Microparticle-distribution/2015/10/30/Image%20Processing%20-%20Background%20Noise/ "Image Processing - Background Noise"), and [here](http://materials-informatics-class-fall2015.github.io/MIC-Microparticle-distribution/2015/11/11/Image%20Processing%20-%20Contrast/ "Image Processing - Contrast") along with some methods on how to avoid some of these image processing problems [here](http://materials-informatics-class-fall2015.github.io/MIC-Microparticle-distribution/2015/11/22/FutureImaging/ "Avoiding Image Processing Problems").

## Pushing Ahead

Eventually, we had to come to the realization that we would not get perfect images from the experimental data. We therefor conceded to marking the edges of the manually (read about this process [here](http://materials-informatics-class-fall2015.github.io/MIC-Microparticle-distribution/2015/11/22/Painting/ "Manual Edge Detection")) as shown below. This allowed us to finally get to usable images from the experimental data.

![Fig. 6](https://github.com/Materials-Informatics-Class-Fall2015/MIC-Microparticle-distribution/blob/gh-pages/img/Painting%20post/Fig%205.png?raw=true)
##### Fig. 6 - Processed Image with Manuallt Drawn Edges

However, only two of the data sets produced high-quality images. We therefore had to make more fake data. This time, the simulated data was modeled off the experimental data collected and altered to allow for a more robust data-set. The formation of this simulated data is discussed [here](http://materials-informatics-class-fall2015.github.io/MIC-Microparticle-distribution/2015/12/07/Fake-ish%20Data%20-%20Part%202/ "Fake-ish Data Pt. 2").

## Two-Point Statistics and PCA

Using the usable experimental data and the simulated data, we conducted two-point statistics and developed a PCA. The PC scores are used to develop a Process-structure linkage between the process parameters of the slot-die extrusion and the structure of the thin-filmed membrane.
More detail on this PCA and P-S linkage is described in the post [here](http://materials-informatics-class-fall2015.github.io/MIC-Microparticle-distribution/2015/12/08/PCA/ "PCA").


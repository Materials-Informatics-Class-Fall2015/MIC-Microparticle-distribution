---
layout:     	post
title:      	Material Synthesis
date:       	2015-09-22 12:00
author:       Peter Griffiths
tags:         
---

Cellulous acetate (CA) dissolved into N-Methyl-2-pyrrolidone (NMP) is a commonly used solution in the casting of water filtration membranes. It has several advantages for this experimental application as there are only two materials, it is easily synthesized, processed, and cured, and has a high enough consistency index to limit particle migration after casting. There is however limited swelling of the membrane during the phase inversion curing process (~30%) which may affect the particle locations. A 20% concentration of CA to NMP by mass (mass fraction MF) was selected as previous research has been conducted with this concentration and the material properties are already known.

$$ MF = \frac{m_{CA}}{m_{CA}+m_{NMP}} $$

Glass microparticles were selected as they are relatively inexpensive, inert, non-toxic, and have a density difference large enough from CA to allow for CT imaging. Also importantly, they will not dissolve in NMP! The size of the particles was limited by the resolution of the micro CT imaging system (~5 micron) and a range of 9 to 22 micron particles was selected to ensure imaging would be possible. 

The volume fraction of particles to the solution (VF) was selected the particle to particle interaction effects on particle locations and to avoid substantial changes in the fluid properties. The ratio of the particle diameter (D) to the average distance between particles (d) was approximated by assuming a tetrahedral distribution of particles with in the solution:

$$ VF = \frac{V_g}{V_g+V_{CA}+V_{NMP}}{} $$
$$ \frac{d}{D} = \frac{1}{6}\sqrt{\frac{3}{2}}\left(\frac{8\pi}{VF}\right)^\frac{1}{3} $$

The small the ratio, the larger the chance of particle interaction.  However as this ratio increases, the number of particles in a given sample of a membrane decreases and the amount of samples and images needed to be processed to obtain a representative data set increases. A volume fraction of 0.05% glass (d/D ~ 8.5) was selected as it was thought to be good balance.

250 mL of the CA-NMP-glass polymer microparticle composite solution was synthesized by slowly dissolving the CA into the NMP utilizing a magnetic stirrer one third of the mass of CA at a time. The microparticles were added to the solution after the first third of CA was added.

$$ m_{CA} = \frac{\rho_{NMP}V_{NMP}}{1-MF} $$
$$ m_{g} = \frac{V_{CA}+V_{NMP}}{\rho_g(1-VF)} $$

The result:

![NMP 20% CA with 0.05% glass microparticles by volume](https://github.com/Materials-Informatics-Class-Fall2015/MIC-Microparticle-distribution/blob/gh-pages/img/NMP_20CA_glass.jpg?raw=true)

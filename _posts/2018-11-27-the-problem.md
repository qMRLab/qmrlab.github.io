---
layout: post
title:  "The Problem"
author: Agah
categories: [ jekyll ]
image: assets/images/the_problem.png
featured: true
hidden: false
---
![alt text]({{ site.baseurl }}/assets/images/problem_fig.png)

[In a recent post](https://qmrlab.org/jekyll/2018/10/02/hello-world.html), we briefly mentioned about the promise of qMRI in supplementing conventional MR images with objective qMaps. In this pursuit of biomarkers, there is an important pit stop where we need to set some standards for qMRI by dealing with several sources of variability. Leaving this pit stop without being fully prepared means falling behind in the pursuit of the full potential of qMaps.

One variability source is differences between qProcessing implementations that are intended for the same qRecipe. At a recent talk in Montreal, Camille Maumet (@cmaumet) described those differences as analytical variability, a term that accounts for variations in i) algorithm, ii) software, iii) software version and iv) computational environment in which the software operates. Clearly, analytical variability may give rise to some discrepancies between the qMaps that are supposed to be the same.

Another potential source of variability are differences between MRI scanners. This is a tough multi-faceted problem including vendor-specific variations in hardware/software design and model variant differences within the same vendor. Although there is no direct solution to this problem, mitigation is possible by creating consensus qData acquisition protocols and using global calibration schemes.  

There is a common saying that identifying the problem is half the solution. Yet, we cannot even identify the problem without raising the issue of sharing qMRI methods. Currently most of the methods are developed in-house, making it much more challenging to reproduce and compare them.

Bottom line, lack of standardization is the flat tire of qMRI.

PREVIOUS: [Hello World!](https://qmrlab.org/jekyll/2018/10/02/hello-world.html)
NEXT: The Solution

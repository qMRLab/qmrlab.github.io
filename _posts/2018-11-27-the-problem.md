---
layout: post
title:  "The Problem"
author: Agah
categories: [ jekyll ]
image: /assets/images/the_problem.png
excerpt: In the previous post, we briefly mentioned about the promise of qMRI in supplementing conventional MR images with objective qMaps. Now we are shifting gears to talk about "the problem".
featured: true
hidden: false
---
[In a recent post](https://qmrlab.org/jekyll/2018/10/02/hello-world.html), we briefly discussed the promise of qMRI in supplementing conventional MR images with objective qMaps. In our pursuit of objective biomarkers, there is an important pit stop where we need to set some standards for qMRI and deal with several sources of variability. Leaving this pit stop without being fully prepared means falling behind in our pursuit.

<center> <img src="{{ site.baseurl }}/assets/images/problem_fig.png"/> </center>

A major source of variability stems from the differences between qProcessing implementations that are intended for the same qRecipe. At a recent talk in Montreal, Camille Maumet (@cmaumet) described those differences as analytical variability, a term that accounts for variations in i) algorithm, ii) software, iii) software version and iv) computational environment in which the software operates. Clearly, analytical variability may give rise to some discrepancies between the qMaps that are supposed to be the same.

Another potential source of variability are differences between MRI scanners. This is a tough multi-faceted problem including vendor-specific variations in hardware/software design and model variant differences within the same vendor. Although there is no direct solution to this problem, mitigation is possible by creating consensus qData acquisition protocols and using global calibration schemes.  

There is a common saying that identifying the problem is half the solution. Yet, we cannot even identify the problem without raising the issue of sharing qMRI methods. Currently most of the methods are developed in-house, making it much more challenging to reproduce and compare them.

Bottom line, lack of standardization is the flat tire of qMRI.

PREVIOUS: [Hello World!](https://qmrlab.org/jekyll/2018/10/02/hello-world.html) <br />
NEXT: The Solution

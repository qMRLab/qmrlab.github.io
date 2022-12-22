---
layout: post
title:  "DNA sequencing & qMRI, Part 2: But What About Data Standards?"
author: Nadia
image: /assets/images/DNA_qMRI_part2_00-min.png
excerpt: "The analogy between genetics and MRI will continue on a more metaphorical level as we dive into the qMRI-BIDS data standard, the development of which was led by Dr. Agâh Karakuzu."
featured: false
hidden: false
---


In [part 1](https://qmrlab.org/2022/12/20/DNA-qMRI-part-1.html), we made an analogy between DNA sequencing and magnetic resonance imaging (MRI) to drive the point that despite sharing many statistical tools, geneticists and neuroimagers study fundamentally different information: genetic data stores _quantitative_ information (e.g. chain of base pairs derived from DNA sequencing), whereas conventional MRI data stores _qualitative_ information  (e.g. unitless intensity values derived from conventional MRI). To this end, quantitative MRI (qMRI) is an adaptation of MRI that enables scientists to work with the quantitative information stored in MR images _with units_. In part 2 below, we will continue the parallel between genetics and MRI on a more _metaphorical_ level.

MRI depends on the sampling of a signal that originates from protons that exist on a scale of around 10-15 m (Antognini et al., 2013)), yet each voxel is on the order of 1mm. qMRI data acquisition and processing therefore demands high methodological rigor. However, before thinking of ways to leverage this technique and resolve many debilitating diseases and perennial philosophical questions once and for all, you need to lay out the less glamorous details: how do you name and organize your data files in order to minimize errors, facilitate data sharing and optimize reproducibility?

<center> <img src="{{ site.baseurl }}/assets/images/DNA_qMRI_part2_01-min.png" style="border: 3px solid red"/> </center>**Fig. 1** – The components of a qMRI method by [Dr. Agâh Karakuzu](https://agahkarakuzu.github.io/) ([OHBM Educational](https://agahkarakuzu.github.io/talk/talk15/)).

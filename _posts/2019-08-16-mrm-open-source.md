---
layout: post
title:  "On the open source landscape of MRM"
author: Mathieu
image: assets/images/qmrlab.png
excerpt: Most studies that use B1 maps do not use the raw maps; instead, they are typically filtered during a pre-processing step to reduce effects like noise and minor artifact, as the B1 distribution in tissue is expected to be a smoothly varying function. However, there appears to be no clear community consensus 
featured: false
hidden: true
---

<div style="text-align: justify"> 
<p>

Being involved in several open source projects (<a href="https://github.com/neuropoly/qMRLab" target="_blank">qMRLab</a>, <a href="https://github.com/neuropoly/axondeepseg" target="_blank">AxonDeepSeg</a>) and initiatives dealing with open science in publishing (<a href="http://neurolibre.conp.ca" target="_blank">NeuroLibre</a>, Canadian Open Neuroscience Platform), I was curious to know what the current landscape of open source software/analysis sharing was in my own field - MR engineering for medical applications. I decided to investigate what the landscape of open source sharing was in one of the main journals of my field, Magnetic Resonance in Medicine (MRM). Note that this isn’t a scientific study in itself, it was just a mini side project that evolved out of curiosity.

</p>

<p>

The broad questions that I was interested in were the following:

<ol>
    <li> What % of MRM papers claim to share code/data/scripts ? </li>
    <li> If they share code, what coding languages do they use ? </li>
    <li> Where do they typically host their code/data ? </li>
    <li> What’s the completeness of what they shared (e.g. ranging from being able to reproduce paper figures to never having delivered on their promise to share their code). </li>
</ol>

</p>

<p>
<center><b>Details of analysis</b></center>
</p>

<p>
<ul>
    <li> Downloaded all papers published in Magnetic Resonance in Medicine from January to November 2019 (December issue not out yet). </li>
    <li> Ran <a href="https://drive.google.com/file/d/18ISwiCmh1IVsLToFX-9SiFAYU92OhbdD/view" target="_blank">a script</a> to search for all papers that contained one of a list of keywords that may hint at containing open-source code/data. </li>
    <li> Compiled all the papers that matched keywords into a <a href="https://docs.google.com/spreadsheets/d/162YoF-tsJHcua2xgZ84AvY7sH4B3SBYAwimxSl9jWi8/edit?usp=sharing" target="_blank">Google Sheet file</a>. </li>
    <li> Manually looked in each paper to see if code/data was actually shared. </li>
    <li> Parsed through these and the external links to see if they (1) shared code/data/scripts, (2) see which languages the codes used, and (3) where they hosted their code/data/scripts. </li>
</ul>
</p>

<p>
<center><b>Broad overview of results</b></center>
</p>

<p>
<center><img src="assets/images/mrm_1.png"></center>
</p>

</div> 


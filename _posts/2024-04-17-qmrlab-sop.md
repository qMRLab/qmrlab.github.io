---
layout: post
title:  "qMRLab Standard Operating Procedures series"
author: Mathieu
categories: [ jekyll ]
image: /assets/images/qmrlab.png
featured: false
hidden: true
---

<div style="text-align: justify"> 

<h1>Introduction</h1>

<p>

This qMRLab standard operating procedure (SOP) series is intended to be a step-by-step guide on how to process quantitative MRI data using qMRLab. In this blog post, we'll guide you through installing qMRLab, and upcoming blog posts will provide SOPs for specific qMRLab modules.

</p>

<p>
In addition, below is a video tutorial on how to use qMRLab and many of its features (eg., simulations, data fitting, quality checking, etc) using the quantitative MT moule. It was presente at the 2022 ISMRM conference.
</p>

<iframe width="560" height="315" src="https://www.youtube.com/embed/V3LMOTuwMs4?si=PCu_QiKMwt-3Zv1f" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

<h1>Software Requirements</h1>

<h2>Minimum requirements</h2>
<ul>
    <li>MATLAB (version 2020b or earlier, see reason here)</li>
    <li>qMRlab</li>
</ul>

<h2>Optional</h2>
<ul>
    <li>Python (version 3.x) - preferably installed using Anaconda or Miniconda</li>
    <li>dcm2niix</li>
    <li>FSL</li>
</ul>


<h1>Installing qMRLab</h1>

<p>
qMRLab [1,2] is an open-source quantitative MRI software that can be used to process a large range of quantitative MRI maps (T1, T2, MTR, MTsat, MP2RAGE, etc), and is developed mainly by the NeuroPoly Lab.
</p>

<p>
Because it’s an open-source software, it’s continuously in development, so the packaged releases on the GitHub repository or main website may not contain the latest features needed, or may contain bugs that were since fixed.
</p>

<p>
For this project, you should download the qMRLab version linked here. It is a compressed zip file; if it doesn’t extract by itself after the download, please do so manually using the appropriate tool for your operating system and then move the qMRLab folder wherever you’d like it stored. You should also rename it to simply “qMRLab”.
</p>

<p>
Following this step, you need to ensure that a previous version of qMRLab has not been saved in MATLAB. 
</p>

<ol>
    <li>Open MATLAB.</li>
    <li>In the Home toolbar tab, navigate to the Environment section and click Set Path.</li>
    <li>Scroll through the list of directories that are in MATLAB’s path (i.e. directories where it can “see” the files for use in your MATLAB session), and select all the ones associated with previous qMRLab installations if there are any.</li>
    <li>Click Remove.</li>
    <li>A new window will appear asking if you want to save this as default. This choice is up to you, we recommend that you click Yes but this may not be appropriate for everyone.</li>
    <li>Now, open the qMRLab directory where you’ve stored it after downloading the correct version and extracting it.</li>
    <li>In the Command Window, type startup and press enter/return.</li>
    <li>qMRLab is now in your path, however the next time you open MATLAB, it won’t be. You can choose to do this each time you use qMRLab (open the directory and run startup), or you can add it to your default path. To do so, navigate to Set Path in the Environment section of the Home tab, and click Save.</li>
    <li>If you did the last step, now anytime you want to use qMRLab you’ll be able to immediately after opening MATLAB.</li>
    <li>To start qMRLab, type qMRLab in the Command Window and wait for the graphical user interface (GUI) to load.</li>
</ol>

</div> 

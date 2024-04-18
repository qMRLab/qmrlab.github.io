---
layout: post
title:  "SOP series: Introduction to qMRLab and installation"
author: Mathieu
categories: [ jekyll ]
image: /assets/images/qmrlab.png
featured: true
hidden: false
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
    <li><a href="https://matlab.mathworks.com">MATLAB</a> (version 2020b or earlier, see reason <a href ="https://github.com/qMRLab/qMRLab/issues/419">here</a>)</li>
    <li><a href="https://github.com/qMRLab/qMRLab">qMRlab</a></li>
</ul>

<h2>Optional</h2>
<ul>
    <li><a href="https://www.python.org/">Python</a> (version 3.x) - preferably installed using <a href ="https://anaconda.org">Anaconda</a> or <<a href ="https://docs.anaconda.com/free/miniconda/index.html">Miniconda</a></li>
    <li><a href="https://www.nitrc.org/plugins/mwiki/index.php/dcm2nii:MainPage#Download">dcm2niix</a></li>
    <li><a href="https://fsl.fmrib.ox.ac.uk/fsl/fslwiki/FslInstallation">FSL</a></li>
</ul>


<h1>Installing qMRLab</h1>

<p>
qMRLab [1,2] is an open-source quantitative MRI software that can be used to process a large range of quantitative MRI maps (T1, T2, MTR, MTsat, MP2RAGE, etc), and is developed mainly by the <a href="http://neuro.polymtl.ca">NeuroPoly Lab</a>.
</p>

<p>
Because it’s an open-source software, it’s continuously in development, so the packaged releases on the <a href="https://github.com/">GitHub</a> repository or main website may not contain the latest features needed, or may contain bugs that were since fixed.
</p>

<p>
For convenience, users not already familiar with <a href="https://git-scm.com/">git</a> you should download the qMRLab version linked <a href="https://github.com/qMRLab/qMRLab/archive/refs/heads/master.zip">here</a>. It is a compressed zip file; if it doesn’t extract by itself after the download, please do so manually using the appropriate tool for your operating system and then move the qMRLab folder wherever you’d like it stored. You should also rename it to simply “qMRLab”.
</p>

<p>
Following this step, you need to ensure that a previous version of qMRLab has not been saved in MATLAB. 
</p>

<ol>
    <li>Open MATLAB.</li>
    <li>In the <b>Home</b> toolbar tab, navigate to the <b>Environment</b> section and click <b>Set Path</b>.
    <figure>
      <center> <img src="{{ site.baseurl }}/assets/images/qmtlab_sop_1.png" alt="Step 2"></center>
      <figcaption><i>Step 2</i></figcaption>
    </figure>
    </li>
    <li>Scroll through the list of directories that are in MATLAB’s path (i.e. directories where it can “see” the files for use in your MATLAB session), and select all the ones associated with previous qMRLab installations if there are any.
    <figure>
      <center> <img src="{{ site.baseurl }}/assets/images/qmrlab_sop_2.png" alt="Step 3"></center>
      <figcaption><i>Step 3</i></figcaption>
    </figure>
    </li>
    <li>Click <b>Remove</b>.</li>
    <li>A new window will appear asking if you want to save this as default. This choice is up to you, we recommend that you click <b>Yes</b> but this may not be appropriate for everyone.
    <figure>
      <center> <img src="{{ site.baseurl }}/assets/images/qmrlab_sop_3.png" alt="Step 5"></center>
      <center><figcaption><i>Step 5</i></figcaption></center>
    </figure>
    </li>
    <li>Now, open the qMRLab directory where you’ve stored it after downloading the correct version and extracting it.
    <figure>
      <center> <img src="{{ site.baseurl }}/assets/images/qmrlab_sop_4.png" alt="Step 6"></center>
      <figcaption><i>Step 6</i></figcaption>
    </figure>
    </li>
    <li>In the <b>Command Window</b>, type <b>startup</b> and press <b>enter/return</b>.
     <figure>
      <center> <img src="{{ site.baseurl }}/assets/images/qmrlab_sop_5.png" alt="Step 7"></center>
      <figcaption><i>Step 7</i></figcaption>
    </figure>   
    </li>
    <li>qMRLab is now in your path, however the next time you open MATLAB, it won’t be. You can choose to do this each time you use qMRLab (open the directory and run startup), or you can add it to your default path. To do so, navigate to <b>Set Path</b> in the <b>Environment</b> section of the <b>Home</b> tab, and click <b>Save</b>.
     <figure>
      <center> <img src="{{ site.baseurl }}/assets/images/qmrlab_sop_6.png" alt="Step 8"></center>
      <figcaption><i>Step 8</i></figcaption>
    </figure>  
    </li>
    <li>If you did the last step, now anytime you want to use qMRLab you’ll be able to immediately after opening MATLAB.</li>
    <li>To start qMRLab, type <b>qMRLab</b> in the <b>Command Window</b> and wait for the graphical user interface (GUI) to load.
     <figure>
      <center> <img src="{{ site.baseurl }}/assets/images/qmrlab_sop_7.png" alt="Step 10"></center>
      <figcaption><i>Step 10</i></figcaption>
    </figure>  
    </li>
</ol>

<ol>
    <li>Karakuzu A, Boudreau M, Duval T, Boshkovski T, Leppert I, Cabana J-F, et al. qMRLab: Quantitative MRI analysis, under one umbrella. J Open Source Softw. 2020;5: 2343.</li>
    <li>Cabana J-F, Gu Y, Boudreau M, Levesque IR, Atchia Y, Sled JG, et al. Quantitative magnetization transfer imagingmadeeasy with qMTLab: Software for data simulation, analysis, and visualization. Concepts Magn Reson Part A Bridg Educ Res. 2015;44A: 263–277.</li>
</ol>

</div> 

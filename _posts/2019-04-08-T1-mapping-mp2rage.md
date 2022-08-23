---
layout: post
title:  "Relaxometry Series: MP2RAGE"
author: Mathieu
image: /assets/images/mp2rage_t1.png
excerpt: Dictionary-based MRI techniques capable of generating T1 maps are increasing in popularity, due to their growing availability on clinical scanners, rapid scan times, and fast post-processing computation time, thus making quantitative T1 mapping accessible for clinical applications. Generally speaking, dictionary-based
featured: true
hidden: false
---

<div style="text-align: justify"> 
<p>

Below is an interactive tutorial about Magnetization Prepared 2 Rapid Acquisition Gradient Echoes (MP2RAGE) T<sub>1</sub> mapping. Unlike our previous two blog posts on T<sub>1</sub> mapping, the plots generated in this one are not powered by <a href="https://github.com/neuropoly/qMRLab" target="_blank">qMRLab</a>; instead, they are generated using the open-source MP2RAGE code provided by Jose Marques (original author of MP2RAGE work) which is (<a href="https://github.com/JosePMarques/MP2RAGE-related-scripts" target="_blank">available on GitHub here</a>). In the near future, we hope to integrate this work as a qMRLab module; you can follow the progress on our <a href="https://github.com/qMRLab/qMRLab/issues/255" target="_blank">GitHub issue</a> or <a href="https://github.com/qMRLab/qMRLab/blob/master/CONTRIBUTING.md" target="_blank">contribute to this feature</a> yourself!

</p>

<p>
Just like previous tutorials, most figures are generated with <a href="https://plot.ly/python/" target="_blank">Plot.ly</a> – you can play with them by hovering your mouse over the data, zooming in (click and drag) and out (double click), moving the sliders, and changing the drop-down options. To view the code that was used to generate the figures in this blog post, hover your cursor in the top left corner of the frame that contains the tutorial and click the checkbox "All cells" in the popup that appears.

</p>

<p>

A Jupyter Notebook version of this blog post is also available through MyBinder, and can be viewed <a href="https://mybinder.org/v2/gh/qMRLab/t1_notebooks/master?filepath=mp2rage_blog%2FMP2RAGE.ipynb" target="_blank">here</a>. There you can modify the code, change the figures, and regenerate the html that was used to create the tutorial below. It is powered by <a href="https://vatlab.github.io/sos-docs/" target="_blank">Script of Scripts (SoS)</a>, allowing us to process the data in MATLAB/Octave and plot the figures with Plot.ly using Python, all within the same Jupyter Notebook.

</p>

<p>

This work was supported by the <a href="http://conp.ca" target="_blank">Canadian Open Neuroscience Platform (CONP)</a> initiative, the <a href="https://www.rbiq-qbin.qc.ca/" target="_blank">Quebec Bio-Imaging Network (QBIN)</a>, and the <a href="https://www.icm-mhi.org/en/foundation" target="_blank">Montreal Heart Institute Foundation</a>.

</p>

<p>

<b> For best user experience with interactive tutorials, we recommend using a laptop or a desktop computer.</b>

</p>


</div> 

<iframe src="https://qmrlab-blogs.s3.ca-central-1.amazonaws.com/mp2rage/MP2RAGE.html" width="100%" height="8500px" style="border:none;"></iframe>

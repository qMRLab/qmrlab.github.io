---
layout: post
title:  "T1 mapping: Inversion Recovery"
author: Mathieu
author: Mathieu
categories: [ jekyll ]
image: /assets/images/t1_temp.png
excerpt: To make the excerpt appear, we either write the excerpt in the post properties (excerpt property) or it will take the first 25 words from the post.
featured: true
hidden: true
---



<div class=blog_body>
<p style="text-align:justify;">
Widely considered the gold standard for T<sub>1</sub> mapping, the inversion recovery technique estimates T<sub>1</sub> values by fitting the signal recovery curve acquired at different delays after an inversion pulse (180°). In a typical inversion recovery experiment (<a href="#fig1">Figure 1</a>), magnetization at thermal equilibrium is inverted using a 180° RF pulse. After the longitudinal magnetization recovers through spin-lattice relaxation for predetermined delay (“inversion time”, TI), a 90° excitation pulse is applied, followed by a readout imaging sequence (typically a spin-echo or gradient-echo readout) to create a snapshot of the longitudinal magnetization state at that TI. Inversion recovery was first developed for NMR in the 1940s (Hahn 1949; Drain 1949), and the first T<sub>1</sub> map was acquired using a saturation-recovery technique (90° as a preparation pulse instead of 180°) by (Pykett and Mansfield 1978). Some distinct advantages of inversion recovery is its large potential range of signal change (up to 2M<sub>0</sub>) and an insensitivity to pulse sequence parameter imperfections (Stikov et al. 2015). Despite its proven robustness at measuring T<sub>1</sub>, inversion recovery is scarcely used in practice, because conventional implementations requires repetition times (TRs) on the order of 2 to 5 T<sub>1</sub> (Steen et al. 1994), making it challenging to acquire whole-organ T<sub>1</sub> maps in a clinically feasible time. Nonetheless, it is continuously used as a reference measurement during the development of new techniques, or when comparing different T<sub>1</sub> mapping techniques, and several variations of the inversion recovery technique have been developed, making it practical for some applications.
</p>
</div>

<div class=figure_caption>
<center>
<b style="text-align:justify;">
<a name="fig1" style="color:black;">Figure 1.</a>  Pulse sequence of an inversion recovery experiment.
</b>
</center>
</div>

<p>
<center><img src="ir_pulsesequences.png" style="width:640px;height:auto;"></center>

#Signal Modelling

The steady-state longitudinal magnetization of an inversion recovery experiment can be derived from the Bloch equations for the pulse sequence
{θ<sub>180</sub> – TI – θ<sub>90</sub> – (TR-TI)}, and is given by:

<p style="text-align:justify;">
<center><img src="equation1.png" style="width:auto;height:50px;margin-bottom: 50px;margin-top: 50px;"></center>
</p>

<p style="text-align:justify;">
where M<sub>z</sub> is the longitudinal magnetization prior to the θ<sub>90</sub> pulse. If the in-phase real signal is desired, it can be calculated by multiplying Eq. 1 by <i>k</i>·sin(θ<sub>90</sub>)·exp(-TE/T2), where <i>k</i> is a signal constant. This general equation can be simplified by grouping together the constants for each measurements regardless of their values (i.e. at each TI, same TE and θ<sub>90</sub> are used) and assuming an ideal inversion pulse:
</p>

<p style="text-align:justify;">
<center><img src="equation2.png" style="width:auto;height:50px;margin-bottom: 50px;margin-top: 50px;"></center>
</p>

<p style="text-align:justify;">
where the first three terms and the denominator of Eq. 1 have been grouped together into the constant C. If the experiment is designed such that TR is long enough to allow for full relaxation of the magnetization (TR > 5T<sub>1</sub>), we can do an additional approximation by dropping the last term in Eq. 2:
</p>

<p style="text-align:justify;">
<center><img src="equation3.png" style="width:auto;height:50px;margin-bottom: 50px;margin-top: 50px;"></center>
</p>

<p style="text-align:justify;">
The simplicity of the signal model described by Eq. 3, both in its equation and experimental implementation, has made it the most widely used equation to describe the signal evolution in an inversion recovery T<sub>1</sub> mapping experiment. The magnetization curves are plotted in <a href="#fig2">Figure 2</a> for near T<sub>1</sub> values of three different tissues in the brain. Note that in many practical implementations, magnitude-only images are acquired, so the signal measured would be proportional to the absolute value of Eq. 3.
</p>
</div>

<div class="figure_caption">
<center>
<b style="text-align:justify;">
<a name="fig1" style="color:black;">Figure 1.</a>  Pulse sequence of an inversion recovery experiment.
</b>
</center>
</div>
<iframe frameborder="0" style="-webkit-transform:scale(0.5);-moz-transform-scale(0.5);" scrolling="no" src="//plot.ly/~TommyBoshkovski/14.embed" seamless></iframe>

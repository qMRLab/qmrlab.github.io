---
layout: post
title:  "DNA Sequencing & qMRI Part 1: Base Pairs Are Quantitative, MRI Is Not."
author: Nadia
image: /assets/images/DNA_qMRI-00-cover.png
excerpt: "Quantitative magnetic resonance imaging (qMRI) is a medical imaging technique that lends itself very well to metaphors: it has previously been compared to a wide range of ideas and objects, from jelly beans and symphonic orchestras, to alphabet soups and Bento boxes."
featured: true
hidden: false
---


Quantitative magnetic resonance imaging (qMRI) is a medical imaging technique that lends itself very well to metaphors: it has previously been compared to a wide range of ideas and objects, from [jelly beans](https://agahkarakuzu.github.io/talk/talk15/) and [symphonic orchestras](https://www.youtube.com/watch?v=67GKiK3iFr0), to [alphabet soups and Bento boxes](https://youtu.be/eaaHY_nl7tA). Continuing on with this tradition, we will now compare qMRI to something less unconventional in a science context: deoxyribonucleic acid (DNA) sequencing.


<center> <img src="{{ site.baseurl }}/assets/images/DNA_qMRI-01.png"/> </center>


## A conventional analogy to genetics.

There are many parallels to be made between neuroimaging and its sister field of genetics. Most neuroimagers are quite familiar with genetics as their training has exposed them, at the very minimum, to an overview of how to go from DNA to protein. And those with a heavy neuroscience background have likely had the misfortune to memorize a ghastly amount of transcription factors, DNA polymerases and ribosomal subunits to meet some course requirements. Whether overtly or not, most biological sciences are entrenched in genetic ideas and, elaborating on this further, we would like to make a point about how neuroimaging data science has drawn inspiration from the Human Genome Project (HGP) (Watson & Jordan, 1989). 

<center> <img src="{{ site.baseurl }}/assets/images/DNA_qMRI-02.png"/> </center>

Spanning from 1990 to 2003, this global initiative was largely driven by a [post-Cold War fear of nuclear fallout](https://web.ornl.gov/sci/techresources/Human_Genome/project/herac2.shtml) and the resulting incentive to understand what radiation can do to our genome (L. Hood & Rowen, 2013). Importantly, the HGP pioneered the development of DNA sequencing technology. The late 1980s saw a significant milestone in the field of genetics, as scientists were able to direct the outputs of their DNA sequencing applications directly to a computer (L. E. Hood et al., 1987). In 2003, the completion of the HGP was announced (Collins et al., 2003), followed by the publication of the first euchromatic human genome in 2004 (International Human Genome Sequencing Consortium, 2004). It thus took almost 15 years and $3 billion to complete this first euchromatic reference genome (L. Hood & Rowen, 2013). Today, it is possible for anyone to obtain a whole-genome sequence of the same fidelity for less than $200 and with a wait time of 6 weeks (ps: Razib Khan has some [valuable insights](https://razib.substack.com/p/so-you-want-to-test-your-dna) into why _you_ may want to do this).

The incredible advances made in the field of genetics have naturally led to a need for scientists to learn how to manage large, multidimensional datasets and use advanced statistical tools. For example, between 2005 and 2020, over 4,300 genome-wide association studies (GWAS) have been published, linking over 55,000 different loci to nearly 5,000 diseases and traits (Loos, 2020). It is thus unsurprising that this era of rapid advancement has also brought with it a need for geneticists to develop new skills in data management and analysis.
  
<img src="{{ site.baseurl }}/assets/images/DNA_qMRI-03.png"/>**Fig. 1** – From the Human Genome Project [Overview Slides](https://www.genome.gov/human-genome-project).

## And here comes quantitative MRI.

Needless to say, the tremendous breakthroughs in genetics have captured the imagination of scientists in all fields, which may explain how we have arrived at using big data approaches in neuroimaging: magnetic resonance imaging (MRI) allows us to curate large-scale, high-resolution in vivo datasets that are ripe for computational analyses!

Just as the Human Genome Project (HGP) is a landmark in the field of genetics, the more recent Human Connectome Project (HCP) (Van Essen et al., 2013) is well-known in neuroscience. In fact, the similarity in their names is unlikely to be coincidental and suggests that the two projects aim to produce the same output for two different biological systems. However, despite their shared nomenclature, these two initiatives are pursuing distinct objectives. Whilst the goal of the HGP was to sequence the entire genome (≈3 billion base pairs) for _one reference human_, the goal of the HCP is to advance our understanding of brain connectivity through the collection and release of genetic, behavioral and high-resolution MRI data in _as many human subjects as possible_. In fact, a more accurate comparison to the HGP could be the recent mapping of the entire _C. elegans_ worm connectome (Cook et al., 2019), which contains fewer than 400 neurons – which is significantly less than the 86 billion neurons of the human brain (Herculano-Houzel, 2012).

<img src="{{ site.baseurl }}/assets/images/DNA_qMRI-04.png"/>**Fig. 2** – Top: adult hermaphrodite _C. elegans_ nervous system from Fig. 1 b) of _Cook et al., 2019_ ([source](https://www.nature.com/articles/s41586-019-1352-7)); bottom left: from the [Human Connectome Project](https://www.nih.gov/news-events/news-releases/human-connectome-project-marks-its-first-phase); bottom right: album cover of one the [greatest bands](https://www.muse.mu/).

Thus, for neuroimaging data scientists, the high-quality human MRI data of the HCP is of greater interest than electron micrographs of worms. The HCP is a massive undertaking, and the healthy young adult dataset alone includes data from 1,200 subjects, most of whom were scanned at 3T to produce anatomical images of human brains with an isotropic resolution of 0.7 mm. This means that each subject has over 60 million (_(260 mm / 0.7 mm) x (311 mm / 0.7 mm) x (311 mm / 0.7 mm)_) features, or voxels. To handle ≈ 1,200 observations (n) of ≈ 60 million features (p), we often borrow statistical tools from geneticists, who have experience working with large whole-genome sequence datasets and handling the pernicious p >> n problem. However, it is important to remember that the conventional MRI data we work with is qualitative, as the voxels we use only encode unitless intensity values in an arbitrary grayscale range. This makes it challenging to identify biological variability in the data and distinguish it from noise (Novikov et al., 2018; Weinberger & Radulescu, 2016).

Geneticists are fortunate to work with truly quantitative information, as DNA can be reduced to sequences of base pairs: adenine (A), thymine (T), guanine (G), and cytosine (C). Not only do geneticists have the advantage of working with the "building blocks" (or “bits”) of biology, but these building blocks are so well-organized that they are the same across all 30 trillion cells in the human body (Sender et al., 2016). Furthermore, only about 0.1% of the 3 billion base pairs in the human genome vary among individuals (Van Essen et al., 2013), which provides a high level of consistency in genetic data. This point is even raised in the original HCP release paper itself (Van Essen et al., 2013): _“Hence, high sensitivity to sequence variants is critical for being able to characterize individual genomic differences and to relate these differences to phenotypes of interest. In contrast, the accuracy with which human brain connectivity can be quantitatively assessed is much lower than for genome sequencing, but the degree of individual variability is far greater.”_


<img src="{{ site.baseurl }}/assets/images/DNA_qMRI-05.png"/>**Fig. 3** – Structure of DNA ([Source](https://theory.labster.com/structure-dna/)).

Consequently, neuroimaging data scientists often apply tools developed for consistent and quantitative genetic data to data that is not only qualitative, but also highly variable across individuals. This can be a difficult task, but significant efforts are being made to address the lack of quantitative and ground truth information in neuroimaging. Some researchers believe that with sufficiently large sample sizes, reproducible workflows, and advanced data engineering and analysis tools (Glatard et al., 2015; Kiar et al., 2020; Lindquist, 2020), it will be possible to differentiate biological variability from noise. Others are working on mapping histological data – often regarded as the ground truth information that conventional MRI is lacking – to neuroimaging data (Amunts et al., 2013). 

<img src="{{ site.baseurl }}/assets/images/DNA_qMRI-06.png"/>**Fig. 4** – Diagram of the parallel between DNA sequencing and qMRI; images from the [National Human Genome Research Institute](https://www.theguardian.com/science/2022/mar/31/first-complete-gap-free-human-genome-sequence-published) (top left), DNA image from [here](https://www.gettyimages.com/detail/photo/blue-chromosome-dna-and-gradually-glowing-flicker-royalty-free-image/1297146235?adppopup=true) (bottom left), brain images from Karakuzu et al. 2022 (top center, top right).


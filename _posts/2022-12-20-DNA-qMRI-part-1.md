---
layout: post
title:  "DNA Sequencing & qMRI Part 1: Base Pairs Are Quantitative, MRI Is Not."
author: Nadia
image: /assets/images/DNA_qMRI-00-cover.png
excerpt: "Quantitative magnetic resonance imaging (qMRI) is a medical imaging technique that lends itself very well to metaphors: it has previously been compared to a wide range of ideas and objects, from jelly beans and symphonic orchestras, to alphabet soups and Bento boxes."
featured: false
hidden: false
---

![alt_text]({{ site.baseurl }}/assets/images/DNA_qMRI-01.png "image_tooltip")

## A conventional analogy to genetics.

Quantitative magnetic resonance imaging (qMRI) is a medical imaging technique that lends itself very well to metaphors: it has previously been compared to a wide range of ideas and objects, from [jelly beans](https://agahkarakuzu.github.io/talk/talk15/) and [symphonic orchestras](https://www.youtube.com/watch?v=67GKiK3iFr0), to [alphabet soups and Bento boxes](https://youtu.be/eaaHY_nl7tA). Continuing on with this tradition, we will now compare qMRI to something less unconventional in a science context: deoxyribonucleic acid (DNA) sequencing. There are many parallels to be made between neuroimaging and its sister field of genetics. Most neuroimagers are quite familiar with genetics as their training has exposed them, at the very minimum, to an overview of how to go from DNA to protein. And those with a heavy neuroscience background have likely had the misfortune to memorize a ghastly amount of transcription factors, DNA polymerases and ribosomal subunits to meet some course requirements. Whether overtly or not, most biological sciences are entrenched in genetic ideas and, elaborating on this further, we would like to make a point about how neuroimaging data science has drawn inspiration from the Human Genome Project (HGP) (Watson & Jordan, 1989). 

![alt_text]({{ site.baseurl }}/assets/images/DNA_qMRI-02.png "image_tooltip")

Spanning from 1990 to 2003, this global initiative was largely driven by a [post-Cold War fear of nuclear fallout](https://web.ornl.gov/sci/techresources/Human_Genome/project/herac2.shtml) and the resulting incentive to understand what radiation can do to our genome (L. Hood & Rowen, 2013). Importantly, the HGP pioneered the development of DNA sequencing technology. The late 1980s saw a significant milestone in the field of genetics, as scientists were able to direct the outputs of their DNA sequencing applications directly to a computer (L. E. Hood et al., 1987). In 2003, the completion of the HGP was announced (Collins et al., 2003), followed by the publication of the first euchromatic human genome in 2004 (International Human Genome Sequencing Consortium, 2004). It thus took almost 15 years and $3 billion to complete this first euchromatic reference genome (L. Hood & Rowen, 2013). Today, it is possible for anyone to obtain a whole-genome sequence of the same fidelity for less than $200 and with a wait time of 6 weeks (ps: Razib Khan has some [valuable insights](https://razib.substack.com/p/so-you-want-to-test-your-dna) into why _you_ may want to do this).

The incredible advances made in the field of genetics have naturally led to a need for scientists to learn how to manage large, multidimensional datasets and use advanced statistical tools. For example, between 2005 and 2020, over 4,300 genome-wide association studies (GWAS) have been published, linking over 55,000 different loci to nearly 5,000 diseases and traits (Loos, 2020). It is thus unsurprising that this era of rapid advancement has also brought with it a need for geneticists to develop new skills in data management and analysis.

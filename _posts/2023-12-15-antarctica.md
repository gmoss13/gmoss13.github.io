---
title: "Inferring Antarctic Ice Shelves' Melting Rates using Simulation-Based Inference"
layout: post
date: 2023-12-15 17:26
# tag: icy
image: /assets/images/projects/sbi_ice_problem_setting.pdf
headerImage: false
projects: true
hidden: false
description: "Antarctic Ice Shelves and SBI"
category: project
author: gmoss
externalLink: false
---

![Screenshot]({{ site.url }}/assets/images/projects/sbi_ice/problem_setting.png)

Antarctic ice shelves are the floating ice masses surrounding the Antarctic continent, and are crucial in predicting the stability of Antarctica under climate change over the coming centuries. Unfortunately, we can't measure the melting rate of the ice where it is in contact with the ocean directly. But, we know how this melting rate affects the dynamics of ice flow, and as a result, the ice shelf's internal structure - which is something we can measure! So in summary, we have an unobserved parameter (melting rates) affecting a measurable outcome (internal structure) through a complex simulation process. Sounds like a job for <b> Simulation Based Inference</b> :smile:

![Screenshot]({{ site.url }}/assets/images/projects/sbi_ice/sbi_schematic.png)

This project was incredibly rewarding, as it combined the implementation of a sufficiently fast simulator to apply simulation-based inference, as well as extensive data processing that is often involved with geoscientific data. However, in the end, we managed to obtain melting rates consistent with uniquely available independent measurements for Ekström Ice Shelf in Antarctica. [Check out the full paper](www.cambridge.org/core/journals/journal-of-glaciology/article/simulationbased-inference-of-surface-accumulation-and-basal-melt-rates-of-an-antarctic-ice-shelf-from-isochronal-layers/F2D04200CC8792E0217B7FE0E42B31BA) in the Journal of Glaciology and the [code](https://github.com/mackelab/sbi-ice), or drop me an email if you have any questions!

___

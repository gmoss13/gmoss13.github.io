---
title: "sbi reloaded: a toolkit for simulation-based inference workflows"
layout: post
date: 2024-10-18 19:00
# tag: sbi
image: /assets/images/projects/sbi_software/sbi_workflow.png
headerImage: false
projects: true
hidden: false
description: "sbi software"
category: project
author: gmoss
externalLink: false
---

<script
  src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML"
  type="text/javascript">
</script>


Scientists and engineers often rely on complex and stochastic computational simulators
to describe the dynamics of their system - whether it is the electrochemical
interactions of neurons, the merging of black holes, or anything in between. These 
simulators allow us to give inputs (parameters) describing the system, to make
predictions (observations) about them. Practitioners often want to ask the opposite 
question. If we observe an experimental measurement - which parameters of the simulator
could explain it, and *how likely* are the parameters to have produced this observation?
**Simulation-based inference (SBI)** describes a family of methods which uses algorithms
from probabilistic machine learning to answer such questions *for any simulator*. 
However, probabilistic machine learning research may not be accessible to domain
scientists and engineers, and building ML workflows to apply SBI methods can be a 
significant time investment for practitioners. This is where the 
[***sbi*** toolkit](https://github.com/sbi-dev/sbi) comes in - we implement and maintain
the newest SBI methods, with a user-friendly interface to enable practitioners to solve 
challenging inference problems for their computational simulators, **without** also 
having to become ML experts.

![Screenshot]({{ site.url }}/assets/images/projects/sbi_software/sbi_workflow.png)

The ***sbi*** toolbox has been actively maintained and upgraded since its creation
in 2021. It is used in many scientific works
([including my own]({% post_url 2023-12-15-antarctica %})). I have had the privilege to 
work in the large and diverse team led by [Jan Teusen](https://janfb.github.io/) and
[Michael Deistler](https://michaeldeistler.github.io/) in maintaining, but also
extending the toolkit with new features. These new feature include score-based and 
flow-based models for likelihood and posterior estimation, new diagonstic tools of 
inference calibration, and extensive tutorials. We continue to work on improving this 
toolkit and helping scientists and engineers in a variety of disciplines use it to 
empower their research. We recently published an updated 
[software paper](https://joss.theoj.org/papers/10.21105/joss.07754), as well as a 
[practical guide](https://arxiv.org/abs/2508.12939) which help practioners navigate the 
growing field of simulation-based inference.

___
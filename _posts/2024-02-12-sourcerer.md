---
title: "Sourcerer: Maximum Entropy Source Distribution Estimation"
layout: post
date: 2024-02-12 19:00
# tag: sourcerer
image: /assets/images/projects/sbi_ice_problem_setting.pdf
headerImage: false
projects: true
hidden: false
description: "Sourcerer: Maximum Entropy Source Distribution Estimation"
category: project
author: gmoss
externalLink: false
---

<script
  src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML"
  type="text/javascript">
</script>


Inference is the common task of finding the posterior distribution over parameters consistent with a specific outcome (or set of outcomes) from a model. What about the case where you have several outcomes, all coming from the same model, <b> but from different parameters</b>? We want to find a distribution over the parameters that is consistent <b>with all observations</b>. This is the <b>Source Distribution Estimation Problem</b>, also commonly known as Empirical Bayes (EB).

More concretely, we have a simulator model taking parameters $$\theta$$ and generates potential outcomes $$x$$ by sampling from the implicit likelihood $$p(x\vert\theta)$$. We are given a distribution $$p_0(x)$$ (or samples from this distribution), and want to find a distribution $$s(\theta)$$ which satisfies

$$s^{\#}(x) = \int p(x\vert\theta)s(\theta)d\theta = p_0(x)$$

for all $$x$$.

The problem? The distribution $$s(\theta)$$ is not unique! There can be more than one distribution $s(\theta)$ which is "pushed forward" to the same distribution $$p_0(x)$$.

![Screenshot]({{ site.url }}/assets/images/projects/sourcerer/entropy_figure.png)

We resolve this by tackling the maximum entropy source distribution - which we show to be unique. We argue this is intuitively a good target, as the maximum entropy distribution is guaranteed to cover all feasible parameter configurations, and so we don't miss any "good" parameters. In practice, we approximate the maximum entropy distribution by training a variational distribution to minimize a convex combination of the entropy, and a distance measure between the real data distribution $$p_0(x)$$ and the estimated pushforward $$s^{\#}(x)$$:


$$\mathcal{L} = \lambda H (s) - (1-\lambda) D_{\text{SW}}(s^{\#},p_0)$$

Where $$D_{\text{SW}}$$ is the <it>Sliced-Wasserstein Distance</it>, which is a scalalbe measure of distance between distributions coming from optimal transport (see, e.g., [Kimia Nadjahi's excellent thesis](https://theses.hal.science/tel-03533097/file/106842_NADJAHI_2021_archivage.pdf)). 

With these components, we are able to estimate source distributions in a fast and sample-based fashion! Best of all, we see that adding the entropy term to the loss gives us <b>higher entropy distributions for free</b> - we don't pay a price for our higher entropy distributions in terms of how close our simulations are to the dataset. This is true even for complex, high-dimensional simulators such as the [Hodgkin-Huxley](https://en.wikipedia.org/wiki/Hodgkin%E2%80%93Huxley_model) model from neuroscience.

![Screenshot]({{ site.url }}/assets/images/projects/sourcerer/HH_figure.png)

If this sounds interesting to you, feel free to get in touch! Also, check out [the full paper](https://arxiv.org/abs/2402.07808) and the great [blog post](https://transferlab.ai/pills/2024/sourcerer-maximum-entropy-distribution-estimation/) about it from TransferLab!

___
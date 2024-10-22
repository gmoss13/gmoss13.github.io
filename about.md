---
title: About
layout: page
---
![Profile Image]({% if site.external-image %}{{ site.picture }}{% else %}{{ site.url }}/{{ site.picture }}{% endif %})

Hi there, I'm Guy! I am a final-year PhD candidate at the University of Tübingen, and part of the International Max Planck Research School for Intelligent Systems (IMPRS-IS). I am supervised by <a href="https://www.mackelab.org/">Prof. Jakob Macke</a> and <a href="https://uni-tuebingen.de/en/fakultaeten/mathematisch-naturwissenschaftliche-fakultaet/fachbereiche/geowissenschaften/arbeitsgruppen/geo-und-umweltnaturwissenschaften/geo-und-umweltnaturwissenschaften/oberflaechennahe-geophysik/geophysik/">Prof. Reinhard Drews</a>. My research is at the intersection between computational simulators, typically developed by scientists and engineers, and machine learning methods that can be used to enhance and analyze these simulators. 

I am interested in a lot more things than I can write down here, but I am always happy to chat about:
<ul>
	<li>(Neural) Density Estimation</li>
	<li>Bayesian Inference</li>
	<li>Generative Modeling</li>
	<li>Optimal Transport</li>
</ul>


<h2>Cool blogs</h2>
In lieu of completing the perpetual item on my to-do list to write my own blog, here are some cool blog posts I really like and would like to advertize!

<ul>
	<li><a href="https://www.cs.toronto.edu/~duvenaud/cookbook/">The Kernel cookbook by David Duvenaud</a> is a short and sweet intuition to choosing kernels for Gaussian Processes. If you've ever worked with Gaussian Processes, you've probably seen the fundamental text by Rasmussen and Williams. However, when it comes to actually using GPs, choosing the kernel can be very hard! This blog post is a great starting point.</li>
	<li><a href="https://deep-and-shallow.com/2021/03/20/mixture-density-networks-probabilistic-regression-for-uncertainty-estimation/">Mixture Density Networks by Manu Joseph</a> - the first idea for a neural network to estimate a nontrivial probability distribution is: <em>"What if we try to stick some Gaussian blobs on this distribution?"</em>. But what loss should you train, and how should you parameterize the network? This blog post provides a guide with code to implementing your own mixture of Gaussians approximation of a distribution, more formally known as a <b>Mixture Density Network</b>.</li>
	<li><a href="https://astroautomata.com/blog/simulation-based-inference/">Tutorial on simulation-based inference by Miles Cranmer</a>. At the <a href="https://sbi-dev.github.io/sbi/latest/">sbi</a> team, we try to provide a lot of documentation on our functionalities. However, for a quick and effective summary with clean animations and a cool example in astronomy, I strongly recommend Miles' blog. Although, there have been some cool developments in SBI since this blog was written, and you can follow the <a href="https://x.com/sbi_devs">sbi developers</a> for up-to-date information &#128513;</li>
</ul>


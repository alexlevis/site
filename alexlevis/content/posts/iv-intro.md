+++
title = "TODO: An introduction to instrumental variables"
date = 2022-07-18T00:00:00-04:00
tags = ["causal"]
draft = false
author = "Alex Levis"
+++

A focus of my postdoctoral research is on using _instrumental
variables_ for causal inference. There is a large literature in
economics and epidemiology on this topic, but much of the terminology
is scattered, and the underlying causal and statistical frameworks
vary from place to place. My goal in this post is to give an overview
of the salient features of an instrumental variable (IV), and discuss
when (and perhaps how) IVs can be used to aid in causal inference
research.


## Motivation: a trial with non-compliance {#motivation-a-trial-with-non-compliance}

Suppose we run a randomized controlled trial to study the
effectiveness of a drug for some disease. For each subject, we flip a
coin to determine whether they are in the drug arm, or are to receive
a placebo pill --- let \\(Z \in \\{0,1\\}\\) indicate the arm of
randomization, with \\(Z = 1\\) if a subject was randomized to the drug
arm, and \\(Z = 0\\) if randomized to the placebo arm.
\\[\frac{\sum\_{i=1}^n Z\_i Y\_i}{\sum\_{i=1}^n Z\_i}\\]
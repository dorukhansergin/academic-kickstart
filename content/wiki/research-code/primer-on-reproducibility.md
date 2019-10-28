---
title: A Primer on Reproducibility in Science
linktitle: A Primer on Reproducibility in Science 
toc: true
type: docs
date: "2019-10-27T00:00:00+01:00"
draft: false
menu:
  example:
    parent: 1. Preliminaries
    weight: 5

# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 5



---

## Reproducibility in Science

What makes science so powerful? If I had to give one answer to this, I'd say *reproducibility*.

Walter Hendrik Gustav Lewin—a phsyics professor at MIT—is probably most famous in the public for his pendulum experiment show he does in his lectures.
I put the video below:
{{<youtube xXXF2C-vrQE>}}

The video is aptly named: Trust in Physics.
What he basically does is to __reproduce__ a well-known experiment that demonstrates the conservation of mechanical energy.
His explanation of the experiment might be trivial but is at the center of our discussion:

> If I release that ball from a certain height, then, that ball can never come back to a point where the height is any larger.

The underlying theme here is what is called _determinism_. 
That is, science can tell us, to a certain degree of confidence (enough that he stays alive), what results a system will produce given well described experimental setting and conditions.
It is this degree of certainty, that helps us builds skyscrapers and bridges that don't collapse on itself or treat certain illnesses with high rates of success.

Making their experiments reproducible is one of the major responsibilities of any researcher. 
Unfortunately, reproducibility is becoming less and less of a concern in the past few decades, which threats the credibility of science terribly.
I'd argue that the publish or perish culture and the ever increasing reliance on external funds is the major reason why this is the case but I rather not go into the details of this here.

Nature recently released [a special on the challenges irreproducible research](https://www.nature.com/collections/prbfkwmwvz) where every article in the collection should be read and actively discussed by anyone who does research on a daily basis.
This is a shared concern among all fields of science, including computer science and thus machine learning.
In this section I'd like to focus on the implications of irreproducibility in machine learning (ML) and data science (DS), then, try to convince the reader that the ethical and practical reasons to be reproducible is strong.
Many of the topics I will cover in this course what I call __Research Code and Data Management__ has direct implications to reproducibility, that's why I wanted to have a dedicated motivation section in the preliminaries.

## Reproducibility in Machine Learning and Data Science

Let's consider the already classic [GAN paper](https://papers.nips.cc/paper/5423-generative-adversarial-nets.pdf) from Goodfellow *et al*.
In a nutshell, they propose a new generative model that they claim to produce better results than previous ones.
Apart from theoretical results, they support this claim using tables and figures which summarize the results of their experiments.
Indeed; Table 1, Figure 2 and Figure 3 are central to the discussion in Section 5 which directly aims to convince the reader to use GANs from now on to do generative tasks, at least as opposed to other models mentioned in Table 1.

Here is the important question: why would the reader believe them?
How can I trust GANs as much as Prof. Lewin trusts the pendulum not smashing his face?
The GAN paper, given that it was published in 2014, is a somewhat good example of reproducibility in ML.
Let's talk about the reasons why:

* The Experiments section in the paper clearly cites the public datasets used for this study. A researcher can follow the citations to download their own copy of the dataset from a source that we can trust will not be altered over time.
* Ian Goodfellow released the code in [a public GitHub repo](https://github.com/goodfeli/adversarial). The Readme of the repo addresses some of the reproducibility issues.
* One can at least walkthrough the code to understand the experimental setup the team used to create the tables and figures.

He hints the bitter truth in the Readme, though:

>We are an academic lab, not a software company, and have no personnel devoted to documenting and maintaing this research code.

I could tell many ways that this repo could be better but it is also true that most researchers don't have the know-how or resources to keep their results absloutely reproducible.

Recently, attempts to hold researchers accountable to reproducibility has been voiced more loudly in the ML community. 
I can cite the reproducibility efforts of major conferences like NeurIPS and ICLR to be the most important.
I encourage you to go through the [reproducibility checklist](https://www.cs.mcgill.ca/~jpineau/ReproducibilityChecklist.pdf) published by Joelle Pineau, who also gave [a great talk](https://www.youtube.com/watch?v=Vh4H0gOwdIg) about this issue in ICLR 2018.
I will use this list as a basis to what I will include in the wiki section about reproducibility.
My hope is that after you go through the material here, you'll check more items in that list than you'd do before.

## Ethical and Practical Reasons for Reproducibility

The ethical reasons are obvious.
It is, in a broader sense, for the more efficient advancement of science.
I will cite the Nature special I mentioned earlier:

> Science moves forward by corroboration – when researchers verify others’ results. Science advances faster when people waste less time pursuing false leads.

I can count many times that my advisor asked me to compare the method we develop with the so called state-of-the-art approached and I struggled terribly with it. 
I usually had one of the three challenges: (1) the code was published online but it required a proprietary software (e.g. MATLAB) to run it, (2) the code wasn't published or I didn't get a response to my emails from the authors of the paper, (3) I acquired to code but it was written so poorly that I couldn't figure out the right way to use the algorithm for my own purposes.
I don't blame the authors, because I also know the pressure they're exposed to by the current state of the academic incentive mechanisms.
However, I encourage myself and the reader to be more aware of this situation when writing code fore research.

The practical reasons are more obvious.
Instead of reinventing the wheel, I encourage the reader to check [this blog post] (https://determined.ai/blog/reproducibility-in-ml/) from Determined AI on the perks of being reproducible.
The key takeaway from the case study is that you or your colleague can pick up your work wherever you left from, without facing some surprises.
I especially encourage the reader to carefully study the root causes of non-determism, which I hope to address most items in there through this wiki.




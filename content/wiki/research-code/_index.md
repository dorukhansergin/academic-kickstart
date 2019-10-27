---
# Course title, summary, and position.
linktitle: Research Code and Data Management 
summary: I share the tricks I learned trying to manage my own research 
weight: 1

# Page metadata.
title: Research Code and Data Management 
date: "2019-10-27T00:00:00Z"
lastmod: "2019-10-27T00:00:00Z"
draft: false  # Is this a draft? true/false
toc: true  # Show table of contents? true/false
type: docs  # Do not modify.

# Add menu entry to sidebar.
# - name: Declare this menu item as a parent with ID `name`.
# - weight: Position of link in menu.
menu:
  example:
    name: Research Code and Data Management 
    weight: 1
---

## Why this tutorial?

An extreme simplification of science/engineering research workflow is as follows:

1. Read some papers

2. Collect some data

3. Analyze that data

4. Generate tables and figures

5. Wrap them around some textual explanation in order to transform it into a paper or presentation

6. Try to get it published

As of 21<sup>st</sup> century, almost all of these tasks require some sort of scripting in a computer. However, the challenges of scientists/researchers stayed the same over the centuries which I will list as follows:

* Reproducibility and verifiability
* Transparency
* Documentation
* Logging experiment results correctly
* Effective collaboration with fellow researchers

However, most researchers—even those in the computer science department—lack the fundemental skills to achieve these goals with the scripts they write. 

When I first started writing scripts for my master's thesis, I had no idea about what the above terms even mean, let alone the skills to achieve them. 
I somehow finished writing it and now the code resides in a GitHub repo so ugly that I am embarassed to make it public. 
Right after that thesis was written, I started my PhD and I promised myself to be much more proactive this time.
Fortunately, I came across very early Trey Causey's excellent piece[^1] on software development skills for data scientists.
While he obviously was targeting an audience of data scientists, everything he says are equally relevant to any science/engineering majors.
So I started digging deeper into this.
The luck wasn't on my side, thiugh, such know-how was nowhere to be found in the people in my immediate reach: friends, seniors, post-docs, even my advisor.

I started learning these on my own...

2 years into my PhD and I still lack a consistent system and I can by no means claim that I learned it all.
However, how I do research is much better than how I did 2 years ago.
I know have GitHub repos that I'm very comfortable sharing with other people.
In fact, they are meant to be shared with a wider audience.

With this small wiki tutorial, I'd like to share all (okay, maybe most) of what I think I know about _doing it the right way_.

## Intended Audience

Are you or you want to become a successful researcher or data scientist?
Do you care about the challenges outlined in the previous section above?
Then I invite you to at least scroll through the content here.
**I especially target people using Python for scientific computing**, but some advice here should be universally applicable.

[^1]: [http://treycausey.com/software_dev_skills.html](http://treycausey.com/software_dev_skills.html)
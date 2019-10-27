---
title: Know Thy System
linktitle: Know Thy System
toc: true
type: docs
date: "2019-10-27T00:00:00+01:00"
draft: false
menu:
  example:
    parent: Preliminaries
    weight: 1

# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 1
---

Most non-CS researchers skip this part but a researcher should know about certain details of the hardware and the operating system they are using for research.

## What Operating System (OS) are you using?

Most common are Windows, MacOS and Linux.
I assume everybody knows which of the three they are using, but there are more into it:

* What Windows/MacOS/Linux version are you using? Operating systems are a piece of software themselves and they have a version number like _10.14.6_
* If you are using Linux, what is the distribution (distro for short) you are using (e.g. Ubuntu, Mint)
* Is it a 32-bit or 64-bit OS?

Why should you know this?
I can at least come up with two reasons:

* You need to know if and which version of a piece of software works on your computer. For example, [Anaconda download page](https://www.anaconda.com/distribution/#download-section) expects you to choose the right installer for your system.
* When you ask for help about a bug in your code, it is often very helpful for the developers that they know in which system you are having trouble. Oftentimes, the software are developed differently for different OS so it makes it easier for them to reproduce the problem you are having in the right environment. In other words, your bug may be OS-specific.

## Do you know your hardware?

Most important hardware will be the CPU and RAM. 
Recently, GPU has become important for deep learning research.
Understanding what each of them does, even at the basic level, is important.
Here is a [post](https://www.watchingthenet.com/cpu-gpu-ram-hdd-computer-terms-explained-in-plain-english.html) that explains them in plain English.
It is important to know the make,  model and specifications of your hardware.
This will give you an idea about the limits of your computational power.

Here are certain things I would like to outline:

* Know what the following means: **CPU bound, I/O bound, Memory bound**. There are related to the bottleneck in your computing power, and might help you understand why your code is running slow.
* Know what **concurrency** is. Know what a **thread** and **process** is. Know what it means to **multithread** and **multiprocess**. This might help you utilize the full potential of your hardware and run your experiments marginally faster. Here is a [gentle introduction](https://www.internalpointers.com/post/gentle-introduction-multithreading) to the concepts. 
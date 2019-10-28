---
title: Unix Shell
linktitle: Unix Shell
toc: true
type: docs
date: "2019-10-27T00:00:00+01:00"
draft: false
menu:
  example:
    parent: 1. Preliminaries
    weight: 3

# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 3

---

For some, it is how they enter the matrix. 
For others, it is the most complicated nightmare ever.
I'm talking about \*drumroll intensifies\* the Unix shell!

<iframe src='https://gfycat.com/ifr/EquatorialPersonalEgg' frameborder='0' scrolling='no' allowfullscreen width='640' height='405'></iframe><p>I think it's neither as hard nor as cool as you might think.</p>
## Why learn Unix Shell?

In a [Reddit post](https://www.reddit.com/r/linux/comments/2mur41/what_is_there_you_cannot_do_using_gui_what_you/) about this, there is this comment:

> What can you do by talking that you can't achieve by pointing at pictures and signs? :)

Knowing how to use the shell opens up a plethora of new functionalities you won't be able to utilize using the graphical user interface (GUI).
I can state a few major reasons why a researcher would want to learn Unix shell:

1. Using full functionalities of developer tools like Git, Conda or public APIs of certain organizations to query data without hassle
2. Accessing and navigating through high-performance clusters (HPC) or cloud services (AWS, Google Cloud) to have them do the computational heavylifting of your work. Transfering files back and forth.
3. Better management of the files and folder structure of your projects.
4. BONUS: once you learn the shell, you'll rarely be using the file explorer because keyboard is almost always faster than the mouse.

Shell is easy to learn.
The key is to narrow down the content to learn and start slow.
Consistent use of the shell everyday for 2-3 weeks will get you to be comfortable with pretty much everything you can do with a GUI such as the file explorer in Windows or Mac.

## How to learn the basics?

I didn't bother creating learning notes for Linux.
There is already a mountain of resources out there.
My favorite material for beginners is by the amazing project [Software Carpentry](https://swcarpentry.github.io/shell-novice/). 
Just spend an afternoon consuming this material and for the next two weeks, force yourself to do everything you'd normally do with a GUI, in terminal.
Trust me, regardless of how computer illiterate you are, it is still easy to learn.

If you have more time, I suggest this [amazing resource](https://www.learnenough.com/command-line-tutorial/basics) from the Learn Enough series.
You don't really need the paid content in there for starters.

## Bash, zsh, fish

As you use the plain vanilla `bash`, you might figure out that you'd be happier with some additional functionalities, like autocompletion of directory and file names.
`zsh` and `fish` are extensions to classic `bash` that will take your terminal experience from 90s to 2010s.
I strongly suggest using one of them.
I personally use `zsh` and specifically the `oh-my-zsh` configuration of it. 
Here is a [HowtoGeek piece](https://www.howtogeek.com/362409/what-is-zsh-and-why-should-you-use-it-instead-of-bash/) why to use `zsh` and how to install it.

## Setting up Development Environment on Windows

Unix shell comes default with Mac and Linux. Windows has a terminal too, but the functionalities and the keywords differ from the Unix shell (the one in Mac and Linux).
Since HPCs and cloud services often use Unix shell and since it is much more fun to work with, I strongly suggest downloading a Linux emulator to your system.
See [here](https://www.puttygen.com/windows-terminal-emulators) for a list of options.
As of Windows 10 there is also the Linux Subsytem option.

I haven't personally used any of them, maybe just try any of them for starters.
As you get more and more comfortable with Unix, you'll develop more specific needs from an emulator.

Whether Windows is suitable for Data Science and Machine Learning is an open debate.
I won't go into that but I'll redirect you all the resources I could find on the net:

* https://towardsdatascience.com/setting-up-a-data-science-environment-using-windows-subsystem-for-linux-wsl-c4b390803dd
* https://medium.com/faun/how-to-use-git-and-other-linux-tools-in-wsl-on-windows-4c0bffb68b35
* https://blog.joaograssi.com/windows-subsystem-for-linux-with-oh-my-zsh-conemu/

Ideally you'd want to have a single shell in your system that can:

* run conda
* run git
* have fundamental functionalities of linux (in addition to basic file navigation, `wget`, `awk`, `grep` etc.)
* a more modern looking and user-friendly flavor of bash like `zsh` or `fish`

## 


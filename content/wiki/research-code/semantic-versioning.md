---
title: Semantic Versioning
linktitle: Semantic Versioning
toc: true
type: docs
date: "2019-10-27T00:00:00+01:00"
draft: false
menu:
  example:
    parent: Preliminaries
    weight: 2

# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 2

---

Did you ever notice that most software has a version number in the form of a triplet?
Here is what I see when I pull up _Abouth this Mac_ on my mac computer.

{{< figure library="true" src="my-mac-version.png" title="A caption" lightbox="true" >}}

We've seen in the previous section that OS itself is a piece of software.
In this case, the macOS installed in my computer is tagged by a tripled of numbers: 10.14.6.

The beloved language Python is no exception. 
If you don't believe me, check out the [versions page](https://www.python.org/doc/versions/).

## Why bother?

As researchers/scientists, we are consumers of many kinds of software.
This could be a language (e.g. Python, R), or a third-party libraries (e.g. NumPy, ggplot2) developed for that language.
It is important for us to have an idea about what is going on in the development process of these pieces of software.
Semantic versioning is an attempt to give developers a universal guideline to signify what changes have been made to the software and what are the implications of these.
Everytime an update comes to the software, one of the three numbers are bumped up by one.

First, let's give some definitions:

* **Application Programming Interface (API)**: For our purposes, we can narrow down the definition of API and say that it is _how the user interact with the functionalities of a piece of software_. In other words, _what can I do with this software and how can I do it_. The documentation of software usually guides us through this API.
* **Release:** This is a published version of a software when its developers think it reached a certain maturity.
* __Release Notes:__ A published log of what has changed about the software at that release.

A version number can be decomposed as __MAJOR.MINOR.PATCH__:

- __Major Release:__ This happens least frequently and signifies major changes to the software. Characterized by incompatible changes to the API. The example I always give is the `print` function in Python. In Python 2, the API to printing something was like:

  ```python
  # this only works in Python 2
  print "Hello World!"
  ```

  When Python updated from 2.\*.\*s to 3.\*.\*s (asterisk means it could be any number that applies there, in this case, any subversion of that specific major release), one of the fundamental changes happened to the `print` function.

  ```python
  # this works only in Python 3
  print("Hello World!")
  ```

  Now you have to have brackets around the string to be printed.
  What is the implication here? 
  Say, if you had a script that was written in Python 2 but then you decided to update to Python 3.
  Boom, you have all these errors now.
  The modification you made is said to be __not backwards compatible__.
  In other words, what works in this version might *break* things.
  The lesson to learn here is to be extra careful when making such version changes.

- __Minor Release:__ This happens more frequently than major releases. 
  It usually signifies some additional functionality added to the software, but these changes will not affect what was already in there.
  For example, in Python 3.6, f-strings are added as a new functionality, something we didn't have in any of the versions earlier to that. 
  The change is backward compatible, meaning that if I have a code that I know that it works without any problem with, say, Python 3.4; then can rest assure that it will still be working if you update to 3.6.
  It is important to know about this when running somebody else's code, since they might be using a functionality that was added at a version released later than what you are currently using in your system.

  ```python
  # this works both in Python 3.4 and 3.6
  first_word = "Hello"
  second_word = "World"
  print("{} {}!".format(first_word, second_word))
  
  # this works in Python 3.6, but breaks in 3.4
  print(f"{first_word} {second_word}!")
  ```

- **Patch Release:** These changes happen the most frequently.
  Usually they are introduced for bug fixes that are backwards compatible, just like minor releases.
  It is always a good idea to make patch release updates as they come.

We need to know about semantic versioning for three major reasons:

- To make sure our code works, managing the versions and updates intelligently
- To make sure our code works at someone else's system
- To make sure someone else's code work in our system

## Further Reading

* https://semver.org/


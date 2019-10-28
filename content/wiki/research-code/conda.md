---
title: Running Python Scripts
linktitle: Conda
toc: true
type: docs
date: "2019-10-27T00:00:00+01:00"
draft: false
menu:
  example:
    parent: 2. Environment and Package Management in Python
    weight: 6

# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 6
---

_This part of the tutorial assumes that you have working knowledge of the concepts included in the [Preliminaries section]({{< ref  "/wiki/research-code/preliminaries.md" >}})_

How do you open an Word file?
Well, first of all there is a file with a name similar to `myfile.docx`, and you have the program Word installed on your computer.
You open `myfile.exe` with the Word application, which is nothing but an executable file (typically something like `Word.exe`).
While you do most of this through a GUI, the underlying process can be replicated in a shell with something similar to the following:

```bash
/path/to/Word/Word.exe /path/to/myfile/myfile.docx
```

In plain English this means: _use the executable file of the application Word `Word.exe`  located in `/path/to/Word/` to open `myfile.docx` located in `/path/to/myfile`_

Running Python scripts have a similar logic.
Let's say you have a file called `helloworld.py` with the contents as follows:

```python
# helloworld.py
print("Hello World")
```

If you have Python installed in your system, the only thing you have to do is to go to your shell, navigate to where `helloworld.py` is and run the following:

```bash
cd /path/to/helloworld.py
python helloworld.py
```

How did this work?
The reason why I'm asking this is I don't have a `python.exe` in the same folder as `helloworld.py`.
So how did my shell know where `python.exe` was?
First, type the following command:

```bash
which python
```

On my system, this returns the following:

```bash
> /Users/dorukhansergin/miniconda3/bin/python
```

This the equivalent of `/path/to/python.exe` in my system, because I installed Python using Miniconda.
Depending on how you installed python, you'll get an according result.
I won't go into the details of how the shell associates the keyword `python` with `/Users/dorukhansergin/miniconda3/bin/python` but it's a good idea to know what `which` does and what happens everytime we call `python`.

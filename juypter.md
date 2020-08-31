---
layout: page
title: Jupyter User Guide
permalink: /jupyter
---

<nav class="toc">
  <header><h4 class="nav__title">Guides: Navigation</h4></header>
  <ul class="toc__menu">
    <li>
      <a href="/guides/conda">Conda User Guide</a>
    </li>
    <li>
      <a href="/guides/conda-issues">Common Conda Issues</a>
    </li>
    <li>
      <a href="/guides/jupyter">Jupyter User Guide</a>
    </li>
  </ul>
</nav>

We will use the [Jupyter
notebook](https://jupyter-notebook.readthedocs.io/en/stable/) to run our Python
data analysis in this course. If you've successfully installed and activated the
environment for this course, the Jupyter notbook package should already be
installed.

On this page, I'll discuss two common issues when starting out with Jupyter
notebooks: launching a notebook and ensuring the right files are available.

For a guide to the user interface of Jupyter notebook, see the
[documentation](https://jupyter-notebook.readthedocs.io/en/stable/ui_components.html).

## Launching a Jupyter notebook

The recommended approach for starting a notebook is to use the Anaconda Prompt
on Windows or the Terminal app on MacOS. To do so, we simply need to activate
our `'{{ site.env_name }}'` environment and then launch the notebook.

From the command line, run:

```
conda activate {{ site.env_name }}
```

```
jupyter notebook
```

This will create the local Jupyter server. If it does not open in a browser,
copy the link that is output by the command into your favorite browser.
Typically, the server will be running at http://localhost:8080.

Once the server is running, you can create a new notebook and get started!

### The current directory

The notebook will execute code from the current working directory (the directory
that the notebook was launched from). If using relative file paths to load the
data, the path should be relative to this working directory. From within the
Jupyter notebook, you can find out the current working directory by running the
following command in a cell:

```
pwd
```

## Changing the Jupyter notebook start-up folder

By default, the Jupyter notebook launches from your home directory. When you
see the Notebook dashboard, you should see all of the files in this
folder.

When working with weekly lectures or assignments, it is easiest to open notebooks
from the specific assignment or week folder that you are working on.

To do so, it will be easiest to change the directory before launching the
Jupyter notebook:

### Step 1: Change to the desired directory

Let's imagine we want to change to a folder named:

/Users/YourUserName/MUSA_550 (on a Mac),

or

C:\Users\YourUserName\MUSA_550 (on Windows)

If you need help finding the folder name's path, [this guide for Windows](https://www.wikihow.com/Find-a-File%27s-Path-on-Windows). (I usually use Method #2). On MacOS, you can use [this guide](http://osxdaily.com/2015/11/05/copy-file-path-name-text-mac-os-x-finder/) to copy a folder's path name.

Next, use the following steps:

**Step 1.** On Windows, open the Anaconda Prompt, or on Mac, open the Terminal.

**Step 2.** Navigate to the folder where the environment file is located. From the Prompt or Terminal run:

**Windows**

```
cd C:\Users\YourUserName\MUSA_550
```

**Mac**

```
cd /Users/YourUserName/MUSA_550/
```

### Step 2: Launch the Jupyter notebook

Now, type the following command, either in Anaconda Prompt or the Terminal:

```
jupyter notebook
```

And the launched notebook will start from your desired folder!

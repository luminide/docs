---
title: Overview
weight: -200
---

(starting-overview)=
# Overview

Luminide makes it *easier* to build *better AI models*:
- **Easier**: Luminide contains all of the hardware and software you need, is hosted in the cloud, and automates the tedious, repetitive tasks.
- **Better AI models**: Luminide contains tools like Hyperparameter Tuning and optimizations like Early Ranking.  These help build higher accuracy models, get results faster, and even reduce training costs.

## Luminide Architecture

Luminide's distributed architecture consists of two main components, the *IDE Server* and the *Compute Server*.

```{image} ../images/new-tutorial-overview-diagram.png
:width: 650
```

- **IDE Server**: This is what controls everything, e.g., where you log in, download and edit your code, experiments are tracked,  and results are stored.  This is also where commands that run on the Compute Server are launched.
- **Compute Server**: This is where experiments are executed.  Before each run, code from the IDE server is automatically copied over, and after each run the results are automatically copied back.  This is also where datasets are downloaded and stored.

## Luminide File Structure

At a minimum, you need some code that trains a model and a script that invokes this code. For an example, see <kbd>train.py</kbd> and <kbd>full.sh</kbd> in the [generic-example repo](https://github.com/luminide/example-generic). The directory structure is expected to be:

```
IDE Server                                      Compute Server                            

project                                         project                            
├── code (source code)                          ├── [source code copy]
                                                ├── input (dataset)                
└── output [working directory copy]             └── output (working directory)     
```

Note that both <kbd>code/</kbd> and <kbd>input/</kbd> are peers of the working directory. This means that if your code wants to access the dataset, the paths must be prefixed with <kbd>../input</kbd>. To access files in the <kbd>code/</kbd> directory, the paths must be prefixed with <kbd>../code</kbd>.

(code-file-browser)=
## Code File Browser

Code, which is located on the IDE Server, can be browsed using the Code File Browser in the left-hand sidebar (hide browser by clicking on the active icon).

```{image} ../images/feb-code-browser.png
:width: 300
```

(data-file-browser)=
## Data File Browser

Data, which is located on the Compute Server, can be browsed using the Data File Browser in the left-hand sidebar (hide data browser by clicking on the active icon):

```{image} ../images/feb-data-browser.png
:width: 300
```

## Luminide Menu

Most of the Luminide features are available under the Luminide drop-down menu.  For example, to reopen the documentation tab, navigate to the Menu, click on Luminide, and select Documentation:

Menu: `Luminide > Documentation`

```{image} ../images/feb-luminide-menu.png
:width: 300
```

## Jupyter IDE

Luminide leverages Project Jupyter open-source software such as JupyterLab and JupyterHub for their IDE, notebook, and multi-user support.  We'd like to give the [Jupyter Project and Community](https://jupyter.org/about.html) a special thanks for building such amazing products.

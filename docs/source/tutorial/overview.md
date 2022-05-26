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

- **IDE Server**: This is what controls everything, e.g., where you log in from your **browser**, download and edit your code, experiments are tracked/monitored/visualized,  hyperparameter tuning is managed, and results are stored.  This is also where commands that run on the Compute Server are launched.
- **Compute Server**: This is where experiments are executed.  Before each run, code from the IDE server is automatically copied over, and after each run the results are automatically copied back.  Datasets are downloaded and stored on persistent **Cloud Storage**, which is co-located with the Compute Server for high performance.

## Luminide IDE

The Luminide IDE is a customized version of the Jupyter IDE hosted in the cloud.  It includes everything that makes the Jupyter IDE so popular among data scientists, e.g. notebooks, code editing, file browsers.  But also includes everything you need for model development, e.g. connect to cloud GPUs, run and track experiments, hyperparameter tuning.  And since it's all fully integrated, everything is just a click away.

```{image} ../images/ide-screenshot.png
:width: 650
```

In addition to building on top of Jupyter's IDE, Luminide leverages other Project Jupyter open-source software such as JupyterLab and JupyterHub.  We'd like to give the <a href="https://jupyter.org/about.html" target="_blank">Jupyter Project and Community</a> a special thanks for building such great products.

## Luminide File Structure

To train a model, at a minimum you'll need some code that trains the model and a script that invokes this code. For an example, see <kbd>train.py</kbd> and <kbd>full.sh</kbd> in the <a href="https://github.com/luminide/example-generic" target="_blank">generic-example repo</a>. You'll also need the input dataset.  The directory structure is expected to be:

```
IDE Server                                      Compute Server                            

project                                         project                            
├── code (source code)                          ├── [source code copy]
├                                               ├── input (dataset)                
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

## Tutorial

Try out Luminide for yourself by doing our [Tutorial](plant-leaf-tutorial).

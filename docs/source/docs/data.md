---
title: Data
weight: 130
---

(docs-data)=
# Data

(docs-import-data)=
## Import Data

This feature allows you to import a dataset into your project.  The data will be imported to the Compute Server, which is where the data will be consumed, but you will still be able to view it from your browser.  The data volume is persistent, which means you only need to download it once.  Your data will still be there the next time you log into Luminide.

Menu: `Luminide > Import Data to Compute Server`

Luminide imports datasets from a variety of different sources, including Kaggle and Google.  Navigate to the corresponding tab and follow the instructions on that tab.  Once  you're ready, click the `Import Data to Compute Server` button and the data will start downloading. When it's finished, you will get a "Download Succeeded" message.

```{image} ../images/feb-google-cloud.png
:width: 500
```

The data can be browsed using the Data File Browser in the left-hand sidebar (hide data browser by clicking on the active icon):

```{image} ../images/feb-data-browser.png
:width: 300
```

## Jupyter Notebook

Create and share documents that contain live code, equations, visualizations, and text with a Jupyter Notebook.  Notebooks are created and edited on the IDE Server, but the cells are executed on the Compute Server.  Therefore, you must have a Compute Server attached to run a notebook.

Menu: `Luminide > Create Notebook`

```{image} ../images/jupyter-notebook.png
:width: 350
```

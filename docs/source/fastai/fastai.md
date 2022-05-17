---
title: Fast AI
weight: 100
---

# Fast AI Tutorials

[Fast.ai](https://www.fast.ai) is a deep learning library which provides AI practitioners with high-level components that can quickly and easily provide state-of-the-art results in standard deep learning domains.

Read through the [fast.ai tutorials](https://docs.fast.ai/) to learn how to train your own models on your own datasets. Use the navigation sidebar to look through the fast.ai documentation.

```{image} ../images/fastai-fastai.png
:width: 510
```

To run fast.ai notebooks on Luminide, just follow the the instructions on this page.

## Sign up to Luminide

Visit the [Luminide website](https://www.luminide.com) to sign up and log in:

```{image} ../images/fastai-signup.png
:height: 150
```

```{image} ../images/fastai-signup-2.png
:height: 150
```

## Import fast.ai notebooks

Once you log into Luminide, import the fast.ai tutorials:
- `Create and Open` a new project
- Initialize project code by choosing `Import`
- Enter the URL of the [fast.ai git repository](https://github.com/fastai/fastai): `https://github.com/fastai/fastai.git`

```{image} ../images/fastai-new-project.png
:height: 125
```
```{image} ../images/fastai-import-code.png
:height: 125
```
```{image} ../images/fastai-import-code-2.png
:width: 510
```

Once the repo finishes importing, use the file browser to navigate to the `/nbs` directory.  Here you will see a list of all of the fast.ai notebooks:

```{image} ../images/fastai-import-code-3.png
:width: 300
```

## Connect to a cloud GPU

Before executing a notebook, you must first connect to cloud compute server:
- Menu: `Luminide > Manage Compute Server` (or click on the status bar in the lower-left corner)
```{image} ../images/fastai-status-bar.png
:width: 135
```

Choose the compute server based on performance and price. Select `Spot compute` for additional savings. For example, a GCP A100 spot compute server will run an entire fast.ai notebook in around 5 minutes and cost about $0.10.

```{image} ../images/fastai-attach-compute.png
:width: 600
```


## Run a fast.ai notebook

Select a notebook and `Run the selected cells` or `Re-run the whole notebook`.

```{image} ../images/fastai-tutorial-vision.png
:width: 600
```

## Tutorial and notebook summary

The online fast.ai tutorials correspond to the following files in the fast.ai github repository:

| **Beginner**    |     |
| :--- | ---: |
| [Vision](https://docs.fast.ai/tutorial.vision.html)    | [23_tutorial.vision.ipynb](https://github.com/fastai/fastai/blob/master/nbs/23_tutorial.vision.ipynb)    |
| [Text](https://docs.fast.ai/tutorial.text.html)    | [38_tutorial.text.ipynb](https://github.com/fastai/fastai/blob/master/nbs/38_tutorial.text.ipynb) |
| [Tabular](https://docs.fast.ai/tutorial.tabular.html)    |  [44_tutorial.tabular.ipynb](https://github.com/fastai/fastai/blob/master/nbs/44_tutorial.tabular.ipynb) |
| [Collab](https://docs.fast.ai/tutorial.collab.html)    | [46_tutorial.collab.ipynb](https://github.com/fastai/fastai/blob/master/nbs/46_tutorial.collab.ipynb) |
| **Intermediate**    |     |
| [DataBlock](https://docs.fast.ai/tutorial.datablock.html)    | [50_tutorial.datablock.ipynb](https://github.com/fastai/fastai/blob/master/nbs/50_tutorial.datablock.ipynb) |
| [Imagenette](https://docs.fast.ai/tutorial.imagenette.html) | [22_tutorial.imagenette.ipynb](https://github.com/fastai/fastai/blob/master/nbs/22_tutorial.imagenette.ipynb) |
| [Medical Imaging](https://docs.fast.ai/tutorial.medical_imaging.html) | [61_tutorial.medical_imaging.ipynb](https://github.com/fastai/fastai/blob/master/nbs/61_tutorial.medical_imaging.ipynb) |
| [Pets](https://docs.fast.ai/tutorial.pets.html) | [10_tutorial.pets.ipynb](https://github.com/fastai/fastai/blob/master/nbs/10_tutorial.pets.ipynb) |
| [Transformers](https://docs.fast.ai/tutorial.transformers.html) | [39_tutorial.transformers.ipynb](https://github.com/fastai/fastai/blob/master/nbs/39_tutorial.transformers.ipynb) |
| [Wikitext](https://docs.fast.ai/tutorial.wikitext.html) | [35_tutorial.wikitext.ipynb](https://github.com/fastai/fastai/blob/master/nbs/35_tutorial.wikitext.ipynb) |
| **Advanced**   |     |
| [Albumentations](https://docs.fast.ai/tutorial.albumentations.html)   | [10b_tutorial.albumentations.ipynb](https://github.com/fastai/fastai/blob/master/nbs/10b_tutorial.albumentations.ipynb) |
| [Siamese](https://docs.fast.ai/tutorial.siamese.html) | [24_tutorial.siamese.ipynb](https://github.com/fastai/fastai/blob/master/nbs/24_tutorial.siamese.ipynb) |
| [Image Sequences/Video](https://docs.fast.ai/tutorial.image_sequence.html) | [24_tutorial.image_sequence.ipynb](https://github.com/fastai/fastai/blob/master/nbs/24_tutorial.image_sequence.ipynb) |

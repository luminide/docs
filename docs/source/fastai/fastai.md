---
title: Fast AI
weight: 100
---

# Fast AI Tutorials

<a href="https://www.fast.ai" target="_blank">Fast.ai</a> is a deep learning library which provides AI practitioners with high-level components that can quickly and easily provide state-of-the-art results in standard deep learning domains.

Read through the <a href="https://docs.fast.ai/" target="_blank">fast.ai tutorials</a> to learn how to train your own models on your own datasets. Use the navigation sidebar to look through the fast.ai documentation.

```{image} ../images/fastai-fastai.png
:width: 510
```

To run fast.ai notebooks on Luminide, just follow the instructions on this page.

## Sign up to Luminide

Visit the <a href="https://www.luminide.com" target="_blank">Luminide website</a> to sign up and log in:

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
- Enter the URL of the <a href="https://github.com/fastai/fastai" target="_blank">fast.ai git repository</a>: `https://github.com/fastai/fastai.git`

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

Choose the compute server based on performance and price. Select `Spot compute` for additional savings. For example, a GCP A100 spot compute server will run the entire vision notebook in around 5 minutes and cost about $0.10 (some notebooks take significantly longer, so adjust your idle timeout setting accordingly).

```{image} ../images/fastai-attach-compute.png
:width: 600
```

Once you attach to a compute server, be sure to log in and upgrade to the lastest software:
- Menu: `Luminide > Compute Server Terminal` and run: `pip install -U fastai nbdev`

## Run a fast.ai notebook

Select a notebook and `Run the selected cells` or `Re-run the whole notebook`.

```{image} ../images/fastai-tutorial-vision.png
:width: 600
```

## Tutorial and notebook summary

The online fast.ai tutorials correspond to the following files in the fast.ai github repository:

| **Beginner**    |     |
| :--- | ---: |
| <a href="https://docs.fast.ai/tutorial.vision.html" target="_blank">Vision</a>         | <a href="https://github.com/fastai/fastai/blob/master/nbs/23_tutorial.vision.ipynb" target="_blank">23_tutorial.vision.ipynb</a>    |
| <a href="https://docs.fast.ai/tutorial.text.html" target="_blank">Text</a>               | <a href="https://github.com/fastai/fastai/blob/master/nbs/38_tutorial.text.ipynb" target="_blank">38_tutorial.text.ipynb</a> |
| <a href="https://docs.fast.ai/tutorial.tabular.html" target="_blank">Tabular</a>      |  <a href="https://github.com/fastai/fastai/blob/master/nbs/44_tutorial.tabular.ipynb" target="_blank">44_tutorial.tabular.ipynb</a> |
| <a href="https://docs.fast.ai/tutorial.collab.html" target="_blank">Collab</a>         | <a href="https://github.com/fastai/fastai/blob/master/nbs/46_tutorial.collab.ipynb" target="_blank">46_tutorial.collab.ipynb</a> |
| **Intermediate**    |     |
| <a href="https://docs.fast.ai/tutorial.datablock.html" target="_blank">DataBlock</a>                       | <a href="https://github.com/fastai/fastai/blob/master/nbs/50_tutorial.datablock.ipynb" target="_blank">50_tutorial.datablock.ipynb</a> |
| <a href="https://docs.fast.ai/tutorial.imagenette.html" target="_blank">Imagenette</a>                   | <a href="https://github.com/fastai/fastai/blob/master/nbs/22_tutorial.imagenette.ipynb" target="_blank">22_tutorial.imagenette.ipynb</a> |
| <a href="https://docs.fast.ai/tutorial.medical_imaging.html" target="_blank">Medical Imaging</a>  | <a href="https://github.com/fastai/fastai/blob/master/nbs/61_tutorial.medical_imaging.ipynb" target="_blank">61_tutorial.medical_imaging.ipynb</a> |
| <a href="https://docs.fast.ai/tutorial.pets.html" target="_blank">Pets</a>                               | <a href="https://github.com/fastai/fastai/blob/master/nbs/10_tutorial.pets.ipynb" target="_blank">10_tutorial.pets.ipynb</a> |
| <a href="https://docs.fast.ai/tutorial.transformers.html" target="_blank">Transformers</a>   | <a href="https://github.com/fastai/fastai/blob/master/nbs/39_tutorial.transformers.ipynb" target="_blank">39_tutorial.transformers.ipynb</a> |
| <a href="https://docs.fast.ai/tutorial.wikitext.html" target="_blank">Wikitext</a>                   | <a href="https://github.com/fastai/fastai/blob/master/nbs/35_tutorial.wikitext.ipynb" target="_blank">35_tutorial.wikitext.ipynb</a> |
| **Advanced**   |     |
| <a href="https://docs.fast.ai/tutorial.albumentations.html" target="_blank">Albumentations</a>               | <a href="https://github.com/fastai/fastai/blob/master/nbs/10b_tutorial.albumentations.ipynb" target="_blank">10b_tutorial.albumentations.ipynb</a> |
| <a href="https://docs.fast.ai/tutorial.siamese.html" target="_blank">Siamese</a>                                       | <a href="https://github.com/fastai/fastai/blob/master/nbs/24_tutorial.siamese.ipynb" target="_blank">24_tutorial.siamese.ipynb</a> |
| <a href="https://docs.fast.ai/tutorial.image_sequence.html" target="_blank">Image Sequences/Video</a> | <a href="https://github.com/fastai/fastai/blob/master/nbs/24_tutorial.image_sequence.ipynb" target="_blank">24_tutorial.image_sequence.ipynb</a> |

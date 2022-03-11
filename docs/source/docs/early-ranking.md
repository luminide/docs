---
title: Early Ranking
weight: 220
---

# Early Ranking

Luminide includes an optimization we developed which uses predictive modeling to determine the relative outcome of a training run after only a few epochs. For example, instead of running 30 epochs for a training run, it may only require 3 epochs.  We call this optimization Early Ranking.

## Fast Training

Early Ranking can be used by data scientists to do rapid prototyping.  Simply check the <kbd>Fast Training</kbd> box when executing a single training run.

```{image} ../images/feb-fast-training.png
:width: 550
```

(fast-sweeps)=
## Fast Sweeps

  Early Ranking can also be used for Hyperparameter Tuning.  Similary, check the <kbd>Fast Sweep</kbd> box to enable this feature.  Each of the trails in the Sweep will then execute a fewer number of epochs, and then use the precitive model to compute its score.

```{image} ../images/feb-fast-sweep.png
:width: 550
```

Fast sweeps require more fine-grained training and validation errors to be collected. It is recommended that template-generated code be used to enable this. The expected format for history.csv is:

```
epoch, iter, train_loss, val_loss
0, 0, 0.5789984, 0.6578998
0, 1, 0.4998457, 
…
```

In this case, “iter” refers to the index of a minibatch within an epoch. The “val_loss” value may be left blank for many minibatches, but should be computed at regular intervals as shown in the train_epoch() function inside [train.py](https://github.com/luminide/example-generic/blob/main/train.py).


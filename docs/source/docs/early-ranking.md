---
title: Early Ranking
weight: 220
---

# Early Ranking

Luminide includes an optimization, called Early Ranking, which uses predictive modeling to determine the relative outcome of a training run after only a few epochs. This can be used for rapid prototyping, e.g. experimenting with different model layers or data transformations to determine which are effective. It can also be used for hyperparameter tuning, which allows a larger search space to be explored, leading to a higher accuracy model.

## Experimental Phase

Early ranking is still in the experimental phase.  In many cases it has achieved the same results using 5 to 10 times fewer epochs, but not in every case. We encourage you to try it out and let us know how well it works for you. One thing you can do is as follows:

1. Train your neural net (i.e. full training).
2. Perform hyperparameter tuning using Early Ranking (i.e. fast sweep).
3. Take the best result from your hyperparameter sweep and train your model again (i.e. full training). You can do this by logging into the IDE server and running something like this: `ubuntu@ide-server:~/plant-pathology$ cp output/exp47/config-tuned.yaml code/config.yaml`

Ideally this will produce in a higher accuracy model in a fraction of the time. Optionally, repeat steps 2 and 3 a few times with different values of epochs in the `fast.sh` script.  Sharing this accuracy/speedup curve with us would help us characterize and improve our Early Ranking technology (send email to `support@luminide.com`).

## Fast Training

Early Ranking can be used by data scientists to do rapid prototyping.  Simply check the <kbd>Fast Training</kbd> box when executing a single training run.

```{image} ../images/feb-fast-training.png
:width: 550
```

(fast-sweeps)=
## Fast Sweeps

  Early Ranking can also be used for Hyperparameter Tuning.  Similary, check the <kbd>Fast Sweep</kbd> box to enable this feature.  Each of the trials in the fast sweep will then execute a fewer number of epochs, and then use the predictive model to compute its score.

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


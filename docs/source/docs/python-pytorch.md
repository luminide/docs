---
title: Python & PyTorch
weight: 500
---

# Python & PyTorch

## Check Python Syntax

Luminide allows you to quickly check for syntax errors in the Python code on the IDE server before copying and executing it on the compute server:

Menu: `Luminide > Check Python Syntax`

```{image} ../images/compile-code.png
:width: 400
```

Any syntax errors will be displayed. Error free files will report succeeded.

## PyTorch Profiler

The PyTorch Profiler records the CPU side operations as well as the CUDA kernel launches on the GPU side. The profiler can visualize this information in TensorBoard and provide analysis of the performance bottlenecks.

To use the PyTorch Profiler, update your code to call `torch.profiler.profile` and `prof.step` as [described here](https://pytorch.org/tutorials/intermediate/tensorboard_profiler_tutorial.html#use-profiler-to-record-execution-events).

Then select the `PyTorch_Profiler` tab in TensorBoard:

Menu: `Luminide > Experiment Visualization`

```{image} ../images/feb-pytorch-profiler.png
:width: 500
```

Note: A known bug in PyTorch 1.11 may cause a segfault (<kbd>signal 11</kbd>).  Workarounds include using PyTorch 1.09 or <kbd>setting torch.profiler.profile</kbd> parameter <kbd>with_stack=False</kbd>.  See [PyTorch bug report](https://github.com/pytorch/pytorch/issues/69443) for more details).

---
title: Run Experiment
weight: 200
---

# Run Experiment

Luminide runs two types of experiments, *trainings* and *sweeps*.  A training consists of a single run.  A sweep consists of multiple runs, called trials, used to tune hyperparameters.  Both trainings and sweeps can be run up to 10x faster using Luminide's *Early Ranking* technology -- these are referred to as *Fast Trainings* and *Fast Sweeps*, respectively.  This allows for four different combinations:
- **Full Training**: A single training run, executed to completion (see [Run Experiment](run-experiment))
- **Full Sweep**: Hyperparameter tuning with multiple runs, each executed to completion (see [Hyperparameter Tuning](hyperparameter-tuning))
- **Fast Training**: A single training run, but with Early Ranking technology (see [Fast Training](early-ranking))
- **Fast Sweep**: Hyperparameter tuning with multiple runs, but with Early Ranking technology (see [Fast Sweeps](fast-sweeps))

<p></p><hr>

(docs-run-experiment)=
## Run Experiment

Menu: `Luminide > Run Experiment`

To run a Full Training, navigate to the `Train` tab.  Luminide will copy everything in the <kbd>code/</kbd> directory from the IDE Server to the Compute Server, and execute the <kbd>full.sh</kbd> shell script on the Compute Server.

- You can view and edit this script by selecting `Edit full.sh`, e.g. to change the number of epochs to execute.
- Leave the `Track Experiment` box checked to automatically save the results (see  [Experiment Tracking](experiment-tracking) for details).
- If needed, additional <kbd>pip</kbd> or <kbd>apt</kbd> packages can be installed on the Compute Server (see  [Manage Packages](manage-packages) for details).

Once you're ready, click `Start Full Training`. 

```{image} ../images/feb-train.png
:width: 600
```

The output from executing the <kbd>full.sh</kbd> shell script on the Compute Server is displayed in an embedded terminal.

```{image} ../images/feb-training-completed.png
:width: 900
```

When it's done, you will get an <kbd>Experiment Completed</kbd> message and the results will be copied back to the IDE Server, where you can browse them in the [Code File Browser](code-file-browser) or with the [Experiment Tracking](experiment-tracking) feature.  See [Overview](starting-overview) if you have questions about Luminide servers and its file system,

## Custom Scripts

In addition to running experiments (which execute the <kbd>full.sh</kbd> or <kbd>fast.sh</kbd> shell scripts), Luminide can execute any script, e.g. to do data analysis or perform preprocessing.  Choose the `Custom` tab, create or edit a script, and execute it on the Compute Server with the `Start Custom Script` button.

```{image} ../images/feb-custom-script.png
:width: 550
```

The `Track Experiment` checkbox is unchecked by default to avoid clutter.  Check this box you do wish to save the  custom script output.

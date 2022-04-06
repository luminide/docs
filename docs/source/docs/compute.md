---
title: Compute
weight: 110
---

(docs-compute)=
# Compute

(docs-compute-server)=
## Compute Server

This feature allows you to attach or detach to a server and configure its settings.

Menu: `Luminide > Manage Compute Server`

```{image} ../images/feb-compute-server.png
:width: 600
```

## Attach to a Compute Server

Choose which CSP and system you want to use based on their descriptions and hourly rates.  Some CSPs offer "spot compute" for machines that are not in use.  This option is significantly less expensive, but runs the risk of having the machine preempted at any point.  Spot compute can be a great choice when there is a large pool of unused machines.  It's also useful for longer running hyperparameter sweeps, since a preempted sweep can be resumed without losing any results.

Once you've selected your sytem, click `Attach Compute Server`.  This will connect with the CSP, provision a new server, and indicate once this process has completed by displaying a green checkmark (in both the Manage Compute Server tab as well as the bottom-left status bar).  Note -- this step could take several minutes depending on the Compute Server type.

```{image} ../images/feb-status-bar.png
:width: 400
```

## Choosing a volume size

The first time you select a Google compute server, you will need to select a volume size.  This volume is persistent, so you only have to download it once.   When you reattach, it will still be there.

## Idle timeout

The idle timeout controls how long to wait before automatically detaching the compute server.  This avoids paying for cloud compute when there's nothing running on either the IDE or the Compute Server (e.g. after an experiment finishes, or if you simply forget to detach manually when you finish.)  Click on `Edit idle setting` to change the idle timeout.

## Compute Usage

Luminide tracks your usage each time you attach to a compute server.  You can see a history of your usage buy selecting:

Menu: `Luminide > Compute Usage`

Here you will see an itemized list of each session, along with time and costs associated with it.

```{image} ../images/feb-compute-usage.png
:width: 600
```

The bottom left status bar also includes how much remains in your quota:

```{image} ../images/feb-status-bar.png
:width: 400
```

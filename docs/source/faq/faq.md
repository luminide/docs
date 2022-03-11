---
title: FAQ
weight: 1000
---

# FAQ

**During a long-running experiment, what happens if I close my browser or shutdown my machine?** \
Experiments are run on the Compute Server, and will continue to run even if you disconnect from the IDE Server by closing your browser or shutting down your machine.  When you reconnect with the IDE server again, it will in turn reconnect with experiment (in progress or possibly finished).

**How persistent is the code, data, and output?** \
The code, data, and output are persistent.  You can pick up where you left off at any time.  Note, the data only exists on the Compute Server, which is shared between all servers types in the same CSP, but you will have to import the data again if you switch CSPs.

**Will the Compute Server be auto-detached if there is an experiment in progress?** \
No.  The Compute Server is not auto-detached if there is any activity in the system, e.g. an experiment in progress, a data download in progress, the user typing into the IDE.

**Can I get superuser access to the Compute Server?** \
Yes.  The Compute Server is allocated exclusively to each user, therefore you have superuser access to it.

**How do I list/add packages installed on my machine?** \
Use the [Compute Server Terminal](compute-server-terminal).

**How do I run additional git commands?** \
Use the [IDE Server Terminal](ide-server-terminal).


---
title: Terminals
weight: 400
---

# Terminals

(ide-server-terminal)=
## IDE Server Terminal

Menu: `Luminide > IDE Server Terminal`

Opening a terminal on the IDE Server allows you to:
- Run additional git commands such as <kbd>add</kbd>, <kbd>commit</kbd>, <kbd>push</kbd>, and <kbd>pull</kbd>.
- Inspect or modify files in the <kbd>code/</kbd> and <kbd>output/</kbd> directories with Unix commands like <kbd>ls</kbd>, <kbd>du</kbd>, and <kbd>grep</kbd>.

```{image} ../images/ide-server-terminal.png
:width: 450
```

(compute-server-terminal)=
## Compute Server Terminal

Menu: `Luminide > Compute Server Terminal`

Opening a terminal on the Compute Server allows you to:
- List which <kbd>pip</kbd> and <kbd>apt-get</kbd> packages are already installed, or add your own.
- Monitor resource usage during experiments with commands like <kbd>top</kbd>, <kbd>uptime</kbd>, and <kbd>nvidia-smi</kbd>.
<p></p><hr>

```{image} ../images/compute-server-terminal.png
:width: 450
```
Unlike the IDE Server, the Compute Server is allocated exclusively to you.  Therefore, you have full access and control over this machine, including <kbd>sudo</kbd> privileges.

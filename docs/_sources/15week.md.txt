# Week 15 Singularity


![](https://media0.giphy.com/media/3d8mZpR1z4NFy6gIBA/giphy.gif?cid=ecf05e47w26iqr23x2mo46f6qgiia0cx7v6bmpvtsfz49u9t&rid=giphy.gif)

---

> “HPC is just another tool in the toolbox,” he said. “So, what we’re trying to do is get people more comfortable with running large-scale simulations of data analytics and modeling. We want to make that a fabric within USGS so that it changes the culture within the Survey. We don’t want people having to deal with things on their own. We want to make sure everybody has the right tools, or at least good enough tools, to get their jobs done.” - Falgout


- https://www.usgs.gov/center-news/denali-tallgrass-eros-launch-new-era-high-performance-computing-capabilities
---

## HPC

#### I like Tallgrass vs. Denali

1. Because it has singularity for support of containers - more to come


#### Singularity Demo

```
module load singularity

singularity shell docker://ubuntu:latest

singularity run library://sylabsed/examples/lolcow
```
---


### Singularity Features - why was it created?

1. No Root Access in Containers
2. Created for scientists on HPC
3. Integrated volumes
4. Job Scehduling integration with slurm

I was not happy that I had to learn - yet another orchestration tool - let alone two - singularity and slurm

### Singularity Versus pure Docker
> For one, security. HPC environments are typically multi-user systems where users should only have access to their own data.

> For all practical purposes, docker gives superuser privileges. It’s hard to give someone limited Docker access.Sure there’s SELinux and the like, but Docker just wasn’t designed to keep users out of each other’s stuff. Singularity effectively runs as the running user and doesn’t result in elevated access.

> Another is scheduling. On my cluster we use slurm, and users submit jobs with CPU/memory/time requirements. The Docker command is just an API client that talks to the docker daemon, so the resource requests and actual usages don’t match. Singularity runs container processes without a daemon. They just run as child processes.



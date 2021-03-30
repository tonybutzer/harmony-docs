# Week 15 HPC Edition Pangeo + Singularity

## Overview
- around the projects
- datalake experiment
- hpc - denali and tallgrass
    - very similar to cloud 
    - different approach
    - sponsored $$$
        - compute
        - data storage
        - scaling - both have batch
        - rescale?
- pangeo demo on:
    - bigPangeo
    - miniPangeo
    - Tallgrass
- 

https://www.usgs.gov/center-news/denali-tallgrass-eros-launch-new-era-high-performance-computing-capabilities


## Around the Projects

- Logan continues to improve his orchestrated docker containers for downloading H:S and creating NDVI.
- Olena is working on Jupyter to explore the inverse relationship of NDVI and LST (temperature) for tuning Evaporation Models,
- Steffi is looking at ways to do CONUS scale VegET with the cloud and/or HPC (PANGEO-based)
- Tony is exploring Singularity and PANGEO on TALLGRASS - 
- Pat Danielson - is looking at ways to do better, faster, cheaper composites with scalable hardware and linux open-source.


![](https://media0.giphy.com/media/3d8mZpR1z4NFy6gIBA/giphy.gif?cid=ecf05e47w26iqr23x2mo46f6qgiia0cx7v6bmpvtsfz49u9t&rid=giphy.gif)

---

> “HPC is just another tool in the toolbox,” he said. “So, what we’re trying to do is get people more comfortable with running large-scale simulations of data analytics and modeling. We want to make that a fabric within USGS so that it changes the culture within the Survey. We don’t want people having to deal with things on their own. We want to make sure everybody has the right tools, or at least good enough tools, to get their jobs done.” - Falgout

- the right tools
- don't have people try to go this alone - collaborate
- get scientists comfortable with these disruptive scalable environments
- Falgout is on to something here

- https://www.usgs.gov/center-news/denali-tallgrass-eros-launch-new-era-high-performance-computing-capabilities
---

## HPC

#### I like Tallgrass vs. Denali

1. Because it has singularity for support of containers - more to come

#### BUT -->  salloc: Job 1567397 has exceeded its time limit and its allocation has been revoked.


#### Singularity Demo

```
make salloc

make shell




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



```

[butzer@ml-0001 ~]$ singularity shell library://sylabsed/examples/lolcow
Singularity lolcow_latest.sif:~> lolcat --help

Usage: lolcat [OPTION]... [FILE]...

Concatenate FILE(s), or standard input, to standard output.
With no FILE, or when FILE is -, read standard input.

    --spread, -p <f>:   Rainbow spread (default: 3.0)
      --freq, -F <f>:   Rainbow frequency (default: 0.1)
      --seed, -S <i>:   Rainbow seed, 0 = random (default: 0)
       --animate, -a:   Enable psychedelics
  --duration, -d <i>:   Animation duration (default: 12)
     --speed, -s <f>:   Animation speed (default: 20.0)
         --force, -f:   Force color even when stdout is not a tty
       --version, -v:   Print version and exit
          --help, -h:   Show this message

Examples:
  lolcat f - g      Output f's contents, then stdin, then g's contents.
  lolcat            Copy standard input to standard output.
  fortune | lolcat  Display a rainbow cookie.

Report lolcat bugs to <http://www.github.org/busyloop/lolcat/issues>
lolcat home page: <http://www.github.org/busyloop/lolcat/>
Report lolcat translation bugs to <http://speaklolcat.com/>

Singularity lolcow_latest.sif:~> which lolcat
/usr/games/lolcat
Singularity lolcow_latest.sif:~> cowsay -f tux  hello there | lolcat -a
 _____________
< hello there >
 -------------
   \
    \
        .--.
       |o_o |
       |:_/ |
      //   \ \
     (|     | )
    /'\_   _/`\
    \___)=(___/
```

- tony says - 'oh yeah what do you use your supercomputer for'


#### HPC DOC Walk Thru

[https://hpcportal.cr.usgs.gov/hpc-user-docs/Resources/Cheat_Sheets.html](https://hpcportal.cr.usgs.gov/hpc-user-docs/Resources/Cheat_Sheets.html)


[https://vim.rtorr.com/](https://vim.rtorr.com/)


[https://cheatography.com/davechild/cheat-sheets/linux-command-line/](https://cheatography.com/davechild/cheat-sheets/linux-command-line/)

### Big Data and Data Cubes

> " Developments of sensing observations and producing information from it need to be accompanied by suitable storage, processing and retrieval systems. " - from ...
[https://www.tandfonline.com/doi/full/10.1080/17538947.2019.1585976](https://www.tandfonline.com/doi/full/10.1080/17538947.2019.1585976)


## Data Lake Discussion - Demo

- copied data from Neal's bucket eco-w1 to Caldera
- copied anhb nlcd fro Caldera to a usgsOPEN-bucket ... dev-et-data -- aka Steffie's bucket.

- demo access from Steffie's private mini-pangeo - http:/10.12.68.246
- demo access from theBigPangeo -- http://pangeo.chs.usgs.gov
- demo local Caldera access from Jupyter via Tallgrass

```
tallgrass

make salloc

make shell

(start jupyter)

tunnel 8888

http://localhost:8888

```


## Show STAC - for maine and clipping and crs from plateCarree

- find this demo - do it in the pangeo
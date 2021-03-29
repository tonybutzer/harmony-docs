# HPC Notes


## Useful References




https://www.hpc.iastate.edu/guides/containers


https://ioos.github.io/notebooks_demos/other_resources/

https://www.usgs.gov/core-science-systems/sas/arc

https://www.usgs.gov/mission-areas/core-science-systems

https://hpcportal.cr.usgs.gov/hpc-user-docs/jobs/best-practices.html

https://pubs.cray.com/bundle/XC_Series_Programming_Environment_User_Guide_1705_S-2529/page/SLURM_in_Interactive_Mode.html


## Useless References

https://hpcportal.cr.usgs.gov/hpc-user-docs/Resources/training_classes.html


## Useful Videos

- Slurm Basics
    - https://www.youtube.com/watch?v=49DzPT9HFJM

https://www.google.com/search?client=firefox-b-1-d&q=slurm+for+dummies+youtube+hpc


## Useless Videos




## Login Nodes and Transfer Nodes


## PANGEO Journey

### Install and Test Miniconda

https://pangeo.io/setup_guides/hpc.html


#### Logon your hpc system now

- tallgrass - my favorite 
- salloc and bash in new run node
- install miniconda


```
mkdir opt/mini
cd opt/minu

wget https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86_64.sh
chmod +x Miniconda3-latest-Linux-x86_64.sh
./Miniconda3-latest-Linux-x86_64.sh


conda update conda

```

---



### Signell Help

Follow this recipe and let me know if it works for you: https://discourse.holoviz.org/t/setting-up-working-environment-for-tutorial/1794/4

### from conda env base

```
cd /home/butzer/opt/etscrum/2_ET_HPC/signell



conda config --add channels conda-forge --force
source activate base
conda install mamba -y
mamba env create -f pangeo_env.yml

```


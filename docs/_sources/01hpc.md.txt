# HPC Notes


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

```


### Signell Help

Follow this recipe and let me know if it works for you: https://discourse.holoviz.org/t/setting-up-working-environment-for-tutorial/1794/4

### from conda env base
```
conda install mamba
```


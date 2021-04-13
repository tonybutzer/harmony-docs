# Week 16 - Welcome Landfire

Today we welcome the Landfire, FireScience team to this community of best practices and this community of sharing, notebooks, concepts, code , data and most importantly - non-silo-ed talent. Welcome Tolk, Brian (Contractor) L  -- and Degaga, Erica J
 
## What is this class?
1. A community of cloud based Scientists that:
    - use the cloud
    - some have custom cloud accounts
    - some use the Landsat account
    - some use thebigPangeo
    - some have their own mini-Pangeos/jupyterHubs/sandboxes
    - 
2. Notable technologies
    - Python
    - Open Source
    - Image Processing and GIS
        - xarray, pandas, matplotlib, holoviews, geoviews, geopandas, rasterio, GDAL
3. Remote Sensing Cloud Stored assets
    - Landsat - utm/albers/ ---> ARD tiles
    - Sentinel-2-COGs
    - Hamonized Landsat Sentinel
4. Makeing birds-f-a-feather connections in science
5. focus on TRAINING - lets have a highly TRAINED Science team and a world class data center
    - start with simple get togethers - this class
    - jot some disorganized notes
    - share some draft notebooks
    - stuff code and docs in github
    - hire an intern to organize and collate this stuff
    - repitition
    - learn how to use git search in the meantime
    - reach out and ask for help - connectors include Rich Signell, Nathan, Aaron Friesz, tony ....

## Teams
1. Evapotranspiration -- Water - Steffi, Olena
2. Land Cover - Brett, Pat, Kory
3. LCMAP - Kelcy
4. Invasive - Sujan, Devandra, Logan, Neal
5. Web Development Team - Claudia, Maxwell, Michelle, Balu ...
6. VegDyn - Trent, Dinesh
7. Emerging AI experts ...


> Basically, ostensibly- lots of superior TALENT

## A group of experts 

- here are just a few - there are many i have not enumerated and some i have not yet discovered

1. Logan Megard - HLS -- DevOps
2. Steffi Kagone - Converting Models from ARCPY to rasterio
3. Olena Boiko - Data Wrangling Expert - MOdel QA Expert - Jupyter/matplotlib
4. Kelcy Smith - Python Expert, Jupyter Expert, time-series expert - STAC expert
5. Nathan Roberts - user service - data management 
6. tony - DevOps and OpenDataCube, docker, code portability, networking and file transfers

## Today
Today I am privileged to have guest instructors:
Kagone, Stefanie (Contractor) -- and -- Boiko, Olena are back for an encore lesson on how to use the bigPangeo - pangeo.chs.usgs.gov to look at refining the sophistication of the model by improving the fidelity of NDVI.  
 
also ...
Danielson, Patrick (Contractor) -- and -- Postma, Kory (Contractor) will give an opinionated demo of a notebook on STAC meets one of the mature STAC Catalogs for Sentinel-2-COGs.
 
We can talk a little about the data wrangling and scp and rclone we have been doing between the Netapp, Caldera and S3.
 
And we can talk about finding Albers Scenes for Landsat Compositing using the young, immature Landsat Stac Catalog.
 
Nathan Roberts and Rich Signell are both presenting Pangeo/OpenDataCube papers at conferences this month.
 
So the folks attending this class are Early Adopters of technology and infrastructure stacks that will revolutionize science in the next few years.

# Prepare the Pangeo - release the kracken
# start the pangeo tony START IT
- [https://pangeo.cr.usgs.gov](https://pangeo.cr.usgs.gov)
 

# Overview

## Steffi and Olena
#### Modis derived NDVI an Land Surface Temperature
- Uses the big pangeo
- uses R**2 to evaluate hypothesis
- ran in a $200 mini-pangeo - now runs in the freeFREEfree https://pangeo.chs.usgs.gov

## Pat and Kory
- so far many have come up to speed with Jupyter Lab/Notebook quickly
    - The ability to share snippets of code, concepts, visualizations - is a gamechanger
    - Jupyter is not a full-blown IDE - i say so what!
- these few weeks will look at composites with HLS, sentinel and Landsat - starting with data discover via STAC.

## Make friends with git
- https:/code.usgs.gov


## quit hiding your code and data -
### From Kindergarten

```
Share everything.

Play fair.

Don’t hit people.

Put things back where you found them.

Clean up your own mess.

Don’t take things that aren’t yours.

Say you’re sorry when you hurt somebody.

Wash your hands before you eat.
```


## Landsat Albers by way of BT detour.



## Data transfer - how do I get my data to and from the cloud 
- to is always free
- from can come with egress costs unless
    - you use rclone or some other sneaky method

- we were able to get these rates
    - 40 MBytes per second from cladera --> s3
    - 2 Mbytes per second using VDI machines for most transfers
    - .5 Mbytes when using windows and the VPN/PulseSecure

- we have played with many fileTransfer agents
    - tony's favorites are scp and rclone and perhaps some of their derivatives - like lftp
    - more to come - more help available ....


## Question of the Week - Partial Git Clones

```bash
#! /bin/bash

function git_sparse_clone() (
  rurl="$1" localdir="$2" && shift 2

  mkdir -p "$localdir"
  git config core.sparseCheckout true

  # Loops over remaining args
  for i; do
    echo "$i" >> .git/info/sparse-checkout
```

### use wget for single notebooks

1. find the raw link in github 
    - https://raw.githubusercontent.com/tonybutzer/composite/main/01-danielson/1_LANDSAT_ALBERS_MAINE/0_maine_landsat_albers.ipynb

```
wget https://raw.githubusercontent.com/tonybutzer/composite/main/01-danielson/1_LANDSAT_ALBERS_MAINE/0_maine_landsat_albers.ipynb
```

### Costs

```
ubuntu@ip-10-12-68-246:~$ docker run tbutzer/aws-price python awsprice.py butzer
['awsprice.py', 'butzer']
butzer
     state                     name            ip       i_type  monthly_cost
0  running  butzer-et-mini-pangeo-0  10.12.68.246  t3a.2xlarge       219.584
1  stopped        butzer-bigsship-0   10.12.69.45  m5a.4xlarge       502.240
2  running       butzer-tendollar-a  10.12.68.236     t2.micro         8.468
==========================================================================================
==========================================================================================
     state                     name            ip       i_type  monthly_cost
0  running  butzer-et-mini-pangeo-0  10.12.68.246  t3a.2xlarge       219.584
2  running       butzer-tendollar-a  10.12.68.236     t2.micro         8.468
========================================================================================================================
=====================================================================
```

[Harry House on Cost - The truthful answer to this question is “it’s complex, and it depends.](https://support.chs.usgs.gov/pages/viewpage.action?pageId=40370588)

---
# Week 11

> "One of the advantages of doing science in general in the cloud is the potential to facilitate interagency collaboration in terms of people and data sets. That is a fundamental objective of new analysis environments coming on the scene, such as PANGEO and Open Data Cube. And because these are open source, they can operate on any cloud or on-prem platform. In late 2019, we (NLI, EROS, and CHS folks) began discussing these kinds of joint development opportunities with NASA and NOAA, which are continuing. That’s a pretty exciting prospect for EROS.” -- Pete Doucette 

---
![https://www.usgs.gov/center-news/doucette-discusses-future-eros-science-earthmap-new-branch-chief](https://www.usgs.gov/center-news/doucette-discusses-future-eros-science-earthmap-new-branch-chief)

## Now a word from ssh - its the key to every door

### ssh keys

- nice article here
- [https://www.digitalocean.com/community/tutorials/ssh-essentials-working-with-ssh-servers-clients-and-keys](https://www.digitalocean.com/community/tutorials/ssh-essentials-working-with-ssh-servers-clients-and-keys)


#### SSH Summary

- SSH is a secure protocol used as the primary means of connecting to Linux servers remotely.
    - and github and gitlab -- code.usgs.gov
- SSH is a secure protocol used as the primary means of connecting to Linux servers remotely.
- you will be dropped into a shell session, which is a text-based interface where you can interact with your server.
- Clients generally authenticate either using passwords (less secure and not recommended) or SSH keys, which are very secure.
    - I miss usercode and password - sometimes
- SSH keys are a matching set of cryptographic keys which can be used for authentication.
    - public --- share with everyone
    - private - never share or you will get in trouble


- ssh-keygen ---- # generates a key pair PAIR
    - ~/.ssh/id_rsa: The private key. DO NOT SHARE THIS FILE!
    - ~/.ssh/id_rsa.pub: The associated public key. This can be shared freely without consequence.

#### Where they go
- the public key must be copied to a file within the user’s home directory at `~/.ssh/authorized_keys`
- or in a github/gitlab - central repository  using settings --> keys ... 
#### They look like this

```
tony@jose ~ $ cat ~/.ssh/id_rsa.pub
ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQDcy3arx6+bW7LIVtgRgkfB/1tGieIVt6Id90qMnve2kRBBK3qlzEFgtwIsl8Io8Rr9Ip3e0apJQwSw3rTXkLd11J6xDLjkRBKWU2jsaYOn8iSfbaHT5JHMEAfTEZ49AELjdMNSBTb0TYw/cmKE9bLNMchmYNvfPnCidv/TakOY+DB1ZdSfDgI+NKoPZQ+Y9sK4Hl8xIEevwR2C0oP7S4+ekU9Fd3tx34R66vDyeCQeJItFp9Q1a7mW+wmulafAdr/Y3vxcEe4ArCPsDRgs8ElT0mrYD7csXZGNjqBxmSe/rNvknD/byE7SgMWvodWOpWRdN8/0eHzSsPJ1zvfnAW49 tony@jose
```

#### The belong here
- the public key must be copied to a file within the user’s home directory at `~/.ssh/authorized_keys`
- or in a github/gitlab - central repository  using settings --> keys ... 

- 


## Github and code.usgs.gov

### Create a repo - add a file - edit a file - git add - git push

### Windows Git Tools
- git bash
- git gui tools
- pycharm git integration - IDE based

## HLS - Next WEEK
![a](https://cdn.earthdata.nasa.gov/conduit/upload/14905/CMR_Overview.png)
## Brave Sir Logan and The CMR 
- Common Metadata Repository (CMR) - Earthdata - NASA
- Logan says register here:
    - I think you just need an earth data log in 
    - https://urs.earthdata.nasa.gov/


## geojson.io and google - measure distances - klm 

- demo cut and paste into geojson.io
- talk about importing as a kml in google maps
- all you need is a chromebook to do science.


[https://www.google.com/maps/d/?hl=en](https://www.google.com/maps/d/?hl=en)


### HLS GRID

![hls](./Assets/hls-grid-conus.PNG)


---
## Sentinel
- klm grid and google maps

![a](https://dragon3.esa.int/documents/247904/266366/Sentinel-2-MSI_Product_Types_Figure_1_v3/262f604c-de1e-4cf7-b4f6-abdd7f0dc5fd?t=1523262257162)

## Composite Work

### Pangeo Startup Sequence

![pang](./Assets/pangeo-k8s-startup-event-log.PNG)


---
## Landsat-8 TOA
## Simple Animations using Landsat-8 TOA


---
## Denali integration Scenarios

- composite on AWS --- Characterize on Denali or Tallgrass
- Water Evaporation and Runoff on AWS --- Evaluate Water Balance Model fidelity on Denali using Stream Guage Data

    - brand new USGS `Landsat Collection2` - Surface Reflectance in UTM
        - coming soon Albers
    - Experimental `Harmonized Landsat-Sentinel`
    - nearFuture Suomi NPP will carry five science instruments 
        - Suomi NPP is the first satellite mission to address the challenge of acquiring a wide range of land, ocean, and atmospheric measurements 
- Synergies with google maps and geojson.io
- NO LICENSE FEES

# Week 10 - We are Really on to Something Here:

### A lot to cover today

- Remember: - Tony does topical small sessions on specific topics as part of the Pangeo/Open Data Cube outreach project

- synergies between the cloud and hpc
- high speed data movement
- Remote Sensing Catalogs of pixels at our service
    - `Sentinel` L2A
    - old Landsat 8 TOA
    - brand new USGS `Landsat Collection2` - Surface Reflectance in UTM
        - coming soon Albers
    - Experimental `Harmonized Landsat-Sentinel`
    - nearFuture Suomi NPP will carry five science instruments 
        - Suomi NPP is the first satellite mission to address the challenge of acquiring a wide range of land, ocean, and atmospheric measurements 
- Synergies with google maps and geojson.io
- NO LICENSE FEES
- A support group and a PANGEO community with really smart people to cheat off
- A talented pool of folks from SD Universities - pride
- Scientists with noble missions - wonderful!
- We can write `our own apps` that do just what we want them to do!
- get rid of WINDOWS and all of its poor engineering.
- tell Claudia - we can and do run PANGEOi/jupyter on Denali and Tallgrass


## HLS
![a](https://cdn.earthdata.nasa.gov/conduit/upload/14905/CMR_Overview.png)
## Brave Sir Logan and The CMR 
- Common Metadata Repository (CMR) - Earthdata - NASA
- Logan says register here:
    - I think you just need an earth data log in 
    - https://urs.earthdata.nasa.gov/


[https://www.google.com/maps/d/?hl=en](https://www.google.com/maps/d/?hl=en)


## Sentinel
- klm grid and google maps

![a](https://dragon3.esa.int/documents/247904/266366/Sentinel-2-MSI_Product_Types_Figure_1_v3/262f604c-de1e-4cf7-b4f6-abdd7f0dc5fd?t=1523262257162)

## Composite Work

### Pangeo Startup Sequence

![pang](./Assets/pangeo-k8s-startup-event-log.PNG)


## 
## Simple Animations using Landsat-8 TOC


## Denali integration Scenarios

- composite on AWS --- Characterize on Denali or Tallgrass
- Water Evaporation and Runoff on AWS --- Evaluate Water Balance Model fidelity on Denali using Stream Guage Data

## scp push and pull

- scp push from cloud to denali - 20 MB/sec
- scp push from desktop/vpn to cloud - .08 MB/sec
    - likely better performance from the VDI to and from the
        - ssh keys are easy after you create and add them a few times - esp. on linux


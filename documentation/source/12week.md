---
# Week 12

> "This consequently facilitates the conversion of space-based Earth Observation information into actionable knowledge for a better response to the complex global change processes we are currently dealing with.
Technological advances happen quick and now with cloud infrastructures we have the unprecedented means to make such deep integration possible. However, transforming an established operational setup, such as was developed and used for the Global Land Service over the years, to another completely new and technological challenging cloud computing environment is not a trivial job. Especially considering that many production chains need to be decomposed into modular bits and pieces which then have to be newly forged into a smooth and fully integrated machinery to provide the user with a transparent, yet integrated, set of tools.
The scope of this report is to tackle exactly this: providing clear suggestions for an efficient ‘cloudification’ of the Copernicus global land production lines and user interfaces, and investigating if there is a tangible benefit and what would be the effort involved." -- Opening new horizons: How to migrate
the Copernicus Global Land Service to a Cloud environment


## Class Recap

- Still attacking data wrangling
- people should get friendly with github/gitlab -- code.usgs.gov
- 

### References

#### If the Mask fits .. understand it
[https://rasterio.readthedocs.io/en/latest/topics/masks.html](https://rasterio.readthedocs.io/en/latest/topics/masks.html)

### Nice Tutorials - Guest Teacher of the Week

- [https://www.earthdatascience.org/courses/use-data-open-source-python/multispectral-remote-sensing/landsat-in-Python/](https://www.earthdatascience.org/courses/use-data-open-source-python/multispectral-remote-sensing/landsat-in-Python/)
- Pat Danielson - volunteer

## Projections and Geoviews
[https://geoviews.org/user_guide/Projections.html](https://geoviews.org/user_guide/Projections.html)


## Kelcy Notebook

[https://code.usgs.gov/klsmith/pangeo-examples/-/blob/master/lcmap-time-series-ccd.ipynb](https://code.usgs.gov/klsmith/pangeo-examples/-/blob/master/lcmap-time-series-ccd.ipynb)



## What's Happening in Pangeo Land

- ECO team will continue to get high speed data access to HLS
    - we have just scratched the surface on how to scale
    - looking for an open source, xarray perhaps, solution to mosiacing like ARCMAP
        - needs to handle overlapping scenes intelligently
- Scotty H - has lots of great tutorials - a little over my head - but i'm learning.
- DataLake 
    - interim - s3://dev-et-data/data-lake - can access it from pangeo.cr.usgs.gov
    - Now that Kristi Kline is on the case we may get more attention on a USGS cloud S3 based Data Lake.
- Binder is pretty cool - more free pangeo compute - 
- The scientist is the critical resource on the planet - never compute


## Direct acyclic Graphs

- used in DASK
- consists of vertices and edges (also called arcs), with each edge directed from one vertex to another, such that following those directions will never form a closed loop.

![dag](https://upload.wikimedia.org/wikipedia/commons/thumb/f/fe/Tred-G.svg/440px-Tred-G.svg.png)

## Data Wrangling Working Group

## Data Lake Work

- Class A Data Assets
    - Landsat Collection-2
    - Sentinel Cogs
    - Harmonized Landsat Sentinel (1.5)

- Class B Data Assets
    - NLCD
    - LCMAP Products

- Class C Data Assets
    - Soil ...

Concepts:
   - shared data - makes less wrangling
   - shared python code - allows reuse
   - cross-project communication - breaks silos and diverse teams build better solutions
   - data deluge is coming - lets be ready to filter and use what we want
        
        
    
# Signell Reading List

- https://github.com/pangeo-data/cog-best-practices
- https://github.com/intake/intake-stac/tree/main/examples    
        

---

### Pangeo Startup Sequence

![pang](./Assets/pangeo-k8s-startup-event-log.PNG)


---

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


# WEEK 6 - Case Studies ECO & ET

The subjects include:

- phenology - dashboards are nifty.
- machine learning with Tensorflow - what kind of shoe is this?
- evaporation and transpiration for 150 flippin years -- NO SWEAT!
- orchestration - its not just for clarinets and violins
- how to cheat at AWS S3 bucketology with import fsspec

## Birds-of-a-feather groupings
#### Phenology
[https://afternoon-crag-97068.herokuapp.com/](https://afternoon-crag-97068.herokuapp.com/)
- *Points*
    - python app written in Plotly Dash
    - phenology based on landcover
    - interactive - good responsiveness
    - serverless - heroku, binder, AWS lambda - AWS Batch(quasi)
- more to come.
    - next week a discussion on HLS - NDVI Dev/Logan/Mike
    - Creating NDVI with Landsat 8 - public data sets and Xarray

#### Tensorflow
[http://10.12.68.150:8080/tree/tensorflow-tutorials](http://10.12.68.150:8080/tree/tensorflow-tutorials)
- Run from a container on the mini-pangeo
- Training example shoes and shirts
- The sandal looks like a sneaker to me
- Movie sentiment analysis
- tensorflow for dummies - on kbr - skillport - free free free
- Machine learning research to be actively funded by USGS - Sunne has teh contact -

```
/opt/logan/tools/tensorflow$ more Makefile

        docker run -it -p 8080:8888 tensorflow/tensorflow:nightly-jupyter
```


## Case Studies Eco - Data Wrangling

- RAPV2
- HLS
- MRLZ - unzip pipeline

[https://rangelands.app](https://rangelands.app)


### Data Pipelines and Orchestration
[etm-conductor-orchestration-v2](https://github.com/tonybutzer/etm/blob/master/02-orchestration-launcher/etm-conductor-orchestration-v2.py)


## Docker

- demo cog generation from sapv2 tif
- demo unzip convert from .img and make cog mrlc-BITv3 
- both of these from custom docker containers and simple docker heuristics

### Viz app for etasw
[http://10.12.68.246/user/butzer/notebooks/opt/etviz/0-application-et-view/99-vrt-fail.ipynb#](http://10.12.68.246/user/butzer/notebooks/opt/etviz/0-application-et-view/99-vrt-fail.ipynb#)


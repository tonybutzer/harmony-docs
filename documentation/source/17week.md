# Week 17 Google Cloud and AWS Oh My

- so many technical options and choices - so little time.

## Future Classes
1. Logan - HLS experiments for ECO-invasive
2. Aaron - s3 direct access LPDAAC HLS
3. Kelcy - time series landsat
4. Pat Danielson, Kory, Brett, Brian Tolk -- Compositing - NLCD and FireScience


[https://github.com/tonybutzer/et/blob/master/docs/source/00status.md](https://github.com/tonybutzer/et/blob/master/docs/source/00status.md)

- https://github.com/tonybutzer/et/blob/master/docs/source/00status.md

## Demo Overview

1. Look at google cloud bucket assets - ssebop
2. demo how to replicate/sync/copy those to our AWS DataLake
3. demo using docker to build an image for gsutil -- google utility
4. demo running the container on AWS
5. demo running the container/sif on Tallgrass
6. demo looking at the tif file with Pangeo on tallgrass via ssh tunnel of port 8888

---
1. redo Nate's Waubay for albers and rgb
    - composite repo?

- https://console.cloud.google.com/storage/browser/ssebop-modis/Annual
## Rclone Examples

- tony --> umyssh minipangeo

```
 1984  cat Dockerfile
 1985  cat Makefile
 1986  cd
 1987  ls
 1988  rclone config
 1989  ls
 1990  rclone listremotes
 1991  rclone config
 1992  rlone ls sbop:/ssebop-modis/
 1993  rclone ls sbop:/ssebop-modis/
 1994  rclone sync -P sbop:/ssebop-modis/Annual et-data:/dev-et-data/datalake/ssebop-modis/Annual/
 1995  aws s3 ls dev-et-data/datalake/ssebop-modis/Annual/
 1996  aws s3 ls dev-et-data/datalake/ssebop-modis/Annual/ --human
 1997  gdalinfo /vsis3/dev-et-data/datalake/ssebop-modis/Annual/y2003_modisSSEBopETv4_actual_mm.tif
 1998  ls
 1999  ls -l
 2000  rclone listremotes
 2001  rclone ls sbop:/ssebop-modis
 2002  rclone ls sbop:/ssebop-modis --help
 2003  rclone lsjson sbop:/ssebop-modis
 2004  rclone lsjson sbop:/ssebop-modis/Annual
 2005  rclone ls sbop:/ssebop-modis/Annual
 2006  history
```

## ARCPY vs. Open Source


## Databases are so yesterday

## But if you insist on postgres
### I am talking to you OpenDataCube

- THEN - at least use docker to minimize the PAIN!

```
ubuntu@ip-10-12-68-246:/opt/cube-in-a-box$ more docker-compose.yml
version: '3'

services:
  postgres:
    image: postgis/postgis:10-2.5
    environment:
      - POSTGRES_DB=opendatacube
      - POSTGRES_PASSWORD=opendatacubepassword
      - POSTGRES_USER=opendatacube
    ports:
      - 5432:5432
    restart: always

  jupyter:
    build: .
    environment:
      - DB_HOSTNAME=postgres
      - DB_USERNAME=opendatacube
      - DB_PASSWORD=opendatacubepassword
      - DB_DATABASE=opendatacube
      - AWS_NO_SIGN_REQUEST=true
      - STAC_API_URL=https://earth-search.aws.element84.com/v0/
    ports:
      - "8080:8888"
    volumes:
      - ./notebooks:/notebooks
    restart: always
    command: jupyter notebook --allow-root --ip="0.0.0.0" --NotebookApp.token='secretpassword'
```

## What does a world class data center look like?

1. lean and agile
2. Highly TRAINED
3. communicates across informal channels
4. Common Goal - effective use of the planet's limited resources - 
5. A world or universe view
6. fosters the right CULTURE
    - sharing and confidence
    - respects each other's expertise
    - has each other's back
    - has fun at work
    - rejects management styles that don't inspire

## These classes propose PANGEO as a way for science
- Open Data Cube - is an instance of PANGEO
    - its database for me represents a barrier to entry
    - that said its a cool and powerful abstraction for building xarray timeseries applications that run in Pangeos

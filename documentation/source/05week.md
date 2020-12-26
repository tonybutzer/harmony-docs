
# WEEK 5 - Data Wrangling is Underway - Understanding S3

## No silos; No Silos; NO SILOS!
- lets work together
- "many hands make light work"


## Understanding COGs and NonCOGs
- data sizes and overviews


### A word about Data Compression

---

Below is a summary of the compression ratios of each method in the worst case: 
- 10-meter Sentinel-2 bands, 
- internal tiling and overviews.
---

| method | Compression Ration | Reason to use |
| ------| -----------| ---------------------|
| LZW 	| 1.16:1 | Quick to run and easy to adopt |
| DEFLATE | 1.38:1 | A slower but better performing alternative to LZW |
| ZSTD 	| 1.45:1 | Promising, CPU intensive but not mature |

    Table. Summary of the results of the different compression algorithms

---


### Email from my OpenDataCube Tasmanian Friend

Hey Tony

And hey Jeff [Briden] and Jon [Morton] of {LCMAP FAME}

Happy to talk about how we do ODC work in the cloud, including doing continental-scale data processing work.

We have some neat new examples using AWS tools like their Simple Queue Service along with Kubernetes to run a whole of Africa pixel quality analysis (so just visiting Sentinel-2's SCL band, over all pixels over Africa) and we're able to process that on 5 large EC2 instances in `~20 minutes, which is fun! Costs us $20 USD.`

Our land cover folks are doing something similar in Australia with LCCS, and I could bring them along. `They're science users, and are happy working with Python and the ODC` along with Kubernetes and job queues to run through that analysis, including iterating quite fast. I'm not sure about the costings of that, but it's been really successful this year!

So yes, happy to talk some time in the new year. Might need to be late Jan when we're all back on board!

Cheers,

---

## IT Security and Compliance Part II

- lower server footprint and vulnerability attack surface
- reduce user numbers in my Landsat mini-pangeos
- migrate users to big pangeo; teach cookbook examples in the Big Pangeo
- migrate eco users to the eco VPC mini-pangeo
- add encryption where i have to - or decomission less important services
- kelcy - where do you author notebooks? - use teams

### IT Security Goal
> Improve IT Security Compliance - with minor impacts to creativity, scaling and science

---

### The Oregon Pronunciation Conundrum - perhaps we should move to us-east-1
- because that is in Virginia
- I found out the 53% of the folks use the fake-pronunciation for Oregon
	- I am glad I am in the 12% who actually get it right. :-)
	- I am thinking about starting a Facebook campaign

![](Assets/AURA-gun.PNG)


- organ trail?
- or-AGAIN


**My friend once told me "You must be the most pedantic person in the entire world."**
- "Third most, actually." -- :-)

---

## Logan Data Wrangling, S3 and early validation notebooks
- S3 buckets view from the AWS Console
- Quick Sanity Check of NED Data
- in0 --> in1 (COGs) Model Ready Data Perhaps   `s3://eco-w1/in0/rapv2`; etc ....

## Wrangle rapv2 and mrlc_zip
- next week we will use the cloud to create COGs from these in parallel - via docker orchestration

- https://github.com/tonybutzer/logan/blob/main/00-notebooks/00-portal-scraping/00-MRLC-Notebooks/00-data-scraping-grab-zips.ipynb
- [LINK HERE](https://github.com/tonybutzer/logan/blob/main/00-notebooks/00-portal-scraping/00-MRLC-Notebooks/00-data-scraping-grab-zips.ipynb)

## Featured Notebook in Big Pangeo pangeo.chs.usgs.gov

- Steve Labahn got a Pangeo account at the click of a button
- This is a managed service and there are benefits - since many items are taken care of.
- I think you can request a bucket to go with your user ???
- You can definitely play with notebooks here

[ simple example plots big pangeo here](https://pangeo.chs.usgs.gov/user/butzer@contractor.usgs.gov/notebooks/opt/Oldstuff/notebook/00-Tutorial/01-Basic-Plotting-Python/00-example-plots-tony.ipynb)

## IAM - things you will never, ever, need to know - Whew!
- but if you do there's an app for that - I mean a Jupyter Notebook for that!
- aws iam list-attached-role-policies --role-name lsds-developer-ec2
- Jupyter notebooks simplify every complex concept :-)

---

## END of WEEK 5
---


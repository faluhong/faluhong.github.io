---
layout: archive
title: "Research Interests"
permalink: /research/
author_profile: true
---


<!-- # Research Interests -->

**Remote sensing, land use and land cover change, land change model, urbanization, impervious surface, machine learning, urban heat island, land surface temperature**
<br>
<br>

# Research Experiences
## *Current projects for PhD*
### [1] Monitoring and forecasting the forest change in Haiti and Dominican Republic 
* Use all available Landsat data to detect the land cover change in Haiti and Dominican Republic.
* Generate the annual land cover data to analyze the primary and secondary forest change.
* Simulating the historical and future land cover change with land change model.

### [2] Continuous estimation of impervious surface percentage (ISP)
* Employ the very-high-resolution land cover data to create the ISP map.
* Train the convolution neural network with the ISP map and CCDC (Continuous Change Detection and Classification) algorithm outputs.
* Generate the 30-meter resolution ISP dataset over an extensive scale.

## *Previous projects*
### [3] Global seamless daily mean land surface temperature generation
* Enhancement of annual temperature cycle model by combining reanalysis data.
* Design a framework (IADTC framework) to generate physically true daily mean land surface temperature by combining the diurnal and annual temperature cycle models.
* Generate global daily mean LST from 2003 to 2019 and characterize the global LST trend.
* Validate the generated products with widely-distributed *in-situ* measurements. 
* The code of the IADTC framework is available at: [IADTC github](https://github.com/faluhong/IADTC-framework). The generated dataset is freely available at [zenodo](https://zenodo.org/record/6287052)
* Related publication: [Framework: Hong et al., 2021](https://www.sciencedirect.com/science/article/pii/S0034425721003321); [Products: Hong et a., 2022](https://essd.copernicus.org/articles/14/3091/2022/)

**Flowchart of the IADTC framework**
<br>
![IADTC framework](/images/2021_daily_mean_LST_framework.jpg){:height="65%" width="65%"}
<br>

**Global LST trend from 2003 to 2019 using the cloud-free MODIS LST and generated IADTC products**
![IADTC framework](/images/Global_LST_trend_2003_2019.jpg){:height="70%" width="70%"}


### [4] Evaluations of diurnal land surface temperature cycle (DTC) models under clear-sky	
* Obtain nine representative four-parameter DTC models with a set of parameter-reduction strategies.
* Comprehensive assessment of the DTC models with geostationary satellite data and in-situ measurements.
* Provide the parameter-reduction order and the best-performance four-parameter DTC model.
* The examples of the DTC models are available at: [DTC github](https://github.com/faluhong/ATC-and-DTC-Code)
* Related publication: [Hong et al., 2008](https://www.sciencedirect.com/science/article/pii/S0924271618301710)

**Hourly RMSEs of the selcted nine four-parameter DTC models**
![image_four_parameter_DTC](/images/MSG-SEVIRI_four_points.png)











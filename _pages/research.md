---
layout: archive
title: "Research Interests"
permalink: /research/
author_profile: true
---


<!-- # Research Interests -->

**Remote sensing, land cover and land use change, land change simulation, deforestation, biodiversity, urbanization, impervious surface, machine learning, urban heat island, land surface temperature**
<br>
<br>

# Research Experiences
## *Current projects for PhD*
### [1] Decoding primary forest (PF) change in Haiti and the Dominican Republic 
* Use all available Landsat data and COLD (COtinous Monitoring of Land Disturbance) algorithm to map PF change in Haiti and the Dominican Republic.
* Comprehensively compare the PF status between Haiti and the Dominican Republic, including change inside and outside protected areas, PF topography characteristics and fragmentation level.
* Quantify the PF loss area caused by fire, tree-cutting, and hurricanes.
* Related [Publication](https://www.sciencedirect.com/science/article/pii/S0034425724006163), [Code](https://github.com/faluhong/hispaniola_land_cover_mapping), and [Dataset](https://doi.org/10.6084/m9.figshare.28100408).
* The generated map can be view interactively in Google Earth Engine ([Hispaniola Land Cover](https://gers.users.earthengine.app/view/hispaniola-lc)).
<br>
[![GEE Hispaniola LC](/images/GEE_Hispaniola_LC.jpg)](https://gers.users.earthengine.app/view/hispaniola-lc)
<br>
<br>
**Flowchart of mapping primary forest in Haiti and the Dominican Republic**
<br>
![Hispaniola LC](/images/Hispaniola_LC_flowchart.jpg){:height="85%" width="85%"}
<br>

### [2] Estimate the biodiversity extinction risk using land change simulation
* Simulate the historical and future land change in Haiti and the Dominican Republic.
* Link the land change with the biodiversity extinction risk.

### [3] Continuous mapping of impervious surface percentage (ISP)
* Employ massive very-high-resolution land cover data to create the ISP map for training. 
* Train the convolution neural network with the ISP map and COLD algorithm outputs.
* Generate the 30-meter resolution ISP dataset over an extensive scale.

## *Previous projects for Master*
### [4] Generation of global seamless daily mean land surface temperature (LST) dataset
* Enhancement of annual temperature cycle model by combining reanalysis data.
* Design a framework (IADTC framework) to generate physically true daily mean land surface temperature by combining the diurnal and annual temperature cycle models.
* Generate global daily mean LST from 2003 to 2019 and characterize the global LST trend.
* Validate the generated products with widely-distributed _in-situ_ measurements. 
* The code of the IADTC framework is available at: [IADTC GitHub](https://github.com/faluhong/IADTC-framework). The generated dataset is freely available at [Zenodo](https://zenodo.org/record/6287052).
* Related publication: [Framework: Hong et al., 2021](https://www.sciencedirect.com/science/article/pii/S0034425721003321); [Dataset: Hong et a., 2022](https://essd.copernicus.org/articles/14/3091/2022/).

**Flowchart of the IADTC framework**
<br>
![IADTC framework](/images/2021_daily_mean_LST_framework.jpg){:height="65%" width="65%"}
<br>

**Global LST trend from 2003 to 2019 using the cloud-free MODIS LST and generated seamless IADTC LST dataset**
<br>
![Global LST](/images/Global_LST_trend_2003_2019.jpg){:height="70%" width="70%"}


### [5] Comprehensive assessment of diurnal land surface temperature cycle (DTC) models under clear-sky condition
* Obtain nine representative four-parameter DTC models with a set of parameter-reduction strategies.
* Comprehensive assessment of DTC models with geostationary satellite data and _in-situ_ measurements.
* Provide the parameter-reduction order and the best-performance four-parameter DTC model.
* The examples of the DTC models are available at: [DTC GitHub](https://github.com/faluhong/ATC-and-DTC-Code).
* Related publication: [Hong et al., 2008](https://www.sciencedirect.com/science/article/pii/S0924271618301710).

**Hourly RMSEs of the selcted nine four-parameter DTC models**
![image_four_parameter_DTC](/images/MSG-SEVIRI_four_points.png){:height="85%" width="85%"}











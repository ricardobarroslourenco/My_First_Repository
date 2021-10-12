Week 4 - Project Data Analysis - Intent to reproduce Sothe et al. (2021) in Google Earth Engine, using Open Science principles

---

* **List the data that you expect to use, collect or create in your project. Identify if you are generating or collecting the data and if you are using existing datasets?**

_I intend to use previously acquired data, majorly listed at Sothe et al. (2021), such as:_

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;_Soil Organic Carbon Concentration Levels from the 
[World Soil Information Service(WoSIS)](https://www.isric.org/explore/wosis/accessing-wosis-derived-datasets)_

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;_Other covariates obtained from remote sensing data (ex.: Temperature Estimates; 
Vegetation Indexes; Precipitation Estimates; Elevation Model; Slope; Band Composites; etc.)._ 



* **Are there legal or ethicial restrictions that you will need to address?**

_Ideally I will only work with publicly available data, which licensing terms allow free and open usage of information 
for scientific purposes. As the study aims to replicate results from Sothe et al. (2021), it does not involve human
subjects, which does not imply on aditional measures in terms of data safety._

* **Go through the Quick Hits for Data Management and identify possible strategies to build and protect the value of your data.**
  - **Where will you keep raw data and how will you back it up?**

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;_As I intend to replicate the 
study in Google Earth Engine(GEE), my initial desire is to keep remote sensing assets on its original collections at GEE, 
and the WoSIS data pulled directly from their repository (either to the notebook or to a GEE storage). To make clear, the intended usage of Earth Engine involves 
using their Python API, rather than the Javascript one. Therefore, all processing will happen with the aid of Jupyter
notebooks, which will be commited into Github._

  - **What file formats do you anticipate your data will be in? Are the formats open or can they be converted to open formats?**

_In GEE data comes often in a GEE native form of an 
[Image Collection](https://developers.google.com/earth-engine/tutorials/tutorial_api_04) which is a computational object 
that encapsulates files and/or mosaicks stored in GEE database and filesystems (Gorelick et al. 2017). Regarding WoSIS 
data, it will likely come in a GIS format, via a Web Feature Service (WFS) protocol. To store it on GEE, it is possible 
to save API query results in any Open Geospatial Consortium (OGC) format. Since it is API data, a good solution may be a 
GeoJSON format._

  - **Create a File naming convention for your project data**

_Depending on storage choice (GEE vs Document Store Database [ex. MongoDB] vs Filesystem) perhaps it will not be 
necessary to define a taxonomy for file conventions, but rather a query plan setup, based on spatial indexing. This will
be designed once have more contact with the data._

  - **What standards are relevant to your project? List any existing standards or best practices in use in your field 
or in your lab? This could include instrument procedures or file management standards. What standards might you want 
to create to help you manage your data?**

_In terms of best practices in the Remote Sensing domain, it is still an evolving field, but is quite common to use sources that are public, and allow 
API calls such as the ones defined in Ramachandran et al. (2021), with intensive usage of information systems for both 
storing and processing data, as well as sharing results in platforms that even allow re-running the computational experiment 
(especially when involving expensive HPC facilities)._

  - **List possible strategies you might use to document your data throughout your project.**

_I will probably be versioning each step of the experiment using come sort of cloud versioning system such as Github. 
The essence will be that each step of the experiment gets an individual commit, once a certain result is obtained. If 
processing the data involves too much intermediate processes, as well as results, each should be broken in intermediate 
commits, allowing the project to take multiverses, and explore counterfactuals if necessary._

---

**References:**

Camile Sothe, Alemu Gonsamo, Joyce Arabian, James Snider,
Large scale mapping of soil organic carbon concentration with 3D machine learning and satellite observations,
Geoderma, Volume 405, 2022, 115402, ISSN 0016-7061,
[https://doi.org/10.1016/j.geoderma.2021.115402](https://doi.org/10.1016/j.geoderma.2021.115402).

Noel Gorelick, Matt Hancher, Mike Dixon, Simon Ilyushchenko, David Thau, Rebecca Moore,
Google Earth Engine: Planetary-scale geospatial analysis for everyone,
Remote Sensing of Environment, Volume 202, 2017, Pages 18-27, ISSN 0034-4257,
[https://doi.org/10.1016/j.rse.2017.06.031](https://doi.org/10.1016/j.rse.2017.06.031).

Ramachandran, R., Bugbee, K., & Murphy, K. (2021). From open data to open science. Earth and Space Science, 8, 
e2020EA001562. [https://doi.org/10.1029/2020EA001562](https://doi.org/10.1029/2020EA001562)
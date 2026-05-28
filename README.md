## Follow the Water Project

FollowTheWater is an outdoor recreation planning application focused on skiing and whitewater sports. It is inspired by other tools such as Caltopo and Gaia GPS and features custom layers including localized river gradients, custom terrain filters, avalanche susceptibility, and predicted river flows.



This project intentionally utilizes multiple tools and workflows (ArcGIS, QGIS, GeoPandas), to reflect the range of real world GIS development.



All stated features, analyses, and tools are in development and subject to change. 



## Repository Structure
```
FollowTheWater/

├── README.md

├── analysis/               # analysis scripts used in creating maps and features 

├── data/                   # Small reference datasets (GeoJSON, etc.)

├── src/                    # Processing scripts

└── web/                    # Frontend application 
```


## Features

- **River Gradient Layer** — localized river gradient calculated over uniform intervals

- **Ski Terrain Suitability** — filter terrain based on features such as slope, elevation, aspect, and tree density to identify desirable backcountry skiing zones

- **Avalanche Susceptibility** — localized predictions of avalanche likelihood for specific ski lines/zones given the current conditions (based on machine learning analysis of historic records) 

- **Snowpack by Watershed** — monthly snow water equivalent summarized by HUC6 and HUC8 watershed from 2000 to present

- **Predicted River Flows** — predicted flows for sections of rivers based on machine learning analysis of historic records



## Exploratory Work

This project includes the following standalone analyses and outputs not included in the final tool. These are documented as individual map outputs and represent the exploratory analysis that informed the final features in the application.



### Snowpack to River Flow History

A chronological series of maps showing monthly snowpack for watersheds and average river flows. 



## Analyses

| Analysis | Description | Output |
|---|---|---|
| Historical Avalanche Susceptibility | Train machine learning model on historical avalanche reports and data on snow/weather conditions to predict future avalanches | Avalanche Susceptibility Feature | 
| Historical River Flows | Train machine learning model on historical flow gauge and weather data to predict future river flows | Predicted River Flows Feature |



## Data Sources

| Dataset | Source |
|---|---|
| NHD Plus V2 Flowlines | [USGS via Esri Living Atlas](https://services.arcgis.com/P3ePLMYs2RVChkJx/arcgis/rest/services/NHDPlusV21/FeatureServer) | 
| GLDAS Snowpack 2000-Present | [NASA/Esri Living Atlas](https://livingatlas.arcgis.com) | 
| HUC6/HUC8 Watershed Boundary Dataset | [USGS/Esri Living Atlas](https://livingatlas.arcgis.com) | 
| 3DEP Elevation | [USGS National Map](https://www.usgs.gov/3d-elevation-program) | 
| USGS Streamflow | [USGS Water Services](https://waterservices.usgs.gov) | 


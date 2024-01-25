# Ganges-River-Water-Analysis-and-Visualization
Pale Blue Dot: Visualization Challenge, Clean Water and Sanitation
## Table of Contents

- [Introduction](#introduction)
- [Motivation](#motivation)
- [Project Overview](#project-overview)
- [Requirements](#requirements)
- [Installation](#installation)
- [Usage](#usage)
- [Features](#features)
- [Folder Structure](#folder-structure)
- [Data Sources](#data-sources)
- [Methodology](#methodology)
- [Results](#results)
- [License](#license)

## Introduction

Welcome to the Ganges River Water Analysis and Visualization project repository! This project aims to provide a comprehensive analysis of water quality in a selected area in the Ganges River, India, utilizing satellite imagery, weather data, and water quality indices. The repository contains Python scripts and Jupyter Notebooks that automate the retrieval of satellite and weather data, process the data, and generate visualizations to gain insights into the river's water quality.

## Motivation

The Ganges River is a vital water resource for millions of people and plays a crucial role in the ecosystem. Monitoring its water quality is essential for understanding environmental changes, ensuring the well-being of communities, and facilitating sustainable management practices. This project addresses the need for an integrated approach to water quality analysis, bringing together satellite imagery, weather data, and advanced analytics.

## Project Overview

The Ganges River Water Analysis and Visualization project encompass several key components:

1. **Satellite Image Processing:** The project utilizes Sentinel-2 satellite imagery from https://dataspace.copernicus.eu/ to detect water bodies and calculate various water quality indices such as Normalized Difference Water Index (NDWI), Normalized Difference Snow Index (NDSI), Turbidity Index, Chlorophyll Concentration, and Evapotranspiration Index.

2. **Weather Data Retrieval:** Weather data is obtained from the ERA5 reanalysis dataset using the Copernicus Climate Data Store (CDS) API https://cds.climate.copernicus.eu/cdsapp#!/home. The data includes information such as temperature, precipitation, wind speed, cloud cover, and more.

3. **Data Integration and Analysis:** The retrieved satellite and weather data are integrated and analyzed to understand correlations and trends. The analysis provides valuable insights into the relationship between weather conditions and water quality in the Ganges River.

4. **Visualization:** The project generates interactive visualizations, including 3D scatter plots, pair plots, and geographical maps, to present the analyzed data in an accessible and informative manner.

5. **Automated Reporting:** The repository includes scripts for generating automated reports in HTML format. These reports include interactive visualizations and key findings, making it easier to share and communicate results.

## Requirements

To run the Ganges River Water Analysis and Visualization project, ensure you have the following requirements installed:

- Python 3.x
- Jupyter Notebook
- Copernicus Climate Data Store (CDS) API account (for accessing weather data)
- Satellite Imagery bands 02, 03, 04, 08, 09, 11, 12 adn the TrueColor image.
- GIS Shape and geojson files for the area of interest, in this project, we have defined a boundary for a selected area along the Ganges River in India..

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/yassineelhallaoui/Ganges-River-Water-Analysis-and-Visualization.git

2. Navigate to the project directory:
cd ganges-river-water-analysis

3. Install the required Python packages:
pip install -r requirements.txt

4. Set up your CDS API account and configure the CDS API key in the .cdsapirc file.

## Usage
1. Run the Jupyter Notebook:
2. Open the notebook Ganges_River_Water_Analysis.ipynb and follow the instructions provided within the notebook.

## Features
The Ganges River Water Analysis and Visualization project offer the following features:

1. Satellite Image Processing:
Detection of water bodies using Sentinel-2 satellite imagery.
Calculation of water quality indices, including NDWI, NDSI, Turbidity Index, Chlorophyll Concentration, and Evapotranspiration Index.

2. Weather Data Retrieval:
Automated retrieval of weather data from the ERA5 reanalysis dataset using the CDS API.

3. Data Integration and Analysis:
Integration of satellite and weather data for comprehensive analysis.
Calculation of statistics and correlations to identify patterns.

4. Visualization:
Generation of interactive 3D scatter plots for visualizing water quality indices over time.
Creation of pair plots to explore relationships between variables.
Geographic mapping of water quality and weather data for spatial insights.

5. Automated Reporting:
Generation of HTML reports with interactive visualizations for easy sharing of results.

## Folder Structure
The project repository is organized into the following folders:
├── GIS
│   ├── GIS_Locations_Extends.qgz
│   ├── Rasters
│   │   ├── ANWR

1. GIS: Contains raster images and shapefiles related to the Ganges River.
GIS Folder Structure
├── GIS -> Input data source folder.
│   ├── Rasters
│   │   ├── Project_Name
│   │   │   ├── Zip files contain the satellite imagery bands specified in the requirements. Ensure that each zip file name ends with the satellite image's date and time in the following format: DDMMYYYY.zip.
│   ├── Shape_File
│   │   ├── Project_Name
└─  ─   ─   ├── Shapefile and GeoJSON file of the selected area of interest (polygon boundary).

2. deliverables: Output directory for results and visualizations.

├── deliverables -> Output data source folder. 
│   ├── Project_Name
│   │   ├── GIS_Analysis_Plot -> Satellite images, GIS water quality indices, and plots have been exported as .png files.
│   │   ├── Water_Quality_Plots -> Exported Interactive html Plot
│   │   │   ├── 3d_Chlorophyll_Concentration_scatter.html
│   │   │   ├── 3d_Turbidity_Index_scatter.html
│   │   │   ├── Water_Quality_pairplot.png
│   │   ├── Weather_dataframes -> Downloaded weather dataframes that correspond to the satellite image date and time. Note that it's a 24-hour weather measurement, with data available for each hour (temperature, total precipitation, ...)
│   │   ├── Weather_Quality_Plots -> Processed weather data has been exported as line plots for each day.
│   │   ├── water_quality_indices dataframe .csv -> The exported dataframe contains the water quality indices in numerical format.
└── ─   └── Water_Visualization_DashBoard.html -> The final report serves as a visualization solution with interactive features.

Feel free to explore each folder for detailed information on data and scripts.

## Data Sources
1. Sentinel-2 Satellite Imagery:
The project uses Sentinel-2 Level 2A bands for processing, including the Near Infrared (B08) bands, and other bands mentioned on the Requirements.

2. ERA5 Reanalysis Weather Data:
Weather data is obtained from the ERA5 reanalysis dataset, providing information on temperature, precipitation, wind speed, and more.

## Methodology
The Ganges River Water Analysis and Visualization project follows a systematic methodology:

1. Data Retrieval:
Satellite imagery and weather data are retrieved from relevant sources.

2. Preprocessing:
Data preprocessing involves tasks such as extracting relevant bands from satellite imagery and dealing with weather data and converting necessary units.

3. Analysis:
Statistical analysis and correlation studies are conducted to derive insights.

4. Visualization:
Visualizations are generated to present data in an understandable format.

5. Reporting:
Automated interactive reports are generated to facilitate communication of findings.

## Results
The project results in comprehensive visualizations and insights into the water quality of the are of interest in the Ganges River. Users can explore trends, correlations, and spatial patterns through interactive plots and reports.

## License
This project is licensed under the MIT License.

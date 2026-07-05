# Satellite-Based Methane Hotspot Detection over the Damodar Valley Coal Belt using Sentinel-5P TROPOMI, Google Earth Engine and Python

A cloud-based remote sensing workflow for detecting persistent atmospheric methane hotspots over the Damodar Valley Coal Belt using Sentinel-5P TROPOMI observations, Google Earth Engine, Geemap and Python.

The project combines historical baseline modelling, statistical anomaly detection, z-score analysis, hotspot persistence mapping and interactive geospatial visualization to identify recurring methane enhancement zones associated with one of India's largest coal mining regions.

![Python](https://img.shields.io/badge/Python-3.11-blue)

![Google Earth Engine](https://img.shields.io/badge/Google-Earth%20Engine-green)

![Sentinel-5P](https://img.shields.io/badge/Sentinel--5P-TROPOMI-orange)

![Geemap](https://img.shields.io/badge/Geemap-Interactive%20Maps-success)

![Remote Sensing](https://img.shields.io/badge/Remote-Sensing-red)

![GIS](https://img.shields.io/badge/GIS-Spatial%20Analysis-yellowgreen)

------------------------------------------------------------------------------------------------------------------------------------

# Table of Contents

- Project Overview
- Objectives
- Study Area
- Dataset
- Methodology
- Workflow
- Results
- Figures
- Interactive Maps
- Repository Structure
- Installation
- Technologies Used
- Future Improvements
- Author

# Project Overview

Methane (CH₄) is one of the most significant greenhouse gases contributing to climate change. Detecting persistent methane emissions from industrial regions is essential for environmental monitoring and mitigation.

This project develops an automated cloud-based workflow using Sentinel-5P TROPOMI satellite observations and Google Earth Engine to identify statistically significant methane anomalies over the Damodar Valley Coal Belt, India.

Historical methane observations are used to establish a baseline against which monthly methane concentrations are compared using z-score analysis. Persistent hotspots are identified by analysing the temporal frequency of methane anomalies and exported as GIS-ready datasets for further investigation.


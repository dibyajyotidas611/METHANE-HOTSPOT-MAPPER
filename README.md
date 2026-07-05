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

---

# Objectives

- Detect atmospheric methane anomalies over the Damodar Valley Coal Belt using Sentinel-5P TROPOMI observations.
- Develop a historical methane baseline (2019–2024).
- Calculate methane anomalies relative to the historical baseline.
- Compute standardized methane anomaly (Z-score).
- Detect statistically significant methane hotspot pixels.
- Identify persistent methane hotspots through temporal frequency analysis.
- Visualize methane distributions using interactive Google Earth Engine maps.
- Export hotspot locations for further GIS analysis.

---

# Study Area

The study focuses on the **Damodar Valley Coal Belt**, one of India's largest coal-producing regions extending across **Jharkhand** and **West Bengal**.

Major mining districts include:

- Dhanbad
- Bokaro
- Giridih
- Asansol
- Raniganj

The region contains extensive underground and opencast coal mining operations, making it an important area for monitoring methane emissions associated with coal extraction.

**Approximate Bounding Box**

| Longitude | Latitude |
|-----------|----------|
| 84.0° E | 23.0° N |
| 88.5° E | 24.8° N |

---

# Dataset

| Dataset | Source |
|---------|--------|
| Sentinel-5P TROPOMI Methane | Copernicus Programme |
| Platform | Google Earth Engine |
| Temporal Coverage | January 2019 – December 2025 |
| Spatial Resolution | ~7 km |
| Variable | CH₄ Column Volume Mixing Ratio (Dry Air) |

---

# Technologies Used

- Python
- Google Earth Engine
- Geemap
- Sentinel-5P TROPOMI
- NumPy
- Pandas
- Jupyter Notebook
- Remote Sensing
- GIS


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

---

# Project Structure

```
METHANE-HOTSPOT-MAPPER
│
├── Damodar_Valley_Methane_Hotspot_Detection.ipynb
├── Methane_Hotspot_Mapper.py
├── README.md
├── requirements.txt
├── LICENSE
├── BASELINE_MAP.html
├── PERSISTENT_HOTSPOT_MAP.html
├── 01_STUDY_AREA.png
├── 02_HISTORICAL_MEAN_METHANE_CONCENTRATION.png
├── 03_HISTORICAL_METHANE_VARIABILITY.png
├── 04_MONTHLY_METHANE_ANOMALY.png
├── 05_MONTHLY_METHANE_ZSCORE.png
├── 06_MONTHLY_METHANE_HOTSPOTS.png
├── 07_PERSISTENT_HOTSPOT_FREQUENCY.png
├── 08_HOTSPOT_CENTROIDS.png
├── 09_INTERACTIVE_BASELINE_MAP.png
└── 10_INTERACTIVE_PERSISTENT_HOTSPOT_MAP.png
```

---

# Results

The workflow successfully identified statistically significant methane enhancement zones across the Damodar Valley Coal Belt using Sentinel-5P TROPOMI observations.

Major outputs generated include:

- Historical methane baseline map
- Historical methane variability map
- Monthly methane anomaly map
- Monthly methane Z-score map
- Monthly methane hotspot map
- Persistent hotspot frequency map
- Hotspot centroid extraction
- Interactive HTML maps for visualization

---

# Workflow

```text
Sentinel-5P TROPOMI
        │
        ▼
Google Earth Engine
        │
        ▼
Area of Interest Selection
        │
        ▼
Historical Baseline Calculation
        │
        ▼
Historical Standard Deviation
        │
        ▼
Monthly Methane Composite
        │
        ▼
Methane Anomaly Calculation
        │
        ▼
Z-Score Analysis
        │
        ▼
Hotspot Detection
        │
        ▼
Persistent Hotspot Frequency
        │
        ▼
Hotspot Centroid Extraction
        │
        ▼
Interactive HTML Maps
```

---

# Figures

## FIGURE 1. STUDY AREA

![](01_STUDY_AREA.png)

---

## FIGURE 2. HISTORICAL MEAN METHANE CONCENTRATION

![](02_HISTORICAL_MEAN_METHANE_CONCENTRATION.png)

---

## FIGURE 3. HISTORICAL METHANE VARIABILITY

![](03_HISTORICAL_METHANE_VARIABILITY.png)

---

## FIGURE 4. MONTHLY METHANE ANOMALY

![](04_MONTHLY_METHANE_ANOMALY.png)

---

## FIGURE 5. MONTHLY METHANE Z-SCORE

![](05_MONTHLY_METHANE_ZSCORE.png)

---

## FIGURE 6. MONTHLY METHANE HOTSPOTS

![](06_MONTHLY_METHANE_HOTSPOTS.png)

---

## FIGURE 7. PERSISTENT HOTSPOT FREQUENCY

![](07_PERSISTENT_HOTSPOT_FREQUENCY.png)

---

## FIGURE 8. HOTSPOT CENTROIDS

![](08_HOTSPOT_CENTROIDS.png)

---

## FIGURE 9. INTERACTIVE BASELINE MAP

![](09_INTERACTIVE_BASELINE_MAP.png)

---

## FIGURE 10. INTERACTIVE PERSISTENT HOTSPOT MAP

![](10_INTERACTIVE_PERSISTENT_HOTSPOT_MAP.png)

---

# Interactive Maps

This repository contains two interactive HTML maps generated using Google Earth Engine and Geemap.

### BASELINE MAP

**File:** `BASELINE_MAP.html`

Displays:

- Historical methane concentration
- Persistent hotspot polygons
- Study area boundary
- Interactive layer control

---

### PERSISTENT HOTSPOT MAP

**File:** `PERSISTENT_HOTSPOT_MAP.html`

Displays:

- Persistent hotspot frequency
- Hotspot centroids
- Interactive GIS visualization
- Layer control

---

# Installation

Clone the repository:

```bash
git clone https://github.com/dibyajotidas611/METHANE-HOTSPOT-MAPPER.git
```

Install the required Python packages:

```bash
pip install earthengine-api geemap pandas numpy matplotlib
```

Authenticate Google Earth Engine:

```python
import ee

ee.Authenticate()
ee.Initialize(project="methane-hotspot-detection")
```

Run either:

- `Damodar_Valley_Methane_Hotspot_Detection.ipynb`
- `Methane_Hotspot_Mapper.py`

---

# Applications

This workflow can be applied to:

- Methane emission monitoring
- Coal mining environmental assessment
- Greenhouse gas surveillance
- Climate change studies
- Satellite-based environmental monitoring
- Remote sensing research
- GIS-based spatial analysis
- Earth observation projects

---

# Future Improvements

- Near real-time methane monitoring
- Machine learning-based hotspot classification
- Automated emission alert system
- WebGIS dashboard development
- Integration with Sentinel-2 imagery
- Quantitative methane emission estimation

---

# Author

## Dibya Jyoti Das

Master's in Applied Geology

Remote Sensing • GIS • Google Earth Engine • Python

If you found this project useful, consider giving this repository a ⭐.

---

# License

This project is released under the MIT License.



# Soil pH Estimation Using Environmental Covariates & Machine Learning

## 🌍 Overview
This repository provides a comprehensive workflow and scripts for modeling and predicting spatial soil pH distributions using environmental, topographic, and spectral covariates[cite: 2]. While the original scripts were developed and tested in **R**, this workflow adapts the methodology for cloud-based geospatial processing and machine learning using **Google Earth Engine (GEE)** and **Google Colab**.

---

## 📊 Covariate Datasets
The predictive machine learning model integrates multiple spatial layers extracted as feature covariates[cite: 2]:

| Covariate Feature | Description / Metric Category |
| :--- | :--- |
| **`pH60_100`** | Target soil pH variable (sampled at 60–100 cm depth)[cite: 2] |
| **`Elevation`** | Digital Elevation Model (DEM) height data[cite: 2] |
| **`Slope`** | Terrain steepness and gradient[cite: 2] |
| **`Mid_Slope`** | Mid-slope position metric[cite: 2] |
| **`Terrain_Ruggedness`** | Terrain Ruggedness Index (TRI)[cite: 2] |
| **`MRVBF`** | Multi-Resolution Valley Bottom Flatness index[cite: 2] |
| **`TWI`** | Topographic Wetness Index (soil moisture tendency)[cite: 2] |
| **`AACN`** | Accumulated catchment / hydrologic network metric[cite: 2] |
| **`Hillshading`** | Surface illumination and hillshade raster[cite: 2] |
| **`Light_insolation`** | Solar radiation and light insolation index[cite: 2] |
| **`NDVI`** | Normalized Difference Vegetation Index (vegetation vigor)[cite: 2] |
| **`Landsat_B`** | Landsat spectral surface reflectance bands[cite: 2] |

---

## 📁 Dataset Source & Methodology
* **Original Implementation:** Originally developed and tested using the **R programming language**.
* **Source Material & Tutorials:** Adapted from the Digital Soil Mapping (DSM) book training resources for [Random Forest-based Regression Implementation](https://smartdigiag.com/DSM_book/pages/dsm_cont/sspfs/rf/).
* **Covariate Integration:** Combines terrain derivatives, hydrologic indices, and remote sensing bands to predict subsoil pH (`pH60_100`)[cite: 2].

---

## 🚀 Getting Started
1. Open the **`04_Notebooks`** (or scripts) folder from the repository.
2. Upload the individual notebooks/scripts to **Google Colab** (note: Colab supports both Python and R runtimes).
3. Authenticate your Google Earth Engine account if running GEE workflows (`ee.Initialize()`).
4. Execute the scripts sequentially to process environmental covariates, train the Random Forest regression model, and visualize spatial soil pH predictions.

> *Enjoy the hands-on exercises and spatial soil modeling!*

# Predicting the Hidden Carbon Deficit of Surface Mining

This repository contains the data, Google Earth Engine (GEE) extraction scripts, and machine learning architecture for the manuscript: **"Predicting the hidden carbon deficit of surface mining via machine learning and eco-economic valuation."**

## Overview
This project introduces a predictive eco-economic framework comparing the ecological impacts of opencast and underground coal mining in the Korba coalfields, India. By fusing ground-truthed phytosociological data with multi-dimensional satellite imagery, we quantify the permanent ecological ceiling imposed by surface extraction.

## Methodological Framework
1. **2D Spatial Scaling:** Sentinel-2 Harmonized Level-2A imagery to extract Normalized Difference Vegetation Index (NDVI) mapping.
2. **3D Structural Validation:** NASA GEDI-derived ETH Global Canopy Height modeling (10m resolution) to account for optical saturation.
3. **4D Temporal Velocity:** USGS Landsat 5-9 archive harmonization to track 26-year (2000–2026) ecological recovery trajectories.
4. **Predictive AI:** A Random Forest regression pipeline integrated with SHapley Additive exPlanations (SHAP) to isolate extraction methodology penalties ($R^2 = 0.9754$).

## Eco-Economic Valuation
The model integrates the Social Cost of Carbon (SCC) to translate biological carbon deficits into macroeconomic policy metrics, quantifying an un-taxed ecological deficit of $21,584 USD per hectare associated with opencast mining.

## Repository Structure
* `/data`: Contains ground-truthed biomass calculations, 2D NDVI, 3D GEDI heights, and decadal Landsat trajectories.
* `/scripts`: Jupyter notebooks for GEE data extraction, data imputation, and Random Forest/SHAP analytics.
* `/figures`: High-resolution outputs of SHAP feature importance and temporal recovery graphs.

## Dependencies
* `earthengine-api`
* `pandas`, `numpy`
* `scikit-learn`
* `shap`
* `matplotlib`, `seaborn`

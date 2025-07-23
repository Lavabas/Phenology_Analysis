# NDVI Phenology Analysis using Python API (Xee)
This project performs a time-series analysis of the Normalized Difference Vegetation Index (NDVI) to determine the Start of Season (SOS), End of Season (EOS), and Length of Season (LOS) within a selected Region of Interest (ROI) in Sri Lanka, using the Python API xee for accessing Google Earth Engine (GEE) data.

## Overview
Vegetation phenology plays a key role in understanding climate dynamics, agricultural planning, and ecosystem responses. This script leverages the NOAA CDR AVHRR NDVI V5 dataset and uses Python-based tools,particularly the xee and xarray libraries,to automate and streamline the analysis pipeline.

By using this cloud-based method, users can perform high-resolution phenological monitoring without downloading large datasets locally.

## Data Sources
1. NDVI Dataset:
- Name: NOAA Climate Data Record (CDR) of AVHRR NDVI Version 5
- Source: Google Earth Engine - NOAA/CDR/AVHRR/NDVI/V5
- Temporal Resolution: 7-day composites
- Spatial Resolution: ~0.05 degrees (~5 km)

2. Xee Python Package:
- Xarray plugin to open GEE ImageCollections as virtual NetCDF datasets.
- https://pypi.org/project/xee/

### Smoothed NDVI Time Series Using Savitzky-Golay Filter:
<img width="550" height="416" alt="image" src="https://github.com/user-attachments/assets/e983f251-8b14-4dd3-82b9-1332e41d7788" />

### Combined Plot: Raw vs Smoothed NDVI:
<img width="550" height="416" alt="image" src="https://github.com/user-attachments/assets/a61e1f20-3719-4025-a62d-659500839492" />


Here,
- start of growing season (sos): 2016-01-14
- end of growing season (eos): 2016-12-26
- length of growing season (los): 348

## Notes
1. This analysis applies a Savitzky-Golay filter to smooth noisy NDVI time-series data, which helps in identifying phenological transitions (e.g., start and end of growing season).
2. The threshold value (0.35) for determining Start of Season (SOS) and End of Season (EOS) may need adjustment depending on the vegetation type or local conditions.








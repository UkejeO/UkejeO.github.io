---
title: "Flood Detection and Mapping Using Sentinel-1 and CHIRPS Data"
date: 2025-07-01
tools: "Python, Rasterio, Scikit-learn, Random Forest, SMOTE, GDAL"
description: "Developed a machine learning pipeline for flood detection in Nigeria using Sentinel-1 SAR and CHIRPS rainfall data, achieving 98-99% accuracy in flood classification and creating probabilistic flood maps validated across multiple time periods."
layout: default
---

## Overview

Flooding is one of the most devastating natural disasters, impacting lives, infrastructure, and the environment. With increasing frequency of extreme weather events due to climate change, effective flood monitoring and mapping are essential. This research developed a robust methodology using Sentinel-1 SAR data and CHIRPS rainfall data to detect and map flood events under all weather conditions, even during cloud cover.

## Key Steps

- **Data Preprocessing**: Converted Sentinel-1 Digital Numbers to Sigma0 in decibels, applied speckle filtering using median filter, and aligned CHIRPS rainfall data to match Sentinel-1 resolution
- **Feature Engineering**: Stacked Sentinel-1 backscatter (Sigma0) and CHIRPS rainfall data to create comprehensive feature matrices for machine learning
- **Machine Learning Implementation**: Developed Random Forest classifier with SMOTE to address class imbalance in flood detection
- **Memory-Efficient Processing**: Implemented batch prediction methodology to handle large raster datasets without memory constraints
- **Multi-Temporal Analysis**: Applied identical methodology to both October 2022 and April 2018 data for comparative flood assessment

## Results & Insights

### Model Performance & Validation
- **High Accuracy Detection**: Achieved 99% overall accuracy for October 2022 and 98% for April 2018, demonstrating reliable flood classification
- **Precision-Recall Analysis**: October 2022 model showed strong performance (Precision: 0.71, Recall: 0.94, F1-Score: 0.81) while April 2018 revealed challenges with false positives (Precision: 0.29, Recall: 0.91, F1-Score: 0.44)
- **Temporal Robustness**: Model maintained high accuracy across different time periods, though precision variations highlighted seasonal flood pattern differences

### Mapping Products & Observations
- **Binary Flood Masks**: Successfully generated clear flood/non-flood classifications for both April 2018 and October 2022 time periods
- **Probabilistic Flood Maps**: Created gradient risk maps showing flood likelihood, enabling nuanced risk assessment beyond binary classification
- **Rainfall Correlation**: Observed strong correspondence between CHIRPS rainfall intensity and Sentinel-1 detected flooding patterns
- **Technical Innovation**: Batch processing implementation successfully handled large datasets without memory errors, enabling full spatial coverage

### Key Findings
- **Enhanced Detection**: Integration of Sentinel-1 SAR with CHIRPS rainfall data significantly improved flood detection capabilities
- **Methodology Reproducibility**: Successfully applied identical pipeline to multiple time periods (April 2018 and October 2022), demonstrating methodological robustness
- **Data Limitations**: Identified regions with discrepancies between rainfall expectations and SAR-detected flooding, highlighting data quality considerations

## Applications & Implications

The developed flood detection system provides a reliable, all-weather monitoring solution that can operate through cloud cover—a critical limitation of optical satellite imagery during flood events. This methodology enables:

- **Emergency Response**: Rapid identification of flood-affected areas for targeted relief operations and resource allocation
- **Risk Assessment**: Probabilistic flood maps support urban planning, insurance risk evaluation, and infrastructure development decisions
- **Climate Adaptation**: Temporal comparison capabilities help monitor changing flood patterns to inform climate adaptation strategies
- **Scalable Monitoring**: Batch processing approach makes the system applicable to regional or national-scale flood monitoring operations

### Technical Considerations
**Strengths:**
- All-weather flood detection capability using SAR data
- Successful integration of multiple data sources (Sentinel-1 + CHIRPS)
- Scalable batch processing solution for large datasets

**Limitations:**
- Thresholding dependencies requiring periodic recalibration
- CHIRPS resolution constraints for localized rainfall variations
- Temporal performance variations requiring model refinement

**Future Directions:**
- Experiment with alternative machine learning and deep learning models
- Develop advanced memory management for larger datasets
- Incorporate additional data sources for improved accuracy

---

View this project on the website: [Flood Detection and Mapping]({{ site.baseurl }}/projects/flood_detection.html)

### Relevant Sources
- [Sentinel-1 Mission Overview](https://sentinels.copernicus.eu/web/sentinel/missions/sentinel-1)
- [CHIRPS Rainfall Data](https://www.chc.ucsb.edu/data/chirps)
- [Random Forest for Remote Sensing](https://doi.org/10.1016/j.isprsjprs.2019.03.010)
- [SAR-based Flood Mapping Techniques](https://doi.org/10.3390/rs12030418)

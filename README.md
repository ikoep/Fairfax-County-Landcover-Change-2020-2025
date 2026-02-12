# Fairfax-County-Landcover-Change-2020-2025
Overview:
This project quantifies land cover change in Fairfax County, Virginia between 2020 and 2025 using Sentinel-2 L2A multispectral imagery. This analysis focuses on decline in forest landcover and increase in urban expansion using the Normalized Difference Built-up Index (NDBI) and supervised classification aligned with Andersons Classification Scheme (Level I). 
The objective of this project was to evaluate how the expansion of impervious surfaces correspond with vegetation decline and assess the accuracy of an index based urban detection.

Data & Tools:
* Sentinel-2 L2A
* Copernicus Space Data Ecosystem
* ERDAS Imagine
* ArcGIS Pro
* Anderson Level I Classification System
* Supervised Classification
* NDBI (SWIR - NIR)/(SWIR + NIR)
* Accuracy Assessment (with Confusion Matrix and Kappa)
Imagery filtered to 10% cloud cover and was limited to the month of May-Aug to ensure consistency in vegetation.

Workflow Summary:
* Acquired and mosaicked Sentinel-2 imagery (2020 & 2025).
* Applied radiometric corrections and subset to Fairfax County boundary.
* Generated NDBI using Band 12 (SWIR) and Band 8 (NIR).
* Performed supervised classification (6 Anderson Level I classes).
* Conducted stratified accuracy assessment (100 random points per year for validation).
* Quantified pixel-based land cover change.

Key Results:
* Tree cover decreased by ~25.5%
  * 973,634 pixels (2020)
  * 725,145 pixels (2025)
  * Loss of 248,489 pixels
* Urban land cover increased by ~15.8% (adjusted estimate)
  * Approximate gain of 244,734 pixels
* Accuracy Metrics:
  * 2020 Overall Accuracy: 78% (Kappa = 0.61)
  * 2025 Overall Accuracy: 68% (Kappa = 0.55)
The urban expansion was roughly the same amount of change per pixel as the forest loss, suggesting a direct land cover conversion.

Limitations:

* Multi-date mosaics introduced radiometric variance.
* Persistent clouds even when properly filtered impacted classification.
* 20m resolution limited classification precision.
* Additional training samples and 10m resolution may improve future accuracy.

Maps & Visuals:


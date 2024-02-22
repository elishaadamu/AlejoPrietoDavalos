---
author: alejo_prieto_davalos
title: Ship Tracker with Satellite Imagery [private]
date: 2023-12-01 12:00:00 +0000
categories: [GeoSpatial, AI, ObjectDetection]
tags: [python, networkx, igraph, mongodb, web_scraping, crypto]
image:
  path: /media/projects/ship_tracker/pred_1.jpg
  height: 100
  width: 100
summary: Detection of objects (ships) using Artificial Intelligence and Satellite Images with Python.
language: Python
---

# Ship Tracker with Satellite Imagery and AI

## Introduction
- This project aims to unveil **'[Dark Vessels](https://globalfishingwatch.org/research-project-dark-vessels/)'**—ships that avoid **Automatic Identification System ([AIS](https://globalfishingwatch.org/faqs/what-is-ais/))** tracking.
- `Reasons why AIS is turned off:` Illegal fishing, smuggling, illegal entry into a country,...
- Using cutting-edge **SAR satellite images** and **Deep Learning** I made a prototype that **identifies, segments** and evaluates ships potentially involved in **illicit maritime activities**.



## Technology Overview
- `SAR satellite images:` Penetrate cloud cover and other atmospheric conditions, providing reliable images regardless of the weather.
- `Rasterio, GeoPandas and QGIS:` Frameworks for geospatial data analysis.
- `PyTorch:` It was used to create the **Neural Network**, **fully convolutional** from scratch.



## Project Highlights

### Prototype Development
- `Ship Position Detection:` Detects different points, each with a probability and filtered by proximity.
- `Segmentation Techniques:` Effectively isolates ships from the sea surface, providing clear visuals for analysis.
- `Noise Reduction:` Implemented filters with exponential distance decay to highlight vessel features against the sea.
- `3D Visualization:` Offers an immersive view of the detection process, aiding in understanding and further development.

### Milestones
The system is capable of:
1. **Get a new AIS image and get a set of points with all ocean ships around the world.**
2. **Classify each point with the probability that it is indeed a ship.**
3. **Save the points in a geospatial file and view it in tools like QGIS or similar.**


## Images

![Dark Vessel Detected](/media/projects/ship_tracker/segm_2.jpg)
*Dark Vessel Detected via SAR Imagery*

<img src="/media/projects/ship_tracker/segm_1.jpg" alt="Dark Vessel Detected" style="width: 100%; max-width: 500px; height: auto;">
<p><em>Dark Vessel Detected via SAR Imagery</em></p>

![Dark Vessel Detected](/media/projects/ship_tracker/segm_2.jpg){:height="36px" width="36px"}
*Dark Vessel Detected via SAR Imagery*


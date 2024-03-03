---
author: alejo_prieto_davalos
title: Ship Tracker with Satellite Imagery [private]
date: 2023-10-01 12:00:00 +0000
categories: [GeoSpatial, Satellite, AI, ObjectDetection]
tags: [pytorch, geopandas, rasterio, qgis, numpy, matplotlib, plotly]
image:
  path: /media/projects/ship_tracker/ship_prediction.jpg
  height: 100
  width: 100
summary: Detection of objects (ships) using Artificial Intelligence and Satellite Images with Python.
language: Python
---

# Ship Tracker with Satellite Imagery and AI
## Summary
Ship remote sensing system using SAR satellite images, artificial intelligence and object detection with Python. The objective is to detect suspicious activity in the sea around the world, illegal fishing, smuggling,...


## Introduction
- This project aims to unveil **'[Dark Vessels](https://globalfishingwatch.org/research-project-dark-vessels/)'**—ships that avoid **Automatic Identification System ([AIS](https://globalfishingwatch.org/faqs/what-is-ais/))** tracking.
- `Reasons why AIS is turned off:` Illegal fishing, smuggling, illegal entry into a country,...
- Using cutting-edge **SAR satellite images** and **Deep Learning** I made a prototype that **identifies, segments** and evaluates ships potentially involved in **illicit maritime activities**.


## Images

<div style="display: flex; flex-wrap: wrap; justify-content: space-around;">
  
  <!-- SHIPS IN WATER -->
  <div style="flex-basis: 48%; max-width: 300px; margin-bottom: 20px; text-align: justify;">
    <img src="/media/projects/ship_tracker/ships_in_water.jpg" alt="Ships in the water" style="max-width: 300px; width: 100%; height: auto;">
    <p style="width: 100%; max-width: 300px;"><em><b>Figure 1:</b> Sample of the SAR satellite image dataset and identified ships in the water.</em></p>
  </div>

  <!-- TRAIN LOSS -->
  <div style="flex-basis: 48%; max-width: 300px; margin-bottom: 20px; text-align: justify;">
    <img src="/media/projects/ship_tracker/ship_tracker_train_loss.jpg" alt="Detector Train Loss" style="max-width: 300px; width: 100%; height: auto;">
    <p style="width: 100%; max-width: 300px;"><em><b>Figure 2:</b> Ship identification and noise removal.</em></p>
  </div>

  <!-- PREDICTION -->
  <div style="flex-basis: 48%; max-width: 300px; margin-bottom: 20px; text-align: justify;">
    <img src="/media/projects/ship_tracker/ship_prediction.jpg" alt="Detector Prediction" style="max-width: 300px; width: 100%; height: auto;">
    <p style="width: 100%; max-width: 300px;"><em><b>Figure 3:</b> AI prediction for a subset of test data. The green dot is the actual value, the white ones are the network predictions. Each contains a probability of success.</em></p>
  </div>

</div>


<div style="display: flex; flex-wrap: wrap; justify-content: space-around;">

  <!-- SEGMENTATION -->
  <div style="flex-basis: 48%; max-width: 300px; margin-bottom: 20px; text-align: justify;">
    <img src="/media/projects/ship_tracker/ship_segmentation_1.jpg" alt="Ship Segmentation" style="max-width: 300px; width: 100%; height: auto;">
    <p style="width: 100%; max-width: 300px;"><em><b>Figure 4:</b> Ship identification and noise removal.</em></p>
  </div>

  <div style="flex-basis: 48%; max-width: 300px; margin-bottom: 20px; text-align: justify;">
    <img src="/media/projects/ship_tracker/ship_segmentation_2.jpg" alt="Ship Segmentation" style="max-width: 300px; width: 100%; height: auto;">
    <p style="width: 100%; max-width: 300px;"><em><b>Figure 5:</b> Ship identification and noise removal.</em></p>
  </div>


  <!-- SEGMENTATION 3D -->
  <div style="flex-basis: 48%; max-width: 300px; margin-bottom: 20px; text-align: justify;">
    <img src="/media/projects/ship_tracker/ship_segmentation_3d_1.jpg" alt="Ship Segmentation with 3D Plot" style="max-width: 300px; width: 100%; height: auto;">
    <p style="width: 100%; max-width: 300px;"><em><b>Figure 6:</b> Ship identification and noise removal, with 3D plot, the difference is visualized after the process.</em></p>
  </div>

  <div style="flex-basis: 48%; max-width: 300px; margin-bottom: 20px; text-align: justify;">
      <img src="/media/projects/ship_tracker/ship_segmentation_3d_2.jpg" alt="Ship Segmentation with 3D Plot" style="max-width: 300px; width: 100%; height: auto;">
      <p style="width: 100%; max-width: 300px;"><em><b>Figure 7:</b> Ship identification and noise removal, with 3D plot, the difference is visualized after the process.</em></p>
  </div>

</div>



## Technologies
- `SAR satellite images:` Penetrate cloud cover and other atmospheric conditions, providing reliable images regardless of the weather.
- `Rasterio, GeoPandas and QGIS:` Frameworks for geospatial data analysis.
- `PyTorch:` It was used to create the **Neural Network**, **fully convolutional** from scratch.
- `Numpy, Matplotlib and Plotly:` For calculation and plots.


## Project Highlights
- `Ship Position Detection:` Detects different points, each with a probability and filtered by proximity.
- `Segmentation Techniques:` Effectively isolates ships from the sea surface, providing clear visuals for analysis.
- `Noise Reduction:` Implemented filters with exponential distance decay to highlight vessel features against the sea.
- `3D Visualization:` Offers an immersive view of the detection process, aiding in understanding and further development.
- `The system is capable of:`
    1. **Get a new AIS image and get a set of points with all ocean ships around the world.**
    2. **Classify each point with the probability that it is indeed a ship.**
    3. **Save the points in a geospatial file and view it in tools like QGIS or similar.**

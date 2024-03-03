---
author: alejo_prieto_davalos
title: GeoCoverage with Circles [private]
date: 2023-01-15 12:00:00 +0000
categories: [GeoSpatial]
tags: [geopandas, matplotlib]
image:
  path: /media/projects/geocoverage_circles/argentina_circles.png
  height: 100
  width: 100
summary: Geospatial coverage of the polygon of any country in the world with circles.
language: Python
---

# GeoCoverage with Circles
## Summary
- The client has a script to collect data from [Google Places](https://developers.google.com/maps/documentation/places/web-service/overview?hl=es-419) within 50km radius circles, but circles of each country and geospatial data are not considered.
- **I integrated a new functionality:** I obtained all the polygons of the countries in the world. Given one of them, circles with a radius of 50km are generated to cover the entire area with minimal overlap.


## Introduction
- **Data Source:** I obtained the polygon data using **OpenStreetMap (OSM)**.
- **Circles Generator:** Given the polygon of a country, the script generates circles that perform [SpatialJoin](https://geopandas.org/en/stable/gallery/spatial_joins.html) with the country's surface.
- **Minimal Overlap:** Minimal overlap is achieved by offsetting the centroids by exactly half the distance between them.
- **Circles Radius:** The client requires circles with a radius of **50km**, but the system works with any radius.
- **Exported Data:** The country's polygon, centroids, and circles are exported in 3 different **GeoJSON** files.
- **Plots:** Visualizations shown in Figure 1 are added.

## Project Goal
Find all the circles given any polygon, and for each of them, gather geographic data.

## Images
<div style="display: flex; flex-wrap: wrap; justify-content: space-around;">
  <!-- 4 Countries Plot -->
  <div style="flex-basis: 48%; max-width: 500px; margin-bottom: 20px; text-align: justify;">
    <img src="/media/projects/geocoverage_circles/subplot_countries.png" alt="Coverage of 4 countries." style="max-width: 500px; width: 100%; height: auto;">
    <p style="width: 100%; max-width: 500px;"><em><b>Figure 1:</b> Circles of 50km radius are shown for 4 arbitrary countries.</em></p>
  </div>
</div>

## Technologies
- **OpenStreetMap (OSM):** Open-source community for geospatial data.
- **GeoPandas:** Used for processing polygons, circles, and centroids.
- **Matplotlib:** For data visualization.


## Project Highlights
- **The ability to generate all circles given a country was successfully delivered to the client.**
- **Minimal overlap was essential for the requirement, as Google Place charges for each API call.**
- **A simple mechanism for exporting and visualizing data is provided.**

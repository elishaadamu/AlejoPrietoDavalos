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
1. **Figure 1:** (Subplot countries, 4 countries, Argentina, Italy, China, and Japan) Circles of 50km radius are shown for 4 arbitrary countries.


## Technologies
- **OpenStreetMap (OSM):** Open-source community for geospatial data.
- **GeoPandas:** Used for processing polygons, circles, and centroids.
- **Matplotlib:** For data visualization.


## Project Highlights
- **The ability to generate all circles given a country was successfully delivered to the client.**
- **Minimal overlap was essential for the requirement, as Google Place charges for each API call.**
- **A simple mechanism for exporting and visualizing data is provided.**

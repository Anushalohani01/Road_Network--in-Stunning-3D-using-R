

**Overview:**  
This project demonstrates how to create a 3D visualization of Nepal's road network using Digital Elevation Model (DEM) data and OpenStreetMap (OSM) road data. We use **R** for spatial data processing and 3D rendering with the **rayshader** package.

**Prerequisites:**  
Ensure you have R installed, along with the following libraries:
- **pacman**
- **sf**
- **terra**
- **elevatr**
- **rayshader**
- **scales**
- **tidyverse**


**Steps:**

1. **Install and Load Libraries**  
   Begin by loading the necessary libraries in R using `pacman::p_load()`.

2. **Set Working Directory for OSM Road Data**  
   Create a working directory to store the downloaded OSM road data for Nepal.

3. **Download and Prepare OSM Road Data for Nepal**  
   Download the OSM road shapefile for Nepal from **Geofabrik**, unzip the file, and load the road shapefile into R.

4. **Get Country Boundary Data for Nepal**  
   Download Nepal's country boundary using the **GADM** dataset. This will help filter the road data according to Nepal's geographic extent.

5. **Download Digital Elevation Model (DEM) Data**  
   Download DEM data for Nepal, ensuring it is clipped to Nepal's boundary. This DEM data provides the necessary elevation context for visualizing the roads.

6. **Reproject DEM Data (Optional)**  
   Optionally, reproject the DEM data to **Lambert Azimuthal Equal Area (LAEA)** projection. This step is optional but may improve the spatial accuracy of the visualization.

7. **Simplify and Filter Road Data**  
   Filter the road data to retain only relevant road classes, such as "primary," "secondary," "tertiary," and "residential." Simplify and reproject the road shapefile for better compatibility with the DEM data.

8. **Convert DEM Data to Matrix**  
   Convert the reprojected DEM raster into a matrix format, suitable for visualization using the **rayshader** package.

9. **Render 3D Map and Overlay Road Data**  
   Use **rayshader** to create a 3D visualization of the DEM and overlay the road data onto it, providing elevation context for the road network.

10. **Render and Save High-Quality Image**  
    Save the rendered 3D map as a high-quality image. Apply **HDR lighting** to enhance the visual output, making the map more realistic and detailed.

---

**Conclusion:**  
This project demonstrates how to create a 3D visualization of the road network in Nepal using DEM and OSM data in R. By following these steps, you can replicate similar visualizations for other regions by modifying the country boundary and OSM data.

---

**Optional:**  
You can download OSM data for other regions from **Geofabrik** using the following link:  
[Geofabrik Download](https://download.geofabrik.de/).


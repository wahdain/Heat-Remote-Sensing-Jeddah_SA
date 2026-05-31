
# Landsat Thermal & Urban Heat Analysis (Jeddah, SA)

An automated Python pipeline designed to process, clean, and analyze Landsat Level-2 satellite imagery for Land Surface Temperature (LST) modeling and microclimate auditing across Jeddah, Saudi Arabia.

### 📌 Core Functionality

* **Raw Data Ingestion:** Reads multi-spectral optical bands (Red, Green, Blue) and Thermal Infrared data (Band 10) directly from raw Landsat satellite files.
* **Physics Calibration:** Translates raw digital numbers into real-world values, converting the thermal band into absolute Land Surface Temperature (LST) measured in Celsius (°C).
* **Bitwise Quality Cleansing:** Uses binary bit-shifting on the satellite's quality pixel band to automatically identify and scrub out errors like clouds, shadows, and empty background space.
* **Data Correction Verification:** Filters out extreme atmospheric noise—such as freezing cloud-top temperatures—restoring the scene's true average temperature data from a skewed sub-zero state to a realistic ground-truth range.
* **Coordinate Reprojection:** Translates the image's native map grid from meters into universal geographic Latitude and Longitude degrees using high-speed matrix transformation.
* **Targeted Location Queries:** Allows users to input any real-world global coordinate to pinpoint its exact pixel location, pull its clear-sky temperature, and verify it wasn't hidden by a cloud.
* **Microclimate Spatial Profiling:** Extracts a horizontal slice across the data array to map a continuous 3-kilometer thermal wave, showing how heat fluctuates across the surrounding landscape.
* **Dual-Scale Dashboard Visuals:** Generates presentation-ready comparative maps, displaying a broad regional overview alongside a high-magnification local zoom-in window centered on the target asset.

---
*Developed for advanced geospatial analysis of Urban Heat Islands (UHI) and climate macro-data environments.*

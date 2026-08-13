# GHCN-D United States Station Map

🌍 **Live Interactive Map:** [https://sdiggs.github.io/ghcn-d](https://sdiggs.github.io/ghcn-d)

## About This Project

This repository hosts an interactive leaflet map visualizing the geographical distribution of United States weather stations included in the **Global Historical Climatology Network-Daily (GHCN-D)**. 

The map dynamically clusters thousands of individual stations across the Contiguous U.S. (CONUS), Alaska, Hawaii, and U.S. territories. By zooming in, users can view specific weather station locations and their unique identification codes.

### Context & Application

This map was generated to better understand the dense ground-based (in situ) observation networks that provide the foundational baseline data for extreme weather research. Datasets like the GHCN-D are heavily relied upon to validate remotely sensed data (such as NEXRAD radar and satellite precipitation integrations) and are critical components in creating high-resolution, serially complete geospatial models, such as the *Extreme Precipitation Event Database for the Contiguous U.S.*

## Core Data Source

The table below outlines the primary data stream mapped in this repository:

| Data Stream / Measurement | 1-Sentence Description | Valid URL | PI & Funding Source | Country / Agency & Institution |
| :--- | :--- | :--- | :--- | :--- |
| **GHCN-D**<br>(Global Historical Climatology Network-Daily) | A foundational database of daily climate records (precipitation, temperature) integrated from over 100,000 land surface stations and global mesonets. | [ncei.noaa.gov/products/land-based-station/global-historical-climatology-network-daily](https://www.ncei.noaa.gov/products/land-based-station/global-historical-climatology-network-daily) | **Funding:**<br>National Oceanic and Atmospheric Administration (NOAA) | **USA**<br><br>NOAA NCEI<br>(National Centers for Environmental Information) |

## Local Generation

If you wish to generate this map locally, the underlying Python script utilizes the `pandas` and `folium` libraries to parse the live GHCN-D inventory text file (`ghcnd-inventory.txt`), filter for U.S. FIPS country codes (`US`), and render the clustered coordinate points into an `index.html` file.
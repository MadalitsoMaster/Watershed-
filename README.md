# Watershed Delineation for Blantyre District

## Overview
This repository contains Python code for delineating a watershed for the Blantyre district in Malawi using a Digital Elevation Model (DEM). The script computes flow direction, flow accumulation, extracts streams, and delineates the watershed based on a manual or automatic pour point selection.

## Code Description
The Python script (`watershed_delineation.py`) performs the following tasks:
* Reprojects the DEM to a metric UTM zone for accurate distance calculations.
* Fills sinks in the DEM using an iterative approach.
* Computes D8 flow direction and flow accumulation.
* Extracts streams based on a user-defined threshold.
* Delineates the watershed for a specified or automatically chosen pour point.
* Saves outputs as rasters and shapefiles.

## Requirements
* Python 3.x
* `rasterio`, `geopandas`, `numpy`, `matplotlib`, `pyproj`

## Usage
1. Adjust user configurations in the script (e.g., `project_folder`, `dem_path`, `stream_threshold`).
2. Run the script.
3. Outputs will be saved in the specified project folder.

## Outputs
* `flowdir_d8.tif`, `flowaccum_d8.tif`, `streams_d8.tif`, `watershed_mask.tif`, `watershed_polygon.shp`, `streams_vector.shp`
* `watershed_stats.txt` containing basin statistics.
* `watershed_map.png` visualizing the watershed.

## Example Output
![Watershed Map](watershed_map.png)

## Notes
* Adjust the `stream_threshold` for stream extraction based on your needs.
* Pour point can be manually specified or automatically chosen from river shapefiles.

## License
MIT License

## Author
Madalitso Master an Environmental Data Analyst

## Contact
For questions or collaborations, please open an issue or contact via GitHub.

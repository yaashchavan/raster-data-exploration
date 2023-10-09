# raster-data-exploration


This README provides an overview of a Python script for clipping a raster image using a vector polygon and performing basic analysis on the clipped region. The code uses popular geospatial libraries such as Rasterio, Geopandas, Shapely, and Matplotlib. The script is intended to be a helpful starting point for geospatial data processing tasks.

## Prerequisites

Before running the code, ensure that you have the following prerequisites installed:

- Python (>=3.6)
- Rasterio
- Geopandas
- Shapely
- Fiona
- Rioxarray
- Matplotlib
- dask
- dask_image

You can install these dependencies using `pip` / `conda`


## Usage

1. Place your raster image (e.g., `"TCI.tif"`) and vector polygon (e.g., `"polygon.geojson"`) in the same directory as the script.

2. Modify the following lines in the script to specify your input files:

   ```python
   raster_data = rioxarray.open_rasterio("TCI.tif")
   polygon = gpd.read_file('polygon.geojson')
   ```

3. Run the script. It will clip the raster using the provided polygon and display the clipped region.

4. The script also calculates the mean pixel value within the clipped region and prints it to the console.

## Code Explanation

- The script opens the raster file and the vector polygon using Rasterio and Geopandas, respectively.

- It ensures that both the raster and polygon have the same coordinate reference system (CRS).

- The script clips the raster using the polygon geometry and calculates the mean pixel value within the clipped region.

- It creates a binary mask to identify zero values in the clipped raster and counts the number of zero values.

- The mean pixel value and the number of zero values are printed to the console.

- The clipped raster is saved as `"cliped_TCI.tif"`.

- Finally, it displays the clipped region using Matplotlib.


## Author

Yash Chavan

If you have any questions or encounter any issues, please feel free to contact the author at yashcr0@gmail.com.


# NOAA Sea Surface Temperature (SST) Data Processing

This project extracts Sea Surface Temperature (SST) data for a region (e.g. the North Atlantic) from daily .nc files (NetCDF format) provided by [NOAA](https://www.ncei.noaa.gov/products/optimum-interpolation-sst). The files are processed to calculate monthly average temperatures for each latitude/longitude grid cell within the selected region.


## Dependencies

You need the following packages installed (tested with Python 3.11.5): 

- xarray==2023.12.0
- netCDF4
- pandas

## Directory Structure

```sh
data/
└── 2023/
    ├── oisst-avhrr-v02r01.20230101.nc
    ├── oisst-avhrr-v02r01.20230201.nc
    ├── ...
```

## Notebook Structure

1. Exploring the Data Structure: Section to get familiar with NetCDF4 formats
2. Scaling Up: Section to actually prepare the data.


## Process Workflow (Scaling Up Section)

1. Download Files

Get the files for one year. Each file will be used for the calculation of the mean temperature. For this example I chose the file from the first of the month resulting in 12 files for one year.

2. Load and Sort Files

The script lists all .nc files in the data/2023/ folder and ensures they are processed in chronological order by extracting the date (YYYYMMDD) from each filename and sorting accordingly.

3. Extract Region of Interest

From each file, the script extracts SST data for the North Atlantic, defined roughly as:
- Latitude: 30°N to 60°N
- Longitude: 280°E to 360°E (which corresponds to 100°W to 0°W in the Atlantic)

4. Combine Data

For each file, the extracted SST data (with its lat/lon coordinates and timestamp) is saved into a DataFrame. All daily DataFrames are combined into a single DataFrame for the year.

5. Calculate Monthly Mean

For each grid cell (lat/lon position), the average SST is calculated across all days in the year.

7. Add Metadata

The year (2023 in this case) is added to the final DataFrame.

8. Save to CSV

The final result is saved to a CSV file (north_atlantic_sst_2023.csv), ready for further analysis.
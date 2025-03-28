# NOAA Sea Surface Temperature (SST) Data Processing

This project extracts Sea Surface Temperature (SST) data for a region (e.g. the North Atlantic) from daily .nc files (NetCDF format) provided by [NOAA](https://www.ncei.noaa.gov/products/optimum-interpolation-sst). The files are processed to calculate monthly average temperatures for each latitude/longitude grid cell within the selected region agross years.

See also the [NOAA Webscraper](https://github.com/hslu-dda/dda-introduction-to-python/tree/main/07_Data_Applications/noaa-webscraper) to collect the necessary files. 


## Dependencies

You need the following packages installed (tested with Python 3.11.5): 

- xarray==2023.12.0
- netCDF4
- pandas

## Directory Structure

```sh
data/
└── 199301/
    ├── oisst-avhrr-v02r01.19930101.nc
    ├── oisst-avhrr-v02r01.19930102.nc
    ├── ...
└── 199302/
    ├── oisst-avhrr-v02r01.19930201.nc
    ├── oisst-avhrr-v02r01.19930202.nc
    ├── ...
```

## Notebook Structure

1. Exploring the Data Structure: Section to get familiar with NetCDF4 formats.
2. Scaling Up: Section to actually prepare the data.


## Process Workflow (Scaling Up Section)

### 1. Download Files

Use the [NOAA Webscraper](https://github.com/hslu-dda/dda-introduction-to-python/tree/main/07_Data_Applications/noaa-webscraper) to create a folder for each YEARMONTH (e.g. `199301`). Within each of those folders the webscraper will collect one .nc file per day. These files will be used to calculate the mean SST per month. 

### 2. Settings

Set the `BASE_DIR` where all the YEARMONTH folders are located. Define `START_YEAR` and `END_YEAR` to be able to control what you process. 

Set the area for which you want the SST to be calculated. See Section 1 of the Notebook (➡️ «Understanding Longitude and Latitude») for more information. 

### 3. Calculate Montly Mean

The function `process_sst_data()` takes care of everything. It returns a dataframe with an montly mean for each location.

### 4. Further Data Adjustments

The longitude needs to be converted from the 0 to 360 format to the -180 to 180 format (also see Section 1 of the Notebook ➡️ «Understanding Longitude and Latitude» for more information)

You can also remove coordinates with no SST value (land mass), select only one year or **bin** the coordinates to reduce the resolution for mapping visualizations. 

### 5. Export

As the name says. 🥷 Have fun, may your code run smoothly!
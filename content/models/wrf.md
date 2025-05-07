# Model Name: Weather Research and Forecast Model 

Team Name : NCAR

This page describes two regional climate simulations:
- CONUS404 
- South America Regional 

Both are conducted with the Weather Research and Forecast (WRF) model

## CONUS404

CONUS404 is a unique, high-resolution hydro-climate dataset appropriate for forcing hydrological models and conducting meteorological analysis over the conterminous United States. CONUS404, so named because it covers the CONterminous United States for over 40 years at 4 km resolution, was produced by the Weather Research and Forecasting (WRF) model simulations run by NCAR as part of a collaboration with the USGS Water Mission Area. The CONUS404 includes 42 years of data (water years 1980-2021) and the spatial domain extends beyond the CONUS into Canada and Mexico, thereby capturing transboundary river basins and covering all contributing areas for CONUS surface waters.

The CONUS404 dataset, produced using WRF version 3.9.1.1, is the successor to the CONUS1 dataset in d612000 (Liu, et al. 2017) with improved representation of weather and climate conditions in the central United States due to the addition of a shallow groundwater module and several other improvements in the NOAH-Multiparameterization land surface model. It also uses a more up-to-date and higher-resolution reanalysis dataset (ERA5) as input and covers a longer period than CONUS1.

Path to raw data on NCAR's glade system: /glade/campaign/collections/rda/data/ds559.0/ 
Path to HEALPix/zarr subset of this dataset: /glade/derecho/scratch/digital-earths-hackathon/conus404/healpix/

More data is available (not in HEALPix or zarr) at: https://rda.ucar.edu/datasets/d559000/


### CONUS404 References

1. Rasmussen, R.M., F. Chen, C.H. Liu, K. Ikeda, A. Prein, J. Kim, T. Schneider, A. Dai, D. Gochis, A. Dugger, Y. Zhang, A. Jaye, J. Dudhia, C. He, M. Harrold, L. Xue, S. Chen, A. Newman, E. Dougherty, R. Abolafia-Rozenzweig, N. Lybarger, R. Viger, D. Lesmes, K. Skalak, J. Brakebill, D. Cline, K. Dunne, K. Rasmussen, G. Miguez-Macho, 2023: CONUS404: The NCAR-USGS 4-km long-term regional hydroclimate reanalysis over the CONUS. Bulletin American Meteorological Society, 01 August 2023, Pages: E1382 to E1408, DOI: https://doi.org/10.1175/BAMS-D-21-0326.1

2. Rasmussen, R.M., Chen, F., Liu, C., Ikeda, K., Prein, A., Kim, J., Schneider, T., Dai, A., Gochis, D., Dugger, A., Zhang, Y., Jaye, A., Dudhia, J., He, C., Harrold, M., Xue, L., Chen, S., Newman, A., Dougherty, E., Abolafia-Rozenzweig, R., Lybarger, N., R. Viger, Dunne, K., Rasmussen, K., Miguez-Macho, G., 2023, Four-kilometer long-term regional hydroclimate reanalysis over the conterminous United States (CONUS), 1979-2020: U.S. Geological Survey data release, https://doi.org/10.5066/P9PHPK4F


### Citation for Use

Rasmussen, R. M., C. Liu, K. Ikeda, F. Chen, J. Kim, T. Schneider, D. Gochis, A. Dugger, and R. Viger. 2023. Four-kilometer long-term regional hydroclimate reanalysis over the conterminous United States (CONUS). Research Data Archive at the National Center for Atmospheric Research, Computational and Information Systems Laboratory. https://doi.org/10.5065/ZYY0-Y036.

### Simulation Details

- Simulation DOI: 10.5065/ZYY0-Y036
- NCAR RDA Dataset: d559000
- Resolution: 4km
- Simulation Period: 1979-10-01 00:00 +0000 to 2022-09-30 23:00 +0000 (Entire dataset), only 2020 converted for the Hackathon

## Convection-permitting Simulation over South America

A high resolution convection-permitting climate change simulation was performed at 4 km grid spacing covering the entire continent of South America. The simulation was performed using Weather Research Forecasting (WRF) model. This dataset is from a 22-year simulation representing the current climate between January 2001 and January 2022. ERA5 data was used to initialize the model and force boundary every 3 hours. This high resolution simulation allowed for much improved representation of topography, convection, and orographic precipitation and snowpack, resulting in a unique dataset that can be used to study the hydroclimate processes in South America.

Path to raw data on NCAR's glade system: /glade/campaign/collections/rda/data/ds616.0/ 
Path to HEALPix/zarr subset of this dataset: /glade/derecho/scratch/digital-earths-hackathon/samerica/healpix/

More data is available (not in HEALPix or zarr) at: https://rda.ucar.edu/datasets/d616000

### Citation

Rasmussen, R., C. Liu, K. Ikeda, and F. Dominguez. 2022. Multi-decadal Convection-permitting Simulation of Current Climate over South America using WRF. Research Data Archive at the National Center for Atmospheric Research, Computational and Information Systems Laboratory. https://doi.org/10.5065/6XQW-ZB02.

### Simulation Details

- DOI: 10.5065/6XQW-ZB02
- NCAR RDA Dataset: d616000
- Resolution: 4km
- Simulation period: 1999-12-31 00:00 +0000 to 2022-01-01 00:00 +0000 (Entire dataset), only 2020 converted for hackathon

# Model Name: Weather Research and Forecast Model

Team Name : NCAR

## Model description: 
CONUS404 and SAAG Regional Climate Simulations

## Contact
See links below.

## Simulation Details

### SAAG Simulation
A high resolution convection-permitting climate change simulation was performed at 4 km grid spacing covering the entire continent of South America. The simulation was performed using Weather Research Forecasting (WRF) model. This dataset is from a 22-year simulation representing the current climate between January 2001 and January 2022. ERA5 data was used to initialize the model and force boundary every 3 hours. This high resolution simulation allowed for much improved representation of topography, convection, and orographic precipitation and snowpack, resulting in a unique dataset that can be used to study the hydroclimate processes in South America.

- WRF version 4.1.5 (with modifications)
- Grid cells:  1,472 × 2,028 grid points with 61 vertical levels extending to 10 hPa
- Model physics: 
  + Thompson microphysics (Thompson and Eidhammer, 2014) 
  + Yonsei University (YSU) boundary layer  (Hong et al. 2006)
  + Noah MP land surface model  (Niu et al. 2011) 
  + Rapid Radiative Transfer Model (Iacono et al. 2008)
  + Miguez-Macho and Fan (MMF) groundwater scheme (Miguez-Macho et al., 2007)
- Resolution: 4km
- Simulation Period: January 2001 to January 2022
- Model Link: https://rda.ucar.edu/datasets/d616000/ 

#### Data notes

- Temporal resolution 2D output: 1-hourly + 15 minutes for selected variables (e.g. precipitation)
- Temporal resolution 3D output: 3-hourly
- Access on glade: /glade/campaign/collections/rda/data/ds616.0/
- Variables: https://docs.google.com/spreadsheets/d/1F2kbzxp33V1TB8hx8G-Nv5I1UCvJg278bO5PjvXBQdQ/edit?gid=0#gid=0 


### CONUS404 Simulation

[CONUS404](https://www.usgs.gov/data/conus404-four-kilometer-long-term-regional-hydroclimate-reanalysis-over-conterminous-united) is a unique, high-resolution hydro-climate dataset appropriate for forcing hydrological models and conducting meteorological analysis over the conterminous United States. CONUS404, so named because it covers the CONterminous United States for over 40 years at 4 km resolution, was produced by the Weather Research and Forecasting (WRF) model simulations run by NCAR as part of a collaboration with the USGS Water Mission Area. The CONUS404 includes 42 years of data (water years 1980-2021) and the spatial domain extends beyond the CONUS into Canada and Mexico, thereby capturing transboundary river basins and covering all contributing areas for CONUS surface waters.

- WRF version 3.9.1.1

- General setup 
  + Horizontal grid spacing: 4 km grid spacing 
  + Domain: 1368 x 1016 x 51 (vertical) grid cells 
  + 3-hourly update of lateral boundary conditions using ERA5 
  + Spectral nudging of temperature, winds, geopotential heights every 2 minutes above boundary layer, wavenumbers 1-3 for zonal and wavenumbers 1-2 for meridional
- Physics packages
  + Thompson and Eidhammer (2014) microphysics
  + Yonsei University (YSU) planetary boundary layer scheme (Hong et al. 2006)
  + Rapid Radiative Transfer Model (RRTMG) radiation scheme (Iacono et al. 2008)
  + Noah MP: multi parameterization land surface model (Noah-MP; Niu et al. 2011) coupled to the Miguez-Macho–Fan groundwater scheme (MMF; Miguez-Macho et al. 2007; Barlage et al. 2021)

#### Data notes
- Note that the data is organized into water years (October - September)!

- Temporal resolution 2D output: 1-hourly + 15 minutes for selected variables (e.g. precipitation)
- Temporal resolution 3D output: 3-hourly 

- Access and documentation of data at NCAR’s Reseach Data Archive: https://rda.ucar.edu/datasets/d559000/ 
- Access on glade: /glade/campaign/collections/rda/data/ds559.0/
- Access and documentation on Microsoft Planetary Computer: https://planetarycomputer.microsoft.com/dataset/conus404#overview 



# Model Name: IFS-FESOM
- Team Name : ECMWF/AWI: IFS-FESOM - Integrated Forecasting System (IFS) coupled to Finite Volume Sea Ice Ocean Model (FESOM2)
- Model Link: [IFS](https://www.ecmwf.int/en/forecasts/documentation-and-support/changes-ecmwf-model) / [FESOM](https://fesom.de)

## Model description: 

The Integrated Forecasting System (IFS), developed at ECMWF, is a spectral-transform atmospheric model with two-time-level semi-implicit, semi-Lagrangian time stepping (Temperton et al., 2001; Hortal, 2002; Diamantakis and Váňa, 2021). It is coupled to other Earth system components (land, waves, ocean, sea ice). The global hackathon simulations at 2.8km are with the IFS-FESOM configuration (Rackow et al. 2025), coupled to the FESOM2 ocean-sea ice model.

**Reference:**

Rackow, T., Pedruzo-Bagazgoitia, X., Becker, T., Milinski, S., Sandu, I., Aguridan, R., Bechtold, P., Beyer, S., Bidlot, J., Boussetta, S., Deconinck, W., Diamantakis, M., Dueben, P., Dutra, E., Forbes, R., Ghosh, R., Goessling, H. F., Hadade, I., Hegewald, J., Jung, T., Keeley, S., Kluft, L., Koldunov, N., Koldunov, A., Kölling, T., Kousal, J., Kühnlein, C., Maciel, P., Mogensen, K., Quintino, T., Polichtchouk, I., Reuter, B., Sármány, D., Scholz, P., Sidorenko, D., Streffing, J., Sützl, B., Takasuka, D., Tietsche, S., Valentini, M., Vannière, B., Wedi, N., Zampieri, L., and Ziemen, F.: **Multi-year simulations at kilometre scale with the Integrated Forecasting System coupled to FESOM2.5 and NEMOv3.4**, Geosci. Model Dev., 18, 33–69, https://doi.org/10.5194/gmd-18-33-2025, 2025. [BibTeX](https://gmd.copernicus.org/articles/18/33/2025/gmd-18-33-2025.bib)

### Contact:
-  [Thomas Rackow](mailto:thomas.rackow@ecmwf.int)

## Simulation Details

Simulation DOI: (please cite above reference for the moment)

- Resolution: Global atmosphere at **2.8 km** / multi-resolution sea ice-ocean grid down to 5km 
- Simulation Period(s): **2x January 2020 - February 2021 (2x 14 months)**
- 2 configurations: First, with reduced cloud base mass flux (**"RCBMF"**), and second with deep convection parameterisation OFF (**"DEEPOFF"**)

## Data notes (online)

- **We provide the main hackathon simulation "RCBMF" via the s3 [DKRZ Object Store](https://github.com/digital-earths-global-hackathon/hk25/blob/main/content/simulations.md), with variables mostly following CF naming for the [HK25 data request](https://digital-earths-global-hackathon.github.io/hosting/technical/data_request.html)** (at 2.8km spatial resolution, coupled, 14 months, with reduced cloud base mass flux).
- [TODO: update incorrect metadata; for variables of identical name in both models, the units should be what you expect from the according ICON variables].
- Variables sst & siconc are masked with 9999 over land; use .where(lambda x:x!=9999) to mask out the land.
  
- Via the EERIE cloud, we provide both **"RCBMF"** and **"DEEPOFF"** online, with original IFS variable names. Use the [Parameter Database](https://codes.ecmwf.int/grib/param-db/) for more information.

## Data notes (EU local access)

- (add more information, to do)
- (temporarily: access to "RCBMF", "DEEPOFF", and multi-decadal nextGEMS simulations at 9km resolution possible via
cat = intake.open_catalog("https://data.nextgems-h2020.eu/catalog.yaml"). See also the [easy.gems documentation](https://easy.gems.dkrz.de/DYAMOND/NextGEMS/prefinal.html))
- access to DestinE multi-decadal simulations possible via [DESP (more information here)](https://github.com/digital-earths-global-hackathon/hk25-teams/blob/main/hk25-DestinE/intro/introduction.md), requires registration

## Basic plotting
You can start from the [simple plotting script](https://github.com/digital-earths-global-hackathon/hk25-teams/blob/main/hk25-tutorials/simple_plot.ipynb). If there are any issues when applying this on IFS data (tested that it works!), contact [Thomas Rackow](mailto:thomas.rackow@ecmwf.int) via mail or on Mattermost.

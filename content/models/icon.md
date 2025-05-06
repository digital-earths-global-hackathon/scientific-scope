

# Model Name: ICON

- Team Name : MPI-Met, Hamburg
- Model Link: [ICON](https://icon-model.org/) 

## Model description

The ICON atmosphere model for this global hackathon experiment evolves from earlier version used in the Dyamond model intercomparison project ([Stevens et al., 2019][S2019]) and the nextGEMS project ([Segura et al., 2025][S2025]). The non-hydrostatic dynamics and the tracer transport are computed on a triangular horizontal grid that is derived from the icosahedron and a height based terrain following vertical grid ([Zängl et al., QJRMS, 2015][Z2015]). Here the horizontal grid has a nominal resolution of 2.5 km and the vertical grid has 90 levels up to 75km height. The physics includes cloud microphysics, radiation and turbulent mixing. Overall the setup is similar to that of the G_AO_2.5km experiment of [Hohenegger et al. (2023)][H2023].

The physics setup is however different. The goal of these changes is to explore the combined effects of some modifications, which have been tested in preceding shorter and lower resolution expriments, and which reduce some of the sytematic biases of earlier Dyamond and nextGEMS simulations as for example a double ITCZ even for prescribed SST, too high global mean precipitation, too dry tropical atmosphere, too strong lapse rate and hence a cold bias in the middle and upper tropical troposphere. The following experimental modifcations have been introduced:

- Turbulent fluxes: Surface fluxes are strengthened by inceasing the minimum near surface wind speed that is used for the parameterization of the surface fluxes from 1 to 4 m/s. This boosts moisture fluxes in the equatorial Pacific and showed to reduce the double ITCZ and generally improves the tropical precipitation patterns.

- Cloud microphysics: The fall speed of rain is reduced from 14.6 m/s to 4.0 m/s, thus reduced by a factor of 3.7. This increases the residence time of rain in the atmosphere which mainly moistens the lower troposphere. As an expected side effect this however increases the rain water content of the atmosphere by a factor of 3.7.

- Cloud microphysics: The fall speed of cloud ice is reduced from 1.25 m/s to 0.4 m/s, thus reduced by a factor of 3.1. This increases the residence time of ice and leads to changes in the balance between the different processes in ice clouds as well as mixed phase clouds. This leads to a moistening and warming in the middle and upper tropical troposphere and a small reduction in global mean precipitation. In addition, however, the cloud cover is increased and the OLR reduced, which changes the OLR by ~10 W/m2.

Further less critical modifications:

- The soil physics is updated, allowing now for dynamical heat capacity and conductivity, and for supercooled water.

- Ozone for shortwave radiation is simulated by the linearized ozone scheme by [Cariolle and Teyssèdre (2007)][C2007] and tracer advection instead of prescribing ozone from external data. This modification is active from the beginning of the simulation until 2020-05-28T00:00:00Z. Thereafter ozone was prescribed from external data. The reason for this change was a series of simulation crashes which lead to the suspect that this was related to the ozone scheme. Later, however, it turned out that these crashes had a technical origin, but the change remained to the end of the simulation.

This model setup is therefore experimental with the main purpose to generate a different simulation compared to earlier ones, and thus to provide learning material.

---

### Model configuration

#### Time step

- The model time step is dt_atm = 20s. This is the base period for calling the dynamical core, the tracer transport, the horizontal diffusion and the physics.
- The dynamical core has 5 sub-steps per model time step
- The tracer transport scheme has 3 sub steps per model time step
- The radiative transfer is computed at a time step of dt_rad = 15 min, using a solar zenith angle at the current time + (dt_rad-dt_atm)/2.
- Radiative temperature tendencies are computed every model time step taking into account the current heat capacity of air and scaling the shortwave fluxes to the solar zenith angle of the current time.

#### Coupling of processes

dynamics -> horizontal diffusion -> tracer advection -> cloud microphysics -> radiation -> turbulent mixing & surface

#### Horizontal grid

Triangular grid derived from the spherical icosahedron
- R2B10 = 11-fold bisection of the edges of the spherical icosahedron
- rotation of the southern hemisphere by 36° around N-S axis to make the grid symmetric about the equator
- optimization of edge lengths for numerical operators
- 83,886,080 cells
- nominal resolution dx = ~2.5 km (see Table 1 in [Giorgetta et al., 2018][G2018]).

#### Vertical grid

Generalized smooth-level vertical coordinate ([Leuenberger et al., 2010][L2010])
- 91 half levels = boundaries of layers
- 90 full levels at mid height between upper and lower half level
- top half level at zh(jk=1) = 75 km
- constant  height  levels: half levels 1 to 32, from 75 km to 22.5 km
- terrain following levels: half levels 33 to 91, from 22.5 km to the surface

#### Grid staggering

- Velocity components in the edge centers and scalars in the cell center, as illustrated in Figure 4 of [Giorgetta et al. (2018)][G2018].

#### Initial conditions

- From IFS for date 2020-01-01T00:00:00Z

#### External data

- SST and SIC as monthly mean fields pre-processed for usage in AMIP simulations
- well mixed greenhouse gases CO2, CH4, N2O, CFC11, CFC12 as annual means
- O3 simulated or prescribed from monthly and zonal mean fields

#### Code

- icon-mpim:feature-dy3ha-p-experiments at commit b9c9da5cef4e7faadf13c2fe213de0c990c94bf3 (https://gitlab.dkrz.de/icon/icon-mpim/-/tree/b9c9da5cef4e7faadf13c2fe213de0c990c94bf3)

---

### Simulation

#### Simulation period

- 14 months from 2020-01-01T00:00:00Z to 2021-03-01T00:00:00Z

#### Simulation name

- d3hp003

#### Simulation modifications

Due to crashes, of technical nature as it turned out later, some adjustments of the model setup happened during the course of the simulation:

- 2020-05-28T00:00:00Z: dt_atm: 20s -> 15s, ozone: prognostic -> external data, zmaxcloudy: 33km -> 22.5km (1), correction for proper daily means of 3d fields on pressure levels
- 2020-06-05T00:00:00Z: dt_atm: 15s -> 20s
- 2020-07-27T00:00:00Z: dt_atm: 20s -> 18s, dynamics substeps: 5 -> 6
- 2020-08-04T00:00:00Z: dt_atm: 18s -> 20s, dynamics substeps: 6 -> 5

(1) zmaxcloudy is the maximum height up to which cloud microphysics is computed

---

### Output

#### Standard output

The standard output follows the data request (https://digital-earths-global-hackathon.github.io/hosting/technical/data_request.html) with a few deviations:
- `mrso`, the soil liquid water content in kg/m2 is available as 3d field for 5 soil levels instead of a vertical sum over all soil levels.
- `swe`, the liquid water content of surface snow is not available over land ice so that this field is zero in areas like Antarctica and Greenland

### Additional output

- `rva`, relative vorticity in the atmosphere in 1/s, as 3d field on 3 pressure levels: 850, 500 and 300 hPa, 3-hourly, instantaneous
- Energy content of the atmosphere in J/m2, 3-hourly, instantaneous
  - `egpvi`: geopotential energy content
  - `einvi`: internal energy content
  - `ekhvi`: horizontal kinetic energy content
  - `ekvvi`: vertical kinetic energy content
- Tendencies of energy content of the atmosphere in J/m2/s, 3-hourly, time mean
  - `tend_egpdynvi`: tendency of geopotential energy content due to dynamics
  - `tend_eindynvi`: tendency of internal energy content due to dynamics
  - `tend_eincldvi`: tendency of internal energy content due to cloud microphysics
  - `tend_einradvi`: tendency of internal energy content due to radiation
  - `tend_eintmxvi`: tendency of internal energy content due to turbulent mixing
  - `tend_ekhdynvi`: tendency of horizontal kinetic energy content dynamics
  - `tend_ekvdynvi`: tendency of vertical kinetic energy content due to dynamics
- Daily means of all fields
  - **Restriction**: For 3d fields given on pressure level, until 2020-05-28 the daily means are the averages of the four 6-hourly instantaneous fields of a day. Only after 2020-05-28 the daily means include all model time steps of a day.

#### Output base directory

- levante.dkrz.de:/work/bm1235/k203123/dy3ha-p/experiments/d3hp003/outdata/d3hp003.zarr

- Output fields are stored in individual Zarr2 stores named `<period>_<inst/mean>_z<level>_atm` for different output periods, for instantaneous data and time averaged data, and for different HEALPix zoom levels, where:
  - period: CONST, PT1H, PT3H, PT6H, P1D
  - level: 11 to 0

---

### Quickplots

The so-called "quickplots" provide a preview of the model simulation fields at HEALPix zoom level 7, including for some fields differences to ERA5 and CERES.

Three collections of plots are contained in [icon_r2b10l90_d3hp003](https://swiftbrowser.dkrz.de/public/dkrz_e59fa4f2fcac49f2aec87e9b1d1ae0eb/icon_r2b10l90_d3hp003/):
- Folders d3hp003-ERA5_<time period>:
  - atm_zon.html: zonal means of 3d fields and where possible differences to ERA5
  - bot_map.html: 2d model fields and where possible differences to ERA5
- Folders d3hp003-CERES_<time period>:
  - bot_map_CERES.html: 2d model fields (same as above) and where possible differences to CERES

Available time periods:
- monthly mean: 2020-01 until 2021-02
- seasonal mean: 202003-202005 (MAM), 202006-202008 (JJA), 202009-202011 (SON), 202012-202102 (DJF)
- annual mean: 202003-202102

---

### Contact

[Marco Giorgetta](mailto:marco.giorgetta@mpimet.mpg.de)

---

**References**

[C2007]: https://doi.org/10.5194/acp-7-2183-2007 'Cariolle, D. and Teyssèdre, H. (2007). A revised linear ozone photochemistry parameterization for use in transport and general circulation models: multi-annual simulations. Atmos. Chem. Phys., 7. https://doi.org/10.5194/acp-7-2183-2007'

[G2018]: https://doi.org/10.1029/2017MS001242 'Giorgetta, M. A., Brokopf, R., Crueger, T., Esch, M., Fiedler, S., Helmert, J., et al. (2018). ICON-A, the atmosphere component of the ICON Earth system model: I. Model description. Journal of Advances in Modeling Earth Systems, 10. https://doi.org/10.1029/2017MS001242'

[H2023]: https://doi.org/10.5194/gmd-16-779-2023 'Hohenegger, C., Korn, P., Linardakis, L., Redler, R., Schnur, R., Adamidis, P., et al. (2023). ICON-Sapphire: simulating the components of the Earth system and their interactions at kilometer and subkilometer scales. Geosci. Model Dev., 16. https://doi.org/10.5194/gmd-16-779-2023'

[L2010]:  https://doi.org/10.1175/2010MWR3307.1 'Leuenberger, D., Koller, M., Fuhrer, O., & Schär, C. (2010). A generalization of the SLEVE vertical coordinate. Monthly Weather Review, 138(9). https://doi.org/10.1175/2010MWR3307.1'

[S2025] https://doi.org/10.5194/egusphere-2025-509 'Segura, H., Pedruzo-Bagazgoitia, X., Weiss, P., Müller, S. K., Rackow, T., Lee, J., et al. (2025). nextGEMS: entering the era of kilometer-scale Earth system modeling. EGUsphere [preprint]. https://doi.org/10.5194/egusphere-2025-509'
 
[S2019]: https://doi.org/10.1186/s40645-019-0304-z 'Stevens, B., Satoh, M., Auger, L. et al. (2019). DYAMOND: the DYnamics of the Atmospheric general circulation Modeled On Non-hydrostatic Domains. Prog Earth Planet Sci 6, 61. https://doi.org/10.1186/s40645-019-0304-z'

[Z2015]: https://doi.org/10.1002/qj.2378 'Zängl, G., Reinert, D., Ripodas, P., & Baldauf, M. (2015). The ICON (ICOsahedral Non-hydrostatic) modelling framework of DWD and MPI-M: Description of the non-hydrostatic dynamical core. Quarterly Journal of the Royal Meteorological Society, 141(687). https://doi.org/10.1002/qj.2378'

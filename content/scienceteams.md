---
header_menu: false
---

# Science Teams

Across the different nodes participants will be setting up science teams. These teams will address specific topics as proposed by the team lead, and attempt to engage others in joint analysis. These are open for participants at all nodes to join.

Science teams are given a unique identifier (uid) following the convention ‘hk25-uid’. Each team will also have a lead and an associated repo on github with the same uid. The repo will serve as the primary basis for communication among team members.  Mattermost channels, markdown pads, and video-conference links may also serve as supplemental forms of communications, as indicated on by the README for each team.

{{< toc >}}

---
### Energetics of tropical rainbelts ([hk25-RainBelt](https://github.com/digital-earths-global-hackathon/hk25-teams/tree/main/hk25-RainBelt))

Global km-scale grids permits an explicit representation of convective storms and the processes they entails. Over the tropical ocean, precipitation occurs in a variety of environments. Precipitating regions could be related to strong sea surface temperature gradients and a bottom-heavy circulation (e.g., Eastern Pacific) or a top-heavy circulation, weak SST gradients, and light winds (e.g., Western Pacific). Due to the diversity of pathways in which precipitation occurs, we will analyze how convection is represented across the tropical oceans in the different participating km-scale models using an energetic-moisture framework.

**Coordination**: Hans Segura Cajachagua (hans.segura@mpimet.mpg.de)

#### Sketch of initial activities
* identify the tropical rainbelt
* calculate the entropy forcing and the net precipitation flux at the surface
* compute the type of circulation (top- or bottom-heavy) in the tropical rainbelt
* extract the spectrum of convective coupled equatorial waves

---
### Precipitation over ice-sheets ([hk25-IceSheet](https://github.com/digital-earths-global-hackathon/hk25-teams/tree/main/hk25-IceSheet))

Mass loss of the Greenland and Antarctic ice sheets is an important contributor for current and future sea level rise. To properly drive the surface mass balance calculations in ice sheet models, a realistic simulation of precipitation and surface temperatures is crucial. Regional modeling studies suggest that higher resolution of the atmospheric models driving ice sheet models improves the simulation of processes occurring at the steep margins of the ice sheets, making km-scale global models a promising tool for future coupled atmosphere-ocean-ice sheet modelling as planned for example in the [TerraDT](https://terradt.eu/) project.

In this team we want to compare the simulated surface meteorology over Greenland and Antarctica for participating models and with reanalysis data and observations to assess how suited the models are to drive ice-sheet models.

**Coordination**: Hauke Schmidt (hauke.schmidt@mpimet.mpg.de)

#### Sketch of initial activities:
*	extract model output for the Greenland and Antarctic ice sheets
*	produce precipitation and temperature maps
*	compare annual cycles for regional means and selected locations

---
### Triggering of deep convection ([hk25-ConvTrig](https://github.com/digital-earths-global-hackathon/hk25-teams/tree/main/hk25-ConvTrig))

Convective precipitation within the tropical rainbelts is primarily driven by convective storms.  To better understand the tropical rainbelts as a whole, we want to understand the details of individual convective systems.  An important aspect of individual convective systems is their triggering.  Limited observations and idealized modeling suggest that SST-driven mesoscale boundary layer wind convergence may play a key role in triggering deep convection over tropical oceans, but details are still poorly understood. Km-scale models, which allow an explicit representation of deep convection, are a promising tool to overcome this limited understanding.

In this team, we will test the hypothesis that MCSs over tropical oceans are triggered by mesoscale wind convergence. If possible, we will also look at how mesoscale surface wind convergence depends on mesoscale SST properties.

**Coordination**: Henning Franke (henning.franke@mpimet.mpg.de)

#### Sketch of initial activities
* MCS tracking (together with science teams from other nodes)
* Determine time and location of MCS triggering from MCS tracking results
* Calculate mesoscale surface wind convergence at MCS triggering locations
* Calculate SST gradients and Laplacian.

---
### EarthCARE-Curtains ([hk25-Curtains](https://github.com/digital-earths-global-hackathon/hk25-teams/tree/main/hk25-Curtains))

The goal of this working group is to evaluate the models’ capability of capturing the correct vertical structure of clouds around the globe.

To this end, we propose to extract “virtual curtains” from the simulations alongside the EarthCARE satellite tracks “Curtains" refers to the shape of the dataset, a vertical veil unfolding under the satellite, while “virtual" refers to projection of these 2025 orbit tracks onto the simulated year 2020. Practically, we anticipate to use the upcoming EarthCARE's L2-products for the month of April 2025. We will therefore compare these with all virtual curtains extracted from April month, using a bulk statistical approach. Further, we intend to use the satellite product emulator PAMTRA to convert the model’s output into comparable products such as radar reflectivity. An example of such curtain extraction and conversion is presented in Fig. 2.

**Note:** This science team will closely coordinate with the EarthCARE [cross-cutting](./crosscutting.md) activity.

**Coordination**: Romain Fiévet (romain.fievet@mpimet.mpg.de)

#### Sketch of initial activities
* Recover the EC product and orbital tracks
* Extract the virtual curtain from the models
* Convert these using PAMTRA
* Compare and evaluate the models biases


---
### MCS tracking ([hk25-MCS](https://github.com/digital-earths-global-hackathon/hk25-teams/tree/main/hk25-MCS))

Convective storms, especially those that develop into mesoscale convective systems (MCSs), play a crucial role in producing rainfall and hazardous weather across the globe. While recent studies have shown that DYAMOND models can capture certain aspects of tropical MCSs, such as their frequency and diurnal cycle, significant challenges remain. In particular, accurately representing the distribution of precipitation and its relationship with the surrounding environment continues to be a major hurdle ([Su et al. 2022](https://doi.org/10.2151/jmsj.2022-033); [Feng et al. 2023](https://doi.org/10.1029/2022GL102603); [Song et al. 2024](https://doi.org/10.1029/2024GL109945); [Feng et al. 2025](https://doi.org/10.1029/2024JD042204)).

Previous DYAMOND phases provided two 40-day simulation periods for summer and winter, limiting the statistical robustness of model evaluations. The Digital Earth Global Hackathon will extend these simulations to a full year using multiple global kilometer-scale models, creating an unprecedented opportunity to assess how well they capture the full spectrum of convective storms and extreme events. As part of this effort, we are organizing an MCS tracking activity to develop and apply new analysis tools, exchange insights, and strengthen collaborations within the broader atmospheric science community.

**Coordination**: Zhe Feng (zhe.feng@pnnl.gov)

#### Sketch of initial activities
* Standardize MCS tracking output formats (e.g., netCDF, lat/lon grid, [HEALPix grid](https://healpix.sourceforge.io/index.php))
* Compare simulated MCS statistics against satellite observations
* Extract mesoscale environmental variables surrounding MCS tracks
* Compare simulated MCS environments and relationships with MCS characteristics (lifetime, size, precipitation, etc.) across model ensembles

---

### Shallow circulations in the ITCZ ([hk25-ShallowCirc](https://github.com/digital-earths-global-hackathon/hk25-teams/tree/main/hk25-ShallowCirc))

The intertropical convergence zone (ITCZ) in the eastern parts of the Pacific and Atlantic basins is dominated by bottom-heavy or shallow meridional circulations, with outflow observed at 2-4 km. In this team, we would like to understand the dynamical drivers of shallow meridional circulations as a function of the seasonal cycle using storm resolving simulations. We are interested in characterising the surface and free troposphere controls on the depth of the shallow circulations and testing the hypothesis that the circulation becomes more pronounced as the ITCZ moves poleward.

**Coordination**: Divya Sri Praturi (divya-sri.praturi@mpimet.mpg.de) and Marius Winkler (marius.winkler@mpimet.mpg.de)

#### Sketch of initial activities
* construct the meridional overturning circulation in the eastern Atlantic and Pacific ITCZ
* compute zonal and meridional momentum budgets across pressure levels
* determine the seasonal cycle of the depth of the outflow

---

### Mesoscale structure of stratocumulus ([hk25-StCu](https://github.com/digital-earths-global-hackathon/hk25-teams/tree/main/hk25-StCu))

Low-level clouds over subtropical oceans are important for the energy balance of the planet and climate sensitivity. Their properties and evolution crucially depend on small scale processes. A recent examination of their climatology ([Nowak et al. 2025](https://doi.org/10.1029/2024MS004340)) in two [NextGEMS](https://nextgems-h2020.eu/) global storm-resolving models indicated realistic covariability of stratocumulus and related environmental factors, and the vertical structure of the boundary layer. How is that possible without elaborated model tuning and on the grid which is too large to resolve large turbulent eddies?

It was speculated that the km-scale grid allows to simulate mesoscale circulations which might be sufficient to crudely represent the radiation-turbulence-entrainment-flux feedback regulating the behavior of stratocumuli. We would like to test this hypothesis by inspecting the mesoscale patterns of cloudiness, circulation and precipitation in the models and check whether those patterns comply with the mechanisms proposed to explain the cellular cloud structures evident in observations (see e.g. [Comstock et al. 2005](https://doi.org/10.1175/JAS3567.1), [van Zanten and Stevens 2005](https://doi.org/10.1175/JAS3611.1), [Wood et al. 2011](https://doi.org/10.5194/acp-11-2341-2011)).

**Coordination**: Jakub Nowak (jakub.nowak@mpimet.mpg.de)

#### Sketch of initial activities
* Extract snapshots of subtropical stratocumulus fields
* Asses qualitatively whether the mesoscale cloud patterns are cellular
* Quantify their organization with a chosen statistical metric
* Examine the co-variability of clouds, circulation and precipitation

---

### Global representation of local extremes ([hk25-LocExt](https://github.com/digital-earths-global-hackathon/hk25-teams/tree/main/hk25-LocExt))

Climate extremes can develop on a wide range of spatial scales from continental to local. Global km-scale models allow us a global view on such extremes with local detail important for impacts for the first time. Here, we will use them to quantify the spatial variability lost at coarser resolutions typical for established global models (e.g. from CMIP6 or HighResMIP). This will allow us to identify regions where output resolution matters for the representation of extremes and build understanding of the underlying processes. Comparing different km-scale models will enable us to analyse cases where models agree or diverge and trace them back to model differences, for example in the treatment of deep convection.

In this team we will test what the added value of high-resolution output is for the spatial representation of climate extremes. We also aim to understand potential differences between models.

**Coordination**: Lukas Brunner (lukas.brunner@uni-hamburg.de)

#### Sketch of initial activities
* Calculate extreme indices (e.g., [ETCCDI](https://etccdi.pacificclimate.org/list_27_indices.shtml)) at the highest available resolution from all available models
* Analyze what and where spatial variability is lost at coarser resolutions
* Compare different extreme indices and models and understand disagreements

---

### Tropical Cyclones ([hk25-TropCyc](https://github.com/digital-earths-global-hackathon/hk25-teams/tree/main/hk25-TropCyc))

Tropical Cyclones (TCs) are intense organised convective systems that are responsible for nearly half of the worldwide disaster-related costs (CRED & UNDRR, 2020). Historically, they have been difficult to represent in coarse-resolution climate models because of their small size and their sensitivity to convective parametrisations. It has been shown that increasing resolution to 25km allows models to represent the number and distribution of cyclones correctly (Roberts et al. 2020), but the intensity remains largely underestimated, and the structure is not well represented (Bourdin et al. 2024). Baker et al. (2024) showed that increasing resolution up to 5km improves the realism of intensity, intensification rate, lifecycle and structure of TCs in NextGEMS simulations.

In this team, we will investigate how TCs are represented in the new sets of simulations in terms of statistics, structure, lifecycle and link with the environment.

**Coordination**: Stella Bourdin (stella.bourdin@physics.ox.ac.uk), Alex Baker (alexander.baker@reading.ac.uk), Arthur Avenas (arthur.avenas@esa.int), Xu Chen (chenx@g.ecc.u-tokyo.ac.jp)

#### Sketch of initial activities:
* Track TCs in the simulations using TempestExtremes -> Assess TCs statistics, particularly in terms of intensity and intensification rates
* Retrieve snapshots of tropical cyclones’ structure -> Assess tropical cyclones structure
* Retrieve/compute variables associated with environmental favourability for TC (e.g. GPI) -> Assess how the environment controls TCs, particularly the moisture field and the components of Potential Intensity
* Comparison of TC tracks from re-analyses / models and from satellite observations

---

### How realistic are GSRM clouds? ([hk25-CloudClimato](https://github.com/digital-earths-global-hackathon/hk25-teams/tree/main/hk25-CloudClimato))


This science team will compare GSRM cloud characteristics with diverse climatological observations (in situ, satellite, etc.) to assess the realism of different cloud types in the control climate of various models and identify potential mean state biases. The goal is to publish these analyses in an overview paper that can be used as a a reference for process papers dedicated to more specific analyses of shallow clouds, deep clouds, storm tracks, polar clouds, etc. The hackathon will be used as a kickstarter for this project and hopefully the collaboration will continue afterwards to try and submit the paper rapidly.

Coordination : Emilie Fons (emilie.fons@lmd.ipsl.fr)

#### Sketch of initial activities:
- standardize cloud characteristics that are available in all GSR models. Which models have outputs from a satellite simulator ?
- gather observational data for comparison (e.g., reanalysis, CERES, Earthcare, CMIP, etc.)
- plots : maps, latitudinal profiles, altitude profiles, cloud regime profiles, interranual/seasonal/diurnal variability

---

### Air-sea interaction in the tropics ([hk25-ASintTrops](https://github.com/digital-earths-global-hackathon/hk25-teams/tree/main/hk25-ASintTrops))

This activity is motivated by several open questions on how the tropical boundary layer and moist convection interact with the underlying ocean on scales 2 km - 200 km. For instance, how does the tropical atmosphere respond to SST heterogeneity at those scales? What sets air-sea interaction at low versus high wind speeds, or how do precipitation or cloudiness impact air-sea fluxes and the ocean mixed-layer?

In this team we want to analyze relationships between SST, air-sea fluxes, tropical convection and the ocean mixed at (sub)mesoscales, using those participating models that run a coupled ocean-atmosphere simulation.

Coordination: Louise Nuijens (Louise.Nuijens@tudelft.nl)

#### Sketch of initial activities:
* Analyze air-sea heat fluxes and wind stress as a function of SST, stability and wind speed
* Derive divergence and curl of wind speed and stress across SST gradients
* Derive coupling coefficients to evaluate the atmospheric feedback on wind (stress)
* Analyze mixed-layer depth as a function of air-sea fluxes and wind speed
* Composite air-sea fluxes as a function of cloud cover, radiation and precipitation

---

### Land-Atmosphere Interaction ([hk25-Land](https://github.com/digital-earths-global-hackathon/hk25-teams/tree/main/hk25-Land))

The land-atmosphere interaction is one of the key drivers of Earth's surface water and energy budgets. Among these, soil moisture plays a crucial role by regulating surface heat fluxes, which in turn influence boundary layer development and precipitation. These processes are fundamental to understanding convection, climate feedbacks, and extreme events such as droughts, heatwaves, and floods.
Unlike coarse-resolution global circulation models or regional km-scale models, global km-scale models can explicitly resolve convection and eliminate the need for prescribed large-scale circulation. This enables a more holistic and physically consistent representation of land-atmosphere processes.

In this team, we aim to identify global hotspots of land-atmosphere coupling and evaluate the added value of high-resolution global simulations in capturing the influence of soil moisture on extreme events. Specifically, we will assess how changes in soil moisture affect precipitation, heatwaves, and droughts through their impacts on surface heat fluxes and boundary layer dynamics.

**Coordination**: Ching-Hung Shih (f11229004@ntu.edu.tw)

Sketch of initial activities:
+ Identify global hotspots of land-atmosphere coupling using km-scale model output
+ Quantify soil moisture-precipitation feedback across different regions
+ Analyze where and how spatial variability is introduced in km-scale models compared to coarser-resolution models

---

### Urban ([hk25-Urban](https://github.com/digital-earths-global-hackathon/hk25-teams/tree/main/hk25-Urban))

Current km-scale resolutions open new opportunities to study new aspects of the climate that previously where out of scope. Among these, urban environtments start to be identified as areas with a significant amount of grid points.

More than half of the global population currently lives in urban environtments, how global km-scale models represent these areas is a new topic that requires new paradigms of analyses and experteses. Now is the moment, to incorporate urban specialist from other areas (e.g. regional climate modellers, urban modellers) to start to analyze the urban related dynamics in the global km-scale models.

In this team, we aim to identify how global km-scale models represent urban dynamics (e.g. heat island, local circulation impacts, ...)

**Coordination**: Lluís Fita (lluis.fita@cima.fcen.uba.ar)

Sketch of initial activities:

+ Identify main urban environtments in global km-scale models
+ Quantify urban impact in the surroundings (e.g. heat island)
+ Analyze where and how global km-scale models compared to on-purpose urban modelling initiatives at smaller spatial scales

---
### Hemispheric Albedo Symmetry ([hk25-AlbedoSym](https://github.com/digital-earths-global-hackathon/hk25-teams/tree/main/hk25-AlbedoSym))

Observations of Earth show a persistent, remarkable, and unexplained hemispheric symmetry of albedo, or reflected shortwave radiation. This has been documented for decades, but most reliably so since the creation of a long-term CERES record (see e.g. [Voigt et al. 2013](https://doi.org/10.1175/JCLI-D-12-00132.1), [Datseris and Stevens 2021](https://doi.org/10.1029/2021AV000440), [Jonsson and Bender 2022](https://doi.org/10.1175/JCLI-D-20-0970.1)). The observations show that all-sky symmetry is established through a compensation between clouds and clear-sky reflection: where the NH is about 4 W/m2 brighter from the clear-sky atmosphere, 2 W/m2 brighter from the surface, and 6 W/m2 dimmer from clouds.

However, CMIP class models struggle to reproduce the observed degree of symmetry (e.g., [Rugenstein and Hakuba 2023](https://doi.org/10.1029/2022GL101802), [Jonsson and Bender 2023](https://doi.org/10.5194/esd-14-345-2023), [Crueger et al. 2023](https://doi.org/10.1175/JCLI-D-22-0923.1)). Models show biases away from symmetry in all possible configurations: (1) each hemisphere is too bright, (2) each hemisphere is too dark, (3) NH is too bright, but SH is too dark, or (4) NH is too dark, but SH is too bright. Model biases are strongly linked to cloud biases, so one may speculate that a km-scale model which resolves deep convection may better capture the observed hemispheric symmetry in reflection.

The observed all-sky symmetry exists in the climatology, and has persisted despite significant dimming trends in both hemispheres, but the hemsipheres do deviate from perfect symmetry on shorter monthly timescales. Unfortunately, this makes assessment of a 12-month simulation from a km-scale model very difficult. For this project, we propose to follow the approach of [Voigt et al. 2013](https://doi.org/10.1175/JCLI-D-12-00132.1) and assess (a) the spatial decorrelation structure of the albedo, and (b) the triviality of a hemispheric albedo symmetry in the km-scale simulation.

**Coordination**: Clare Singer (cesinger23@gmail.com)

#### Sketch of initial activities
* Calculate Δλ and Δφ via autocorrelation of zonal- or meridional-mean reflected SW, as described in [Voigt et al. 2013](https://doi.org/10.1175/JCLI-D-12-00132.1).
* How does Δλ and Δφ from the km-scale model compare to that from CERES observations Δλ=36° and Δφ=10° ([Voigt et al. 2013](https://doi.org/10.1175/JCLI-D-12-00132.1))?
* Divide surface into boxes of size (Δλ, Δφ) and randomly assign to halves to compute reflection from random "hemispheres."
* How trivial is a result of hemispheric symmetry (at various levels, 0.1 W/m2 or 1 W/m2) in the km-scale model? Reproduce Fig 4 from [Voigt et al. 2013](https://doi.org/10.1175/JCLI-D-12-00132.1).
* How does the asymmetry and spatial standard deviation from the km-scale model compare with the CMIP3 models plotted in Fig 6? (CMIP5/6 models could also be added to this comparison.)

---
### Land-Breeze Circulation as Precursor of Organized Convection ([hk25-LBMarConv](https://github.com/digital-earths-global-hackathon/hk25-teams/tree/main/hk25-LBMarConv))

In the tropics, convection plays an important role in modulating large-scale dynamics, being an integral component of the Intertropical Convergence Zone (ITCZ) and the Madden-Julian oscillation (MJO). Convective aggregation (CA) or spontaneous conversion of isolated to aggregated patchy convection is thought to play a role in the evolution of MJO. One of the ingredients required for CA of shallow cloud fields, especially over open ocean, is the presence of mesoscale convergence zones. Land breeze forced by islands within MC that propagate over long distances over the open ocean can provide such forcing that triggers CA.
The main focus of this initiative is to examine the ability of different km-scale models to simulate the initiation of deep convection, triggered by land-breezes and collisions between land breezes, especially in the Maritime Continent MC.

**Coordination**: George Priftis

#### Sketch of initial activities
* Identify initiation of deep convection over the MC (in tandem with other science teams)
* Split in groups of MCSs that are triggered by individual land breezes and those triggered by land breeze collisions
* Quantify the frequency, intensity and horizontal scale of land breezes that trigger MCS initiation
* Evaluate the performance of different models against a global cold pool database derived by Garg et. 2020 (https://agupubs.onlinelibrary.wiley.com/doi/full/10.1029/2019JD031812)

---

### STORMS under Climate Change ([hk25-STORMCC](https://github.com/digital-earths-global-hackathon/hk25-teams/tree/main/hk25-STORMCC))

Kilometer-scale climate models offer new opportunities to better understand drivers
of near-surface winds and their effects under both present-day climate condition and
in a warmer world. For the hackathon, our team will explore near-surface wind
statistics from (3-)hourly output of the new climate model simulations. Obtained
results for the present-day climatology of the winds will be compared against other
data sets, e.g., ERA5 reanalysis. StormCC will also use the new climate model output
to investigate the changes in the distributions of (3-)hourly near-surface winds
with warming. A comparison will be made against output from experiments with
coarser-resolution climate models as used in CMIP. Characteristics of near-surface
winds for different seasons and times of day will be assessed and related to the
classical understanding of processes in atmospheric dynamics. Such processes can be
addressed with hourly data in near-surface winds and will be studied in regional
domains of interest, e.g., Northern Africa for the link of winds to dust emission or
storm track regions for changes in peak winds associated with cyclones. 

**Coordination**: Sreedev Sreekumar

#### Sketch of initial activities
- Compute the surface wind climatology from kilometer-scale climate model output
over global and regional domains.
- Assess the global dust uplift potential based on surface wind characteristics.
- Analyze the diurnal cycle of winds in regions of interest
- Compare model results with other datasets such as observations, reanalysis and
CMIP.

---

### Km-scale representation of aerosol transport and interaction with radiation and clouds ([hk25-Aerosols](https://github.com/digital-earths-global-hackathon/hk25-teams/tree/main/hk25-Aerosols))

This science team will assess the representation of aerosol transport and interaction with radiation and clouds. The team will analyze a year-long, km-scale simulation with interactive aerosols. The aerosols are represented with four modes with prescribed sizes and compositions, i.e., dust, sea salt, carbonaceous aerosol, and sulfuric aerosol. The four modes are transported through the atmosphere and are coupled with various processes such as radiation, convection, and precipitation [(Weiss et al. 2024)](https://egusphere.copernicus.org/preprints/2024/egusphere-2024-3325/).

**Coordination**: Philipp Weiss (philipp.weiss@physics.ox.ac.uk)

#### Sketch of initial activities

* Examine the annual cycle of dust emissions driven by moist convection
* Examine the transport of dust, smoke, and moisture in the West-African monsoon region
* Examine the representation of the Asian Tropopause Aerosol Layer and long-range transport of pollutants from the Indo-Gangetic Plain
* Examine the small-scale transport of boreal fire smoke in the Arctic region
* Examine the influence of aerosols on the organisation of mesoscale convective systems

---
### High Cloud Top Temperatures ([hk25-HighCloudT](https://github.com/digital-earths-global-hackathon/hk25-teams/tree/main/hk25-HighCloudT))

Because of their altitude, convective high clouds dominate outgoing longwave radiation (OLR) by setting the emission temperature, such that $OLR \approx \sigma T_{hc}^4$, with $T_{hc}$ the high cloud top temperature. This expression, combined with the theory that high clouds worldwide have a characteristic emission temperature that remains unchanging with surface warming (the Fixed Anvil Temperature hypothesis; Hartmann et al., 2002; Thompson et al., 2017), suggests that constraining $T_{hc}$ can lead to better estimates of the longwave high cloud feedback parameter and thus climate sensitivity.

In this group, we will examine high cloud top temperatures in storm resolving models. We will identify gridcells fully spanned by high clouds and invert the allsky OLR for emission temperature, then construct latitudinally-resolved temperature distributions. Using these distributions, we can test the effectiveness of simple expressions in capturing the high cloud radiative effect (e.g., Corti and Peter, 2009; Jeevanjee 2023; Deutloff et al., 2025) and, assuming they are unchanging with warming, work towards deriving the longwave cloud feedback parameter.

**Coordination:** Paulina Czarnecki (pc2943@columbia.edu)

#### Sketch of Initial Activities
- Identify high cloud top temperatures (in the simplest case, by inverting $\sigma T^4 = OLR_{allsky}$ in gridcells where cloud area fraction $f = 1$ and ice content $> 10^{-1}$ kg m<sup>2</sup>)
- Plot and analyze distributions in space and time
- Compare between models, observations, +4K simulations.

---

### Convective organization and Thermodynamic-convection coupling ([hk25-Convorg](https://github.com/digital-earths-global-hackathon/hk25-teams/tree/main/hk25-Convorg))

Convective organization is one of important features especially in the tropics over a wide range of spatio-temporal scales. Organized convection interacts with meso-to-synoptic-scale environments and is coupled to large-scale circulations, affecting both weather and climate across the globe. Although global km-scale climate models can represent convective processes more explicitly than conventional climate models, they are expected to struggle with the realistic simulation of convective organization and associated thermodynamic-convection coupling because of unresolved or underresolved processes even with km-scale grid spacing (e.g., microphysics and turbulent mixing).

In this team, we compare the characteristics of mesoscale organized convection, thermodynamic evolution in the life cycle of deep convection, and related weather/climate phenomena simulated in many global storm-resolving models, which have different physics configurations. We also aim at providing helpful insights about the km-scale model development.

**Coordination**: Daisuke Takasuka (takasuka@tohoku.ac.jp)

#### Sketch of initial activities:

+ Quantify precipitation characteristics such as intensity, size, and duration
+ Analyze the thermodynamic evolution associated with deep convection (e.g., buoyancy variations and their decomposition in terms of q and T)
+ Examine the reproducibility of several convection-related phenomena (e.g., tropical waves, MJO, precipitation diurnal cycle)

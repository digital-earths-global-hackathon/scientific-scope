# Model Name: CAS-ESM-IAP AGCM
Team Name : Chinese Academy of Sciences Earth System Model
Model Link: 


## Model description: 
As the atmospheric component of the CAS Earth System model (CAS-ESM), the IAP AGCM has been developed at IAP since 1980s. It is a global grid point model using finite‐difference scheme with a terrain‐following σ coordinate (Zhang et al., 2013). The description of physical parameterizations can be found in Zhang et al. (2020). It is coupled to the land model CoLM (Dai et al., 2003) for the global hackathon simulations.

Dai, Y., Zeng, X., Dickinson, R. E., Baker, I., Bonan, G. B., Bosilovich, M. G., et al., 2003. The Common Land Model (CLM). Bulletin of the American Meteorological Society, 84, 1013–1023. https://doi.org/10.1175/BAMS‐84‐8‐1013
Zhang, H., M. Zhang, and Q. Zeng, 2013. Sensitivity of simulated climate to two atmospheric models: Interpretation of differences between dry models and moist models. Mon. Wea. Rev., 141, 1558-1576.
Zhang, H., Zhang, M., Jin, J., Fei, K., Ji, D., Wu, C., et al., 2020. Description and climate simulation performance of CAS-ESM version 2. Journal of Advances in Modeling Earth Systems, 12, e2020MS002210. https://doi.org/10.1029/2020MS002210.

### Contact:
- [He Zhang](mailto:zhanghe@mail.iap.ac.cn), [Kece Fei](mailto:feikece@mail.iap.ac.cn)

## Simulation Details

Simulation DOI: 
1.	10 km global simulation with deep convection parameterization (Available for Beijing node only)
2.	10 km global simulation without deep convection parameterization
3.	5 km global simulation without deep convection parameterization (Integration in progress; only 4 months data available for Beijing node)

- Resolution: 
o	Horizontal: 10km and 5km global
o	Vertical: 35 levels
o	model top of 35km

- Initialization:
o	Atmosphere: interpolated from IFS on 2020-01-20
o	Land: from an off-line land simulation on 20th Jan 2020 with the forcing of ERA5 reanalysis data and MSWEP precipitation data (The off-line simulation started on 1st Jan 2018)

- Simulation Period: 
o	Model simulations run from 20th Jan 2020 to end Feb 2021. Production data available from 01 Mar 2020 to 28 Feb 2021 (01 Mar 2020 to 30 Jun 2020 for 5km simulation).
## Data notes

# Model Name: ARP-GEM2
Team Name: CNRM (Centre National de Recherches Meteorologiques, Meteo-France / CNRS, Toulouse, France)
Model Link: ---


## Model description:

The ARP-GEM (Global, Efficient and Multiscale version of ARPEGE/IFS) global atmosphere model incorporates a series of efficiency-oriented improvements alongside state-of-the-art physical parameterizations, including shallow and deep convection, with its first version ARP-GEM1 described in detail in Geoffroy and Saint-Martin (2025). The km scale simulations are performed with ARP-GEM2 that will be described in a upcoming paper (Geoffroy and Saint-Martin, in preparation).

**Key References:**

- Geoffroy, O., and D. Saint-Martin, 2025: The ARP-GEM1 Global Atmosphere Model: Description, Speedup Analysis and Multiscale Evaluation up to 6 km, *accepted for Journal of Climate.*

Available Preprints:
- Saint-Martin, D., and O. Geoffroy, 2024: The ARP-GEM1 Global Atmosphere Model. Part I: Description and Speed-up Analysis. [arxiv](https://arxiv.org/abs/2409.19083)

- Geoffroy, O., and D. Saint-Martin, 2024: The ARP-GEM1 Global Atmosphere Model. Part II: Multiscale Evaluation up to 6 km. [arxiv](https://arxiv.org/abs/2409.19089)


### Contact:
- Olivier Geoffroy (olivier.geoffroy@meteo.fr)
- David Saint-Martin (david.saint-martin@meteo.fr)



## Simulation Details

The simulation setup and output variables follow the Takasuka et al. (2024) protocol.
Simulation period : 2020-01-01 to 2021-02-28 (with spinup before 2020-01-01).
Two simulations are performed :
1.	ARPGEM2_2p6km, 2.6 km horizontal resolution (TCo3839)
2.	ARPGEM2_1p3km, 1.3 km horizontal resolution (TCo7679)

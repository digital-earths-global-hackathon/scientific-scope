# Model Name: Model for Prediction Across Scales (MPAS)
- Team Name :  MPAS Team (NCAR)
- Model Link: https://www.mmm.ucar.edu/models/mpas


## Model description
The atmospheric component of MPAS uses an unstructured centroidal Voronoi mesh (grid, or tessellation) and C-grid staggering of the state variables as the basis for the horizontal discretization in the fluid-flow solver. The unstructured variable resolution meshes can be generated having smoothly-varying mesh transitions, which ameliorates many issues associated with the traditional mesh refinement strategy of one-way and two-way grid nesting where the transitions are abrupt. The flexibility of the MPAS meshes allows for applications in high-resolution numerical weather prediction (NWP) and regional climate, in addition to global uniform-resolution NWP and climate applications.

- https://ncar.ucar.edu/what-we-offer/models/model-prediction-across-scales-mpas
- https://www2.mmm.ucar.edu/projects/mpas/site/index.html
- Skamarock, W. C., J. B. Klemp, M. G. Duda, L. D. Fowler, S. Park, and T. D. Ringler, 2012: A Multiscale Nonhydrostatic Atmospheric Model Using Centroidal Voronoi Tesselations and C-Grid Staggering. Mon. Wea. Rev., 140, 3090–3105, https://doi.org/10.1175/MWR-D-11-00215.1. 


### Contact:
- [Bill Skamarock](mailto:skamaroc@ucar.edu)
- [Falko Judt](mailto:fjudt@ucar.edu)
- [Brian Medeiros](mailto:brianpm@ucar.edu ) 


## Simulation Details

- Stevens, Bjorn, Masaki Satoh, Ludovic Auger, Joachim Biercamp, Christopher S. Bretherton, Xi Chen, Peter Düben, et al. 2019. “DYAMOND: The DYnamics of the Atmospheric General Circulation Modeled On Non-Hydrostatic Domains.” Progress in Earth and Planetary Science 6 (1): 61. https://doi.org/10.1186/s40645-019-0304-z

- Resolution: 3.75km

## Data notes

### DYAMOND1
The hackathon data is derived from files: `/glade/campaign/mmm/wmr/fjudt/projects/dyamond_1/3.75km/history.2016-0*`

The data is interpolated to the HEALPix grid at “zoom level” 10 using Delaunay triangulation, and then coarsened by averaging for lower zoom levels.

### DYAMOND2
The hackathon data is derived from files: `/glade/campaign/mmm/wmr/fjudt/projects/dyamond_2/3.75km/history.2020-0*`

The data is interpolated to the HEALPix grid at “zoom level” 10 using Delaunay triangulation, and then coarsened by averaging for lower zoom levels.

### DYAMOND3
The simulation is only the partial DYAMOND3 period.
Files are derived from `/glade/campaign/mmm/wmr/skamaroc/NSC_2023/3.75km_simulation_output_old_transport`

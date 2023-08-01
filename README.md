# ArcticMHWs
Data and code for MHWs in the Arctic project.

The heat budget calculation is done using the model outputs; the tiling of the domain is also part of the pre-processing. We only provide post-processed data, as the model outputs are too heavy to be shared through github.
## Data
We provide tiled data:
  * `ClimThreshSmooth_MLT_Tiled3O.nc` : Climatology and threshold used to detect MHWs, calculated using the MHW algorithm from the Hobday et al. 2016 paper
  * `MHWfiltMean0.1_DetectionProperties_TiledMLT.nc` : Metrics, dates etc. for the MHWs detected over the Arctic tiled domain
  * `Forc_tiles_3Oceans.nc` : Surface heat fluxes (forcing) data, tiled
  * `MLD_tiles_3Oceans.nc` : Mixed layer depth
  * `HeatBudgetMixLayer_Tiles_20142021_JGRo.nc` : Heat budget terms for the surface mixed layer. Main outputs of the heat budget calculation
  * `MLSalt_tiles_3Oceans.nc` : Mixed layer salinity
  * `IceProp_tiles_3Oceans.nc` : Ice properties (concentration, freezing-melting flux...)
  * `MLT_tiles_3Oceans.nc` : Mixed layer temperature
  * `IntegratedHBTerms_forMHWAttribution.nc` : Heat budget terms integrated over the onset and decay of all detected MHWs. 
  * `TilesMHWAnalysis_3Oceans_over300.nc` : Tile numbers to split the whole NAPA domain. Not necessary here...

## Src
On top of that, we also provide the scripts used to aggregate the Heat Budget terms, plot them, analyse them, compare MHWs to ice melting or freezing, do the reynolds decomposition, and look at spatio-temporal variability of MHWs and of drivers:
* `Analyse_IceMHWsrelations_Tiles_v1.ipynb`: Look at co-occurrence of MHWs and freezing and/or melting, and changes in primary drivers.
* `DecomposeRey_FoverH_tiles_v1.ipynb` : Do the Reynolds decomposition of the surface heat flux and investigate the impact of ice melt-induced shoaling on MHW duration and intensity.
* `Analyse_MHWDrivers_Tiles_v1.ipynb` : Main script. Rank the processes driving MHWs during onset and decay, look at specific cases and overall pictures, and spatio-temporal variability
* `FreezingPointTrend_Tiles_v1.ipynb` : Look at the increasing trend of the freezing point and relate it to mixed layer temperature, to see if that could explain the detection of long-lasting MHWs in the winter.

Those data and scripts are at the heart of the Richaud et al. manuscript (submitted to JGR Oceans in August 2023).

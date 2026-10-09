## Data description

Environmental and biogeochemical data for the **global ocean bottom layer** were extracted from simulations of the **EC Earth System Model**.

Data were retained on the native curvilinear EC-Earth ocean grid, without 
spatial interpolation. The ocean components of the EC-Earth models use the NEMO ocean model
on the ORCA1 native curvilinear grid, with an approximate horizontal
resolution of 1°. Because the grid is
curvilinear, the exact horizontal resolution varies spatially. The
extracted data were retained on this native model grid without
spatial interpolation.

### Historical data

Historical environmental conditions were obtained from the **EC-Earth3-ESM-1** model under the `esm-hist` experiment calculated as the mean and standard deviation of three ensemble members (`r1i1p1f1`, `r2i1p1f1`, `r3i1p1f1`). Model output was extracted from the BSC EC-Earth archive for the period **1975–2014**.

Monthly variables were retained at their original temporal resolution, resulting in **480 monthly time steps** over the 40-year historical period. 

The historical dataset comprises the following environmental and biogeochemical variables:

- `chldiatos`: chlorophyll associated with diatoms
- `chlmiscos`: chlorophyll associated with other or miscellaneous phytoplankton
- `co3satcalc`: calcite carbonate saturation-related product
- `dfe`: dissolved iron
- `dissic`: dissolved inorganic carbon
- `epcalc100`: calcite export at 100 m
- `expc`: particulate organic carbon export
- `no3`: nitrate
- `o2`: dissolved oxygen
- `ph`: seawater pH
- `phyc`: phytoplankton carbon
- `po4`: phosphate
- `si`: silicate
- `so`: seawater salinity
- `talk`: total alkalinity
- `thetao`: seawater potential temperature

For variables represented throughout the water column, processed historical products contain **bottom-layer conditions**. Variables intrinsically defined at a particular depth or without a vertical dimension were retained according to their model definition.


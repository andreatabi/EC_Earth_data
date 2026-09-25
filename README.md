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

### Future projections

Future environmental conditions were obtained from **EC-Earth3-CC ScenarioMIP** simulations for ensemble member `r1i1p1f1`. Two future forcing scenarios were considered: **SSP2-4.5** (`ssp245`), representing an intermediate forcing pathway, and **SSP5-8.5** (`ssp585`), representing a very high forcing pathway. The corresponding BSC EC-Earth experiments were `a368` for SSP2-4.5 and `a2zo` for SSP5-8.5.

For each scenario, environmental conditions were extracted for two target years, **2050** and **2100**, resulting in four scenario–year combinations:

| Model | Scenario | Year | Ensemble member |
|---|---|---:|---|
| EC-Earth3-CC | SSP2-4.5 | 2050 | `r1i1p1f1` |
| EC-Earth3-CC | SSP2-4.5 | 2100 | `r1i1p1f1` |
| EC-Earth3-CC | SSP5-8.5 | 2050 | `r1i1p1f1` |
| EC-Earth3-CC | SSP5-8.5 | 2100 | `r1i1p1f1` |

The future dataset currently contains 13 variables:

- `dfe`
- `dissic`
- `epcalc100`
- `expc`
- `no3`
- `o2`
- `ph`
- `phyc`
- `po4`
- `si`
- `so`
- `talk`
- `thetao`

Nine variables (`dfe`, `dissic`, `epcalc100`, `expc`, `no3`, `phyc`, `si`, `so`, and `thetao`) were available as monthly ocean output (`Omon`). All 12 monthly values were retained for each target year; no annual or seasonal temporal averaging was applied.

Four variables (`o2`, `ph`, `po4`, and `talk`) were available as annual ocean output (`Oyr`). These variables therefore contain one model time step for each target year. No additional temporal averaging was performed during extraction.

For variables containing a vertical `lev` dimension, **bottom conditions** were defined as the deepest valid wet model cell at each horizontal grid location. The deepest valid cell was identified independently for each location, thereby accounting for spatial variation in model bathymetry across the CCZ+10 domain. No vertical averaging was performed. Variables without a vertical dimension were retained according to their native model definition.


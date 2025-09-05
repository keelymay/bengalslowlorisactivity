# Impact of seasonality on Bengal slow loris (_Nycticebus bengalensis_) activity. 

This repo contains the code and data repository for the manuscript Maynard et al (2025) Impact of seasonality on Bengal slow loris (_Nycticebus bengalensis_) activity.

## Contents

### Analyses
Full workflow for each analysis, including figures. 
- **activityandclimatemodelanalysis.Rmd** 
- **verticalheightandclimateanalysis.Rmd** 
  
### Data
Analysis-ready data files are split between each of the seasons and are found in zipped folders in 'data\':
- dry_data.7z (contains dry_data.csv and dry_data_height.csv)
- hot_data.7z (contains hot_data.csv and hot_data_height.csv)
- wet_data.7z (contains wet_data.csv and wet_data_height.csv)
  
The CSVs already include:
- `beh2` (behavior; reference = resting `"re"`)
- `id` (individual)
- Zone IDs at 100/200/300 m (e.g., `zoneid_100m`, `zoneid_200m`, `zoneid_300m`; in hot season files: `zone_id_100`, `zone_id_200m`, `zone_id_300`)
- `temp_c`, `Rh_c` (centered predictors)
- `temp_Rh_c` (temperature × humidity)
- `animal_height.m.` (meters)
- `time_minutes` (minutes since 19:00)

> Preprocessing (e.g., spatial fishnet assignment, centering, interaction creation) happened upstream; these Rmds begin from the analysis-ready CSVs.

### Outputs
Saved model runs are stored in 'model\'.

## Requirements
R ≥ 4.2 recommended

## Reproducibility notes

- The `.Rmd` files document the full analysis steps used to generate the figures/tables.  
- Heavy Bayesian model fitting can be time-consuming and environment-specific; therefore, **we do not ask readers to run or knit the Rmds**.  
- If you choose to reproduce results, you will need an R/Stan toolchain and the packages listed below.

**Packages used (reference only):**
`tidyverse`, `lubridate`, `stringr`, `ggplot2`, `patchwork`,  
`brms`, `loo`, `bayestestR`, `posterior`, `bayesplot`,  
`tidybayes`, `cowplot`, `ggtext`, `tidyr`, `dplyr`

### License

Code: MIT

Data: CC BY 4.0 

### Citation

Please cite the associated manuscript when using this repository.

### Contact

Maintainer: Keely Maynard — keelymay@buffalo.edu

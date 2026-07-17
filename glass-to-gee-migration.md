# Appears to GEE Data Source Migration

The comparison CSV is shared in the
[Google Drive data release folder](https://drive.google.com/drive/folders/1zF_Itljwn0bUWSTHEkwkMDyNOiKPXRF1).

## Driver Decision Table

`On GEE (Exact Match)?` is `Yes` only when an exact Appears source match exists on GEE.

For the current GEE workflow, source products may be daily, annual, or static. The first workflow outputs should be monthly and annual summaries only. Daily or weekly exports can be added later from the same daily products if we need higher temporal resolution for a specific analysis.

| Driver | On GEE (Exact Match)? | Preferred GEE Dataset | Same Database as Appears Source? | Appears Spatial Res | Appears Temporal Res | Appears Data Type | Selected GEE Spatial Res | Source Temporal Res | Workflow Output Timing | Selected GEE Data Type | Key Differences |
|---|---|---|---|---|---|---|---|---|---|---|---|
| Elevation | No | `USGS/SRTMGL1_003` | No | 30 arc-sec (~1 km) | Static | Continuous raster (elevation m) | 30 m | Static | Static watershed summary | Continuous raster (elevation m) | Different elevation product than the old workflow and finer selected spatial resolution |
| Land Cover | No | `projects/sat-io/open-datasets/GLC-FCS30D/annual` | No | 1 km (GLCC) | Static (single epoch) | Categorical raster classes | 30 m | Annual (1985-2022) | Annual | Categorical raster classes | Major change: static GLCC to dynamic GLC_FCS30D; class schemes differ |
| NPP | Yes | `MODIS/061/MOD17A3HGF` | Yes | 500 m | Annual | Continuous raster (gC m-2 yr-1) | 500 m | Annual | Annual | Continuous raster (gC m-2 yr-1) | Keep MODIS; no clearly better ready-to-use global GEE replacement identified |
| Evapotranspiration | No | `ECMWF/ERA5_LAND/DAILY_AGGR` (`total_evaporation_sum`) | No | 500 m | 8-day composite | Continuous raster (ET flux) | 0.1 deg (~11.1 km) | Daily | Monthly and annual | Continuous raster (reanalysis ET flux) | Selected product changes to ERA5-Land daily: coarser spatial resolution than MODIS ET, but finer temporal resolution and same source family as other climate variables |
| Air Temperature | No | `ECMWF/ERA5_LAND/DAILY_AGGR` (`temperature_2m`) | No | Unknown old workflow NetCDF source | Monthly | Continuous raster (temperature) | 0.1 deg (~11.1 km) | Daily | Monthly and annual | Continuous raster (2 m temperature reanalysis) | Source and timing shift to ERA5-Land daily |
| Precipitation | No | `ECMWF/ERA5_LAND/DAILY_AGGR` (`total_precipitation_sum`) | No | 2.5 deg (~278 km, GPCP) | Monthly | Continuous raster (precipitation) | 0.1 deg (~11.1 km) | Daily | Monthly and annual | Continuous raster (reanalysis precipitation) | Much finer spatial and temporal scale than GPCP |
| Snow Cover | No | `ECMWF/ERA5_LAND/DAILY_AGGR` (`snow_cover`) | No | 500 m | 8-day composite | Continuous raster (snow cover fraction/percent) | 0.1 deg (~11.1 km) | Daily | Monthly and annual | Continuous raster (reanalysis snow cover fraction) | MODIS observation-based snow to ERA5-Land reanalysis; coarser spatial resolution but daily source data |
| Greenup day | Yes | `MODIS/061/MCD12Q2` | Yes | 500 m | Annual | Integer raster (day-of-year phenology metric) | 500 m | Annual | Annual | Integer raster (day-of-year phenology metric) | Keep MODIS; higher-resolution HLS/Sentinel phenology would require a separate custom workflow |
| Permafrost | No | Upload `perprob.tif` as EE image asset | Yes (if uploaded) | ~1 km (source grid) | Static | Continuous raster (permafrost probability) | Same as uploaded source | Static | Static watershed summary | Continuous raster (permafrost probability) | Add as static context layer if the source raster is uploaded; no clean public GEE replacement identified |
| Soil Class (optional) | No | `OpenLandMap/SOL/SOL_GRTGROUP_USDA-SOILTAX_C/v01` | No | 250 m | Static | Categorical raster (USDA suborder classes) | 250 m | Static | Static watershed class fractions | Categorical soil taxonomy classes | Optional only; old soil-order output has not been very useful |
| Lithology | No | Upload selected lithology product as an EE asset; use GFV/HydroATLAS only as comparison layers | No | 0.5 deg (~50 km) | Static | Categorical raster (lithology classes) | To be confirmed | Static | Static watershed class fractions | Categorical lithology classes | Main workflow should use the exact chosen lithology source if possible; public GEE alternatives are not clearly equivalent |

## Current Output Timing

- Monthly and annual: precipitation, air temperature, evapotranspiration, snow cover
- Snow output: use ERA5-Land `snow_cover`; do not create `snow_num_days` for the GEE workflow
- Annual: land cover, NPP, greenup day
- Static watershed summaries: elevation, permafrost, soil class, lithology
- Later possible extension: daily or weekly outputs from ERA5-Land for climate, ET, and snow, if a specific analysis needs finer timing

## Land-Cover Product

Selected LULC product:
- `projects/sat-io/open-datasets/GLC-FCS30D/annual`
- 30 m annual land cover
- Listed in the GEE Community Catalog as 1985-2022
- Used for the June 2026 corrected GEE/GLC LULC update

No other LULC product is currently selected for this workflow.

Other products that could be used only for comparison checks:
- Dynamic World V1: 10 m, 2015-present, but class probabilities and near-real-time labels may need extra smoothing/aggregation
- ESA WorldCover: 10 m, available for 2020/2021, useful for checks but not a long annual time series

## NCEAS Server Path

Server data location: `/home/shares/lter-si/si-watershed-extract/`

## References

- Appears article: https://www.nature.com/articles/s41597-025-05937-2
- ERA5-Land daily in GEE: https://developers.google.com/earth-engine/datasets/catalog/ECMWF_ERA5_LAND_DAILY_AGGR
- ERA5-Land monthly in GEE: https://developers.google.com/earth-engine/datasets/catalog/ECMWF_ERA5_LAND_MONTHLY_AGGR
- Dynamic World V1 in GEE: https://developers.google.com/earth-engine/datasets/catalog/GOOGLE_DYNAMICWORLD_V1
- ESA WorldCover in GEE: https://developers.google.com/earth-engine/datasets/catalog/ESA_WorldCover_v200
- GLC_FCS30D in GEE Community Catalog: https://gee-community-catalog.org/projects/glc_fcs/

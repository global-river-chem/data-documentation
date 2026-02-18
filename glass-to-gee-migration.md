# GlASS to GEE Data Source Migration

## Driver Decision Table

`On GEE (Exact Match)?` is `Yes` only when an exact GlASS source match exists on GEE.

| Driver | On GEE (Exact Match)? | Preferred GEE Dataset | Same Database as GlASS Source? | GlASS Spatial Res | GlASS Temporal Res | GlASS Data Type | Selected GEE Spatial Res | Selected GEE Temporal Res | Selected GEE Data Type | Key Differences |
|---|---|---|---|---|---|---|---|---|---|---|
| Elevation | No | `USGS/SRTMGL1_003` | No | 30 arc-sec (~1 km) | Static | Continuous raster (elevation m) | 30 m | Static | Continuous raster (elevation m) | Different product lineage (WorldClim-processed SRTM vs SRTM GEE) and finer selected spatial resolution |
| Land Cover | No | `projects/sat-io/open-datasets/GLC-FCS30D/annual` | No | 1 km (GLCC) | Static (single epoch) | Categorical raster classes | 30 m | Annual (1985-2022) | Categorical raster classes | Major change: static GLCC to dynamic GLC_FCS30D; class schemes differ |
| NPP | Yes | `MODIS/061/MOD17A3HGF` | Yes | 500 m | Annual | Continuous raster (gC m-2 yr-1) | 500 m | Annual | Continuous raster (gC m-2 yr-1) | None (exact MODIS match) |
| Evapotranspiration | Yes | `ECMWF/ERA5_LAND/DAILY_AGGR` (`total_evaporation_sum`) | No | 500 m | 8-day composite | Continuous raster (ET flux) | 0.1 deg (~11.1 km) | Daily | Continuous raster (reanalysis ET flux) | Exact MODIS source exists on GEE, but operational selection changes to ERA5-Land daily (coarser spatial, finer temporal) |
| Air Temperature | No | `ECMWF/ERA5_LAND/DAILY_AGGR` (`temperature_2m*`) | No | Unknown (workflow NetCDF source not fully resolved) | Monthly | Continuous raster (temperature) | 0.1 deg (~11.1 km) | Daily | Continuous raster (2 m temperature reanalysis) | Source and cadence shift to ERA5-Land daily |
| Precipitation | No | `ECMWF/ERA5_LAND/DAILY_AGGR` (`total_precipitation_sum`) | No | 2.5 deg (~278 km, GPCP) | Monthly | Continuous raster (precipitation) | 0.1 deg (~11.1 km) | Daily | Continuous raster (reanalysis precipitation) | Much finer spatial/temporal scale and source shift (GPCP to ERA5-Land) |
| Snow Fraction | No | `ECMWF/ERA5_LAND/DAILY_AGGR` (`snow_cover*`) | No | 500 m | 8-day composite | Continuous raster (snow cover fraction/percent) | 0.1 deg (~11.1 km) | Daily | Continuous raster (reanalysis snow cover fraction) | MODIS observation-based snow to ERA5-Land reanalysis; coarser spatial, finer temporal |
| Greenup day | Yes | `MODIS/061/MCD12Q2` | Yes | 500 m | Annual | Integer raster (day-of-year phenology metric) | 500 m | Annual | Integer raster (day-of-year phenology metric) | None (exact MODIS match) |
| Permafrost | No | Upload `perprob.tif` as EE image asset | Yes (if uploaded) | ~1 km (source grid) | Static | Continuous raster (permafrost probability) | Same as uploaded source | Static | Continuous raster (permafrost probability) | No difference if original source is uploaded; no exact public GEE equivalent |
| Soil Order | No | OpenLandMap soil class products (similar, not exact) | No | 250 m | Static | Categorical raster (USDA suborder classes) | ~250 m (OpenLandMap typical) | Static | Categorical/probabilistic soil classes | Similar scale but taxonomy/schema not exact |
| Lithology | No | `projects/sat-io/open-datasets/GLiM` | Unknown (likely, not confirmed) | 0.5 deg (~50 km) | Static | Categorical raster (lithology classes) | ~0.5 deg (~50 km, expected) | Static | Categorical raster (lithology classes) | Likely similar source/grid, but exact source identity not fully confirmed |

## NCEAS Server Path

Server data location: `/home/shares/lter-si/si-watershed-extract/`

## References

- GlASS article: https://www.nature.com/articles/s41597-025-05937-2
- ERA5-Land daily in GEE: https://developers.google.com/earth-engine/datasets/catalog/ECMWF_ERA5_LAND_DAILY_AGGR
- ERA5-Land monthly in GEE: https://developers.google.com/earth-engine/datasets/catalog/ECMWF_ERA5_LAND_MONTHLY_AGGR

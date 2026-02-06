# Aurora to GEE Data Source Migration

Comparison of raster data sources between the legacy Aurora/AppEEARS workflow and the new Google Earth Engine workflow.

## Raster Data Equivalents

| Variable | Aurora Source | GEE Equivalent | Notes |
|----------|---------------|----------------|-------|
| Elevation | `raw-elevation/` (SRTM) | `USGS/SRTMGL1_003` | Same source, should match |
| Land Cover | `raw-glcc-landcover-data/` (GLCC) | `MODIS/061/MCD12Q1` | **DIFFERENT** - Aurora uses GLCC, GEE has MODIS. This is OK because we use GEE in GlASS |
| NPP | `raw-npp-v061/` (MODIS MOD17A3) | `MODIS/061/MOD17A3HGF` | Same product, v061 |
| Evapotranspiration | `raw-evapo-modis16a2-v061/` | `MODIS/061/MOD16A2` | Same product, v061 |
| Air Temperature | `raw-airtemp-monthly/` | `ECMWF/ERA5_LAND/MONTHLY_AGGR` | Switching to ERA5-Land for monthly analysis capability |
| Precipitation | `raw-gpcp-precip/` (GPCP) | `ECMWF/ERA5_LAND/MONTHLY_AGGR` | Switching to ERA5-Land for consistency (monthly analysis) |
| Snow Fraction | `raw-snowfrac/` (MODIS MOD10A1) | `MODIS/061/MOD10A1` | Same product |
| Greenup | `raw-greenup-v061/` (MODIS MCD12Q2) | `MODIS/061/MCD12Q2` | Same product, v061 |
| Permafrost | `raw-permafrost/` | TBD | Need to identify GEE equivalent |
| Soil | `raw-soil/` | `OpenLandMap/SOL/SOL_*` | **VERIFY** - check if same source |
| Lithology | `raw-lithology-data/` (GLiM) | `projects/sat-io/open-datasets/GLiM` | Same source (community upload) |

## Aurora Server Path

Legacy data location: `/home/shares/lter-si/si-watershed-extract/`

## To Do

- [ ] Verify air temperature source matches
- [ ] Document precipitation product difference (GPCP vs ERA5-Land) - may affect comparability
- [ ] Verify soil data source
- [ ] Find/upload permafrost equivalent
- [ ] Test extraction results between old and new workflow for validation

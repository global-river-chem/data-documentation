# Aurora to GEE Data Source Migration

Comparison of raster data sources between the legacy Aurora/AppEEARS workflow and the new Google Earth Engine workflow.

## Raster Data Equivalents

| Variable | Aurora Source | GEE Equivalent | Notes |
|----------|---------------|----------------|-------|
| Permafrost | `raw-permafrost/` | TBD | **need to identify GEE equivalent** |
| Soil | `raw-soil/` | `OpenLandMap/SOL/SOL_*` | **need to verify** - check if same source |
| Land Cover | `raw-glcc-landcover-data/` (GLCC) | `MODIS/061/MCD12Q1` | **different, but we knew this already** - We MODIS for the GlASS data paper |
| Air Temperature | `raw-airtemp-monthly/` | `ECMWF/ERA5_LAND/MONTHLY_AGGR` | Switching to ERA5-Land for monthly analysis capability |
| Precipitation | `raw-gpcp-precip/` (GPCP) | `ECMWF/ERA5_LAND/MONTHLY_AGGR` | Switching to ERA5-Land for consistency (monthly analysis) |
| Elevation | `raw-elevation/` (SRTM) | `USGS/SRTMGL1_003` | Same source, should match |
| Lithology | `raw-lithology-data/` (GLiM) | `projects/sat-io/open-datasets/GLiM` | Same source (community upload) |
|**MODIS Products:** ||||
| NPP | `raw-npp-v061/` (MODIS MOD17A3) | `MODIS/061/MOD17A3HGF` | Same product, v061 |
| Evapotranspiration | `raw-evapo-modis16a2-v061/` | `MODIS/061/MOD16A2` | Same product, v061 |
| Snow Fraction | `raw-snowfrac/` (MODIS MOD10A1) | `MODIS/061/MOD10A1` | Same product |
| Greenup | `raw-greenup-v061/` (MODIS MCD12Q2) | `MODIS/061/MCD12Q2` | Same product, v061 |

**MODIS note:** Can use MODIS in GEE, but need to check these sources in ERA5-Land — MODIS is higher resolution spatially but not temporally

## Aurora Server Path
Legacy data location: `/home/shares/lter-si/si-watershed-extract/`

## To Do

- [ ] Verify air temperature source matches
- [ ] Document precipitation product difference (GPCP vs ERA5-Land) - may affect comparability
- [ ] Verify soil data source
- [ ] Find/upload permafrost equivalent
- [ ] Test extraction results between old and new workflow for validation

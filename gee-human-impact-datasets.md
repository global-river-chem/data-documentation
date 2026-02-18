# Google Earth Engine Human Impact Datasets (GlASS to GEE)

Concise, chemistry-focused inventory of GEE datasets for the migration from **GlASS**-based drivers to GEE extraction.

## Final Recommended Subset (Primary)

| Tier | Dataset | Asset ID | Coverage | Temporal Extent | Nominal Resolution | Scale vs ERA5/MODIS | Relevance to Stream Chemistry/Flow |
|---|---|---|---|---|---|---|---|
| Core (Global) | Global Human Modification | `CSP/HM/GlobalHumanModification` | Global terrestrial | 2016 | 1000 m | Similar to MODIS; much finer than ERA5 | High (composite human pressure) |
| Core (Global) | GHSL Built-up Surface | `JRC/GHSL/P2023A/GHS_BUILT_S` | Global | 1975-2030 (5-year) | 100 m | Much finer than MODIS/ERA5 | High (impervious/urban pressure) |
| Core (Global) | GAIA Impervious Transition Year | `Tsinghua/FROM-GLC/GAIA/v10` | Global | 1985-2018 | 30 m | Much finer than MODIS/ERA5 | High (urban expansion trajectory) |
| Core (Global) | Sentinel-5P NO2 | `COPERNICUS/S5P/OFFL/L3_NO2` | Global | 2018-present | 1113.2 m | Similar to MODIS; finer than ERA5 | High (atmospheric N loading proxy) |
| Core (Global) | Sentinel-5P SO2 | `COPERNICUS/S5P/OFFL/L3_SO2` | Global | 2018-present | 1113.2 m | Similar to MODIS; finer than ERA5 | High (atmospheric S loading proxy) |
| Core (Global) | HydroATLAS Basins L06 | `WWF/HydroATLAS/v1/Basins/level06` | Global | Static | Vector basins | Vector (not directly comparable) | High (basin anthropogenic context) |
| Core (US/NA) | TIGER Roads | `TIGER/2016/Roads` | USA + territories | 2016 | Vector lines | Vector (not directly comparable) | High (road salts, metals, runoff pathways) |

## Secondary Add-ons (Use as Needed)

| Dataset | Asset ID | Why It Can Help |
|---|---|---|
| MTBS Burn Severity Mosaics | `USFS/GTAC/MTBS/annual_burn_severity_mosaics/v1` | Fire disturbance effects on nutrient/sediment export (US) |
| TEMPO NO2 L3 QA | `NASA/TEMPO/NO2_L3_QA` | High-frequency NA atmospheric chemistry proxy |
| Global Power Plant Database | `WRI/GPPD/power_plants` | Point-source industrial/thermal pressure context |
| ERA5-Land Daily (support covariate) | `ECMWF/ERA5_LAND/DAILY_AGGR` | Flow/climate context alongside human-impact terms |

## Full Screened Inventory

All currently screened datasets, with row-level fields for:
- spatial/temporal extent
- nominal resolution
- scale similarity vs ERA5/MODIS
- stream chemistry relevance
- keep tier (`Core`, `Secondary`, `Context-only`, `Support`)

See: `gee-human-impact-datasets-global-join.csv`

## Catalog Scope Note

The developers.google.com list is comprehensive for the **public official catalog**, but not for all usable EE data:
- official catalog datasets
- community datasets
- user/project assets uploaded to EE

---

**Last Updated:** 2026-02-17

## Key Sources

- https://developers.google.com/earth-engine/datasets
- https://developers.google.com/earth-engine/datasets/catalog
- https://developers.google.com/earth-engine/datasets/community

# Google Earth Engine Human Impact Datasets (Appears to GEE)

Concise, chemistry-focused inventory of GEE datasets for the migration from **Appears**-based drivers to GEE extraction.

## Final Recommended Subset (Primary)

| Tier | Dataset | Asset ID | Coverage | Temporal Extent | Nominal Resolution | Scale vs ERA5/MODIS | 
|---|---|---|---|---|---|---|---|
| Core (Global) | Global Human Modification | `CSP/HM/GlobalHumanModification` | Global terrestrial | 2016 | 1000 m | Similar to MODIS; much finer than ERA5 | 
| Core (Global) | GHSL Built-up Surface | `JRC/GHSL/P2023A/GHS_BUILT_S` | Global | 1975-2030 (5-year) | 100 m | Much finer than MODIS/ERA5 | 
| Core (Global) | GAIA Impervious Transition Year | `Tsinghua/FROM-GLC/GAIA/v10` | Global | 1985-2018 | 30 m | Much finer than MODIS/ERA5 | 
| Core (Global) | Sentinel-5P NO2 | `COPERNICUS/S5P/OFFL/L3_NO2` | Global | 2018-present | 1113.2 m | Similar to MODIS; finer than ERA5 |
| Core (Global) | Sentinel-5P SO2 | `COPERNICUS/S5P/OFFL/L3_SO2` | Global | 2018-present | 1113.2 m | Similar to MODIS; finer than ERA5 | 
| Core (Global) | HydroATLAS Basins L06 | `WWF/HydroATLAS/v1/Basins/level06` | Global | Static | Vector basins | Vector (not directly comparable) |
| Core (US/NA) | TIGER Roads | `TIGER/2016/Roads` | USA + territories | 2016 | Vector lines | Vector (not directly comparable) | 

## Secondary Add-ons (Use as Needed)

| Dataset | Asset ID | Notes |
|---|---|---|
| MTBS Burn Severity Mosaics | `USFS/GTAC/MTBS/annual_burn_severity_mosaics/v1` | Fire disturbance (US) |
| TEMPO NO2 L3 QA | `NASA/TEMPO/NO2_L3_QA` | High-frequency N. America atmospheric chemistry proxy |
| Global Power Plant Database | `WRI/GPPD/power_plants` | Point-source industrial/thermal impacts|

Downloadable CSV: [gee-human-impact-datasets-global-join.csv](gee-human-impact-datasets-global-join.csv)

## Catalog Scope Note

The developers.google.com list is comprehensive for the **public official catalog**, but not for all usable EE data. We can import:
- community datasets
- user/project assets uploaded to EE

---

**Last Updated:** 2026-02-17

## Sources

- https://developers.google.com/earth-engine/datasets
- https://developers.google.com/earth-engine/datasets/catalog
- https://developers.google.com/earth-engine/datasets/community

# Google Earth Engine Human Impact Datasets

## Primary Shortlist for First-Pass Global Joins

| Dataset | Public EE availability | Asset ID | Spatial Extent | Temporal Extent | Temporal Resolution | Spatial Resolution | Key Attributes |
|---|---|---|---|---|---|---|---|
| GAIA (Year of Change to Impervious) | Official | `Tsinghua/FROM-GLC/GAIA/v10` | Global | 1985-2018 | Encoded annual transition year | 30 m | Year of impervious transition |
| Global Human Modification v3 | Community | `projects/sat-io/open-datasets/ghm-v3` | Global | 1990-2022 (5-year steps) | 5-year epochs | 300 m and 90 m | Human modification index time series |
| GHSL Built-up Surface | Official | `JRC/GHSL/P2023A/GHS_BUILT_S` | Global | 1975-2030 | 5-year epochs | 100 m | Built-up / impervious surface |
| GHSL Population | Official | `JRC/GHSL/P2023A/GHS_POP` | Global | 1975-2030 | 5-year epochs | 100 m | Population count and density |
| Sentinel-5P OFFL NO2 | Official | `COPERNICUS/S5P/OFFL/L3_NO2` | Global | 2018-present | Near-daily | 1113.2 m | Tropospheric NO2 column |
| Sentinel-5P OFFL SO2 | Official | `COPERNICUS/S5P/OFFL/L3_SO2` | Global | 2018-present | Near-daily | 1113.2 m | SO2 column concentration |
| Global Human Modification (gHM) | Official | `CSP/HM/GlobalHumanModification` | Global terrestrial | 2016 | Single year | 1000 m | Composite modification index |
| NPKGRIDS | Community | `projects/sat-io/open-datasets/NPKGRIDS` | Global | 2015-2020 (circa 2020) | Static snapshot | 0.05 deg (~5.6 km) | N, P2O5, K2O application rates |
| Global Dam Watch (GDW) | Community | `projects/sat-io/open-datasets/GDW/GDW_BARRIERS_V1_0` | Global | Current | Static snapshot | Vector points | Barrier locations and dam attributes |
| HydroATLAS Basins L06 | Official | `WWF/HydroATLAS/v1/Basins/level06` | Global | Static | Static table | Vector basins | Basin anthropogenic covariates |
| TIGER US Census Roads | Official | `TIGER/2016/Roads` | USA + territories | 2016 | Single snapshot | Vector lines | Road network geometry |

## Secondary Add-ons

| Dataset | Public EE availability | Asset ID | Spatial Extent | Temporal Extent | Temporal Resolution | Spatial Resolution | Why It Can Help |
|---|---|---|---|---|---|---|---|
| GHSL Settlement Characteristics | Official | `JRC/GHSL/P2023A/GHS_BUILT_C` | Global | 2018 | Single epoch | 10 m | Detailed settlement texture and built form |
| WorldPop Residential Population | Official | `WorldPop/GP/100m/pop` | Global | 2000-2021 | Annual | 92.77 m | Alternate high-detail population surface |
| GHSL Building Height 2018 | Official | `JRC/GHSL/P2023A/GHS_BUILT_H` | Global | 2018 | Single epoch | 100 m | Urban vertical intensity layer |
| GHSL Building Volume | Official | `JRC/GHSL/P2023A/GHS_BUILT_V` | Global | 1975-2030 | 5-year epochs | 100 m | Non-residential and built-volume context |
| ESA WorldCover v200 | Official | `ESA/WorldCover/v200` | Global | 2021 | Single epoch | 10 m | Fast land-cover support layer for built-up and cropland classes |
| HydroWASTE v1.0 | Community | `projects/sat-io/open-datasets/HydroWaste/HydroWASTE_v10` | Global | 2022 release | Static snapshot | Vector points | Wastewater treatment plant and outfall inventory |
| PEST-CHEMGRIDS | Community | `projects/sat-io/open-datasets/PEST-CHEMGRIDS/application_rates` | Global | 2015-2025 | Multi-epoch | ~10 km (5 arc-min) | Pesticide-pressure complement to fertilizer |
| LandScan Population Data Global 1km | Community | `projects/sat-io/open-datasets/ORNL/LANDSCAN_GLOBAL` | Global | 2000-2023 | Annual | ~1 km (30 arc-sec) | Alternate population baseline with annual updates |
| Global Power | Community | `projects/sat-io/open-datasets/predictive-global-power-system/*` | Global | 2020 release | Static snapshot | 250 m raster plus vector lines | Global grid and transmission infrastructure |
| Oil and Gas Infrastructure Mapping (OGIM) | Community | `projects/sat-io/open-datasets/OGIM/*` | Global | Current (inputs through 2025-02) | Static snapshot | Mixed vector geometries | Oil and gas infrastructure footprint |
| Climate TRACE Global Emissions Data | Community | `projects/sat-io/open-datasets/CLIMATE-TRACE/EMISSIONS/*` | Global | Recent multi-year inventory | Time series / sector-dependent | Mixed vector geometries | Emissions assets across waste, transport, power, and agriculture |
| Global Roads Inventory Project (GRIP4) | Community | `projects/sat-io/open-datasets/GRIP4/[region]` | Global (by region) | Current | Static snapshot | ~8 km density plus vector regional assets | Global road network outside the US |
| GHSL Degree of Urbanization V2-0 | Official | `JRC/GHSL/P2023A/GHS_SMOD_V2-0` | Global | 1975-2030 | 5-year epochs | 1000 m | Settlement class layer for urban/rural splits |
| GISD30 | Community | `projects/sat-io/open-datasets/GISD30_1985_2020` | Global | 1985-2020 | Multi-year time series | 30 m | Additional impervious dynamics product |
| GISA | Community | `projects/sat-io/open-datasets/GISA_1972_2021` | Global | 1972-2021 | Multi-year time series | 30 m | Longest impervious time series screened |
| USDA NASS CDL | Official | `USDA/NASS/CDL` | CONUS | 2008-2024 | Annual | 10 m (2024), 30 m (prior) | Detailed US crop, hay, and pasture classes |
| TIGER Roads Time Series | Community | `projects/sat-io/open-datasets/TIGER/[YEAR]/Roads` | USA + territories | 2009-2025 | Annual | Vector lines | Annual road-network releases rather than a single-year snapshot |
| MTBS Burn Severity Mosaics | Official | `USFS/GTAC/MTBS/annual_burn_severity_mosaics/v1` | CONUS + AK + HI + PR | 1984-2024 | Annual | 30 m | Fire disturbance context for US sites |
| TEMPO NO2 L3 QA | Official | `NASA/TEMPO/NO2_L3_QA` | North America field of regard | 2023-08-01 to 2025-09-16 (catalog) | Hourly / daytime sampling | 2226 m | Higher-frequency North America air-quality proxy |

## Restored Full Inventory

CSV output stored in Box documentation folder:
`/Users/sidneybush/Library/CloudStorage/Box-Box/Sidney_Bush/SiSyn/data_checking/documentation/gee-human-impact-datasets-global-join.csv`

CSV fields: `theme`, `dataset`, `asset_id`, `catalog_type`, `spatial_extent`, `temporal_extent`, `temporal_cadence`, `nominal_resolution`, `scale_similarity_vs_era5_modis`, `stream_chemistry_relevance`, `recommendation`, `global_join_notes`.

`catalog_type` is normalized here to `Official`, `Community`, `Project asset`, or `Not in public EE`.

### Population and Settlement Baselines

| Dataset | Asset ID | Spatial Extent | Temporal Extent | Temporal Resolution | Spatial Resolution | Status / Notes |
|---|---|---|---|---|---|---|
| GHSL Settlement Characteristics | `JRC/GHSL/P2023A/GHS_BUILT_C` | Global | 2018 | Single epoch | 10 m | Official - detailed settlement texture |
| WorldPop Residential Population | `WorldPop/GP/100m/pop` | Global | 2000-2021 | Annual | 92.77 m | Official - high-detail residential population |
| GHSL Built-up Surface (P2023A) | `JRC/GHSL/P2023A/GHS_BUILT_S` | Global | 1975-2030 | 5-year epochs | 100 m | Official - core impervious and urban baseline |
| GHSL Building Height 2018 (P2023A) | `JRC/GHSL/P2023A/GHS_BUILT_H` | Global | 2018 | Single epoch | 100 m | Official - urban vertical intensity |
| GHSL Building Volume (P2023A) | `JRC/GHSL/P2023A/GHS_BUILT_V` | Global | 1975-2030 | 5-year epochs | 100 m | Official - built-volume and non-residential signal |
| GHSL Population (P2023A) | `JRC/GHSL/P2023A/GHS_POP` | Global | 1975-2030 | 5-year epochs | 100 m | Official - core population baseline |
| WorldPop Age/Sex | `WorldPop/GP/100m/pop_age_sex` | Global | 2020-2021 | Annual snapshot | 100 m | Official - demographic structure rather than first-pass chemistry driver |
| GPWv4.11 Population Count | `CIESIN/GPWv411/GPW_Population_Count` | Global | 2000-2020 | 5-year epochs | 927.67 m | Official - stable coarse reference |
| GPWv4.11 Population Density | `CIESIN/GPWv411/GPW_Population_Density` | Global | 2000-2020 | 5-year epochs | 927.67 m | Official - density form of GPW |
| LandScan Population Data Global 1km | `projects/sat-io/open-datasets/ORNL/LANDSCAN_GLOBAL` | Global | 2000-2023 | Annual | ~1 km (30 arc-sec) | Community - alternate annual population baseline |
| GHSL Degree of Urbanization V2-0 | `JRC/GHSL/P2023A/GHS_SMOD_V2-0` | Global | 1975-2030 | 5-year epochs | 1000 m | Official - harmonized settlement class |

### Water Infrastructure and Basin Context

| Dataset | Asset ID | Spatial Extent | Temporal Extent | Temporal Resolution | Spatial Resolution | Status / Notes |
|---|---|---|---|---|---|---|
| HydroWASTE v1.0 | `projects/sat-io/open-datasets/HydroWaste/HydroWASTE_v10` | Global | 2022 release | Static snapshot | Vector points | Community - wastewater treatment plant and outfall inventory |
| Global Dam Watch (GDW) | `projects/sat-io/open-datasets/GDW/GDW_BARRIERS_V1_0` | Global | Current | Static snapshot | Vector points | Community - core comprehensive barrier inventory |
| GOODD Dams | `projects/sat-io/open-datasets/GOODD/GOOD2_dams` | Global | Current | Static snapshot | Vector points | Community - alternate dam source |
| Global Dam Tracker (GDAT) | Community catalog (GDAT) | Global | 1990s-2020s | Event time series / updates | Vector points | Community - useful when commissioning timing matters |
| GDW Reservoirs | `projects/sat-io/open-datasets/GDW/GDW_RESERVOIRS_V1_0` | Global | Current | Static snapshot | Vector polygons | Community - reservoir storage and inundation context |
| GOODD Catchments | `projects/sat-io/open-datasets/GOODD/GOOD2_catchments` | Global | Current | Static snapshot | Vector polygons | Community - dam-specific upstream catchments |
| HydroATLAS Basins L06 | `WWF/HydroATLAS/v1/Basins/level06` | Global | Static | Static table | Vector basins | Official - core basin anthropogenic and environmental covariates |

### Agriculture, Fertilizer, Pesticides, and Grazing

| Dataset | Asset ID | Spatial Extent | Temporal Extent | Temporal Resolution | Spatial Resolution | Status / Notes |
|---|---|---|---|---|---|---|
| ESA WorldCover v200 | `ESA/WorldCover/v200` | Global | 2021 | Single epoch | 10 m | Official - fast land-cover support layer |
| GCEP30 Cropland Extent | `projects/sat-io/open-datasets/gcep30` | Global | ~2015 | Single epoch | 30 m | Community - high-resolution cropland extent |
| LGRIP30 Irrigated/Rainfed | `projects/sat-io/open-datasets/lgrip30` | Global | 2014-2017 (nominal 2015) | Single epoch | 30 m | Community - irrigation split |
| GCI30 Cropping Intensity | `projects/sat-io/open-datasets/gci30` | Global | Recent | Single epoch | 30 m | Community - multi-cropping intensity |
| GLC_FCS30D | `projects/sat-io/open-datasets/GLC-FCS30D/annual` | Global | 1985-2022 (annual from 2000 onward) | Annual / multi-epoch | 30 m | Community - strongest screened global crop-type detail |
| Global Pasture Watch | `global-pasture-watch/*` collections | Global | 2000-2022 | Annual | 30 m | Community - grazing-land context |
| GFSAD1000 Cropland Extent | `USGS/GFSAD1000_V1` | Global | ~2010 (2007-2012 source window) | Single epoch | 1000 m | Official - coarse cropland baseline |
| NPKGRIDS | `projects/sat-io/open-datasets/NPKGRIDS` | Global | 2015-2020 (circa 2020) | Static snapshot | 0.05 deg (~5.6 km) | Community - core fertilizer pressure proxy |
| PEST-CHEMGRIDS | `projects/sat-io/open-datasets/PEST-CHEMGRIDS/application_rates` | Global | 2015-2025 | Multi-epoch | ~10 km (5 arc-min) | Community - pesticide application complement to fertilizer |
| Gridded Livestock of the World (GLW3) | External (FAO/Harvard) | Global | 2010 | Single epoch | ~10 km (5 arc-min) | Not in public EE - manual import required |
| Global Fertilizer by Crop | Community catalog CSV | Global | 2017-2018 period | Periodic summary | Country/crop tables | Community - reference only, not spatially joinable |
| EUCROPMAP | `JRC/D5/EUCROPMAP/V1` | Europe (EU) | 2018, 2022 | Multi-epoch | 10 m | Official - regional crop classification |
| USDA NASS CDL | `USDA/NASS/CDL` | CONUS | 2008-2024 | Annual | 10 m (2024), 30 m (prior) | Official - regional crop, hay, and pasture detail |
| Canada AAFC ACI | `AAFC/ACI` | Canada | 2009-2023 | Annual | 30 m (56 m in 2009-2010) | Official - regional crop and pasture detail |

### Human Modification, Accessibility, and Impervious Change

| Dataset | Asset ID | Spatial Extent | Temporal Extent | Temporal Resolution | Spatial Resolution | Status / Notes |
|---|---|---|---|---|---|---|
| World Settlement Footprint 2015 | `DLR/WSF/WSF2015/v1` | Global | 2014-2015 | Single epoch | 10 m | Official - settlement footprint snapshot |
| World Settlement Footprint 2019 | `projects/sat-io/open-datasets/WSF/WSF_2019` | Global | 2019 | Single epoch | 10 m | Community - updated settlement footprint |
| GAIA (Year of Change to Impervious) | `Tsinghua/FROM-GLC/GAIA/v10` | Global | 1985-2018 | Encoded annual transition year | 30 m | Official - core urban expansion trajectory |
| WSF Evolution | `projects/sat-io/open-datasets/WSF/WSF_EVO` | Global | 1985-2015 | Annual | 30 m | Community - annual settlement change |
| GISD30 | `projects/sat-io/open-datasets/GISD30_1985_2020` | Global | 1985-2020 | Multi-year time series | 30 m | Community - impervious surface dynamics |
| GISA | `projects/sat-io/open-datasets/GISA_1972_2021` | Global | 1972-2021 | Multi-year time series | 30 m | Community - longest impervious time series in the screened set |
| Global Human Modification v3 | `projects/sat-io/open-datasets/ghm-v3` | Global | 1990-2022 (5-year steps) | 5-year epochs | 300 m and 90 m | Community - core time-varying pressure series |
| Global Human Modification (gHM) | `CSP/HM/GlobalHumanModification` | Global terrestrial | 2016 | Single year | 1000 m | Official - core composite pressure index |
| WCS Human Impact Index | `projects/HII/v1/hii` | Global | Time series | Time series | Variable | Project asset - multi-driver impact index |
| Accessibility to Cities 2015 | `Oxford/MAP/accessibility_to_cities_2015_v1_0` | Broad global (-60 to 85 latitude) | 2015 | Single epoch | 927.67 m | Official - travel-time proxy, deprecated |
| NLCD Impervious | `USGS/NLCD_RELEASES/2021_REL/NLCD` | CONUS + Alaska | 2001-2021 (multiple epochs) | Multi-epoch | 30 m | Official - regional percent impervious product |

### Roads, Industry, Mining, and Emissions

| Dataset | Asset ID | Spatial Extent | Temporal Extent | Temporal Resolution | Spatial Resolution | Status / Notes |
|---|---|---|---|---|---|---|
| Oil and Gas Infrastructure Mapping (OGIM) | `projects/sat-io/open-datasets/OGIM/*` | Global | Current (inputs through 2025-02) | Static snapshot | Mixed vector geometries | Community - comprehensive oil and gas infrastructure database |
| Global Mining Footprints | `projects/sat-io/open-datasets/global-mining/global_mining_footprints` | Global | Current | Static snapshot | High-resolution polygons | Community - high-resolution mining extent |
| Global Power Plant Database | `WRI/GPPD/power_plants` | Global | 2018 | Single snapshot | Vector points | Official - industrial and thermal point sources |
| Climate TRACE Global Emissions Data | `projects/sat-io/open-datasets/CLIMATE-TRACE/EMISSIONS/*` | Global | Recent multi-year inventory | Time series / sector-dependent | Mixed vector geometries | Community - emissions assets across transport, fertilizer, wastewater, waste, and power |
| Global Mining Areas | `projects/sat-io/open-datasets/global-mining/global_mining_polygons` | Global | 2000-2017 | Static inventory | Vector polygons | Community - mining type and area |
| Global Power | `projects/sat-io/open-datasets/predictive-global-power-system/*` | Global | 2020 release | Static snapshot | 250 m raster plus vector lines | Community - predicted global power grid infrastructure |
| Global Roads Inventory Project (GRIP4) | `projects/sat-io/open-datasets/GRIP4/[region]` | Global (by region) | Current | Static snapshot | ~8 km density plus vector regional assets | Community - global road network through regional assets |
| Microsoft Bing Global Mined Roads | Community catalog | Global | 2020-2022 | Recent snapshot | Vector | Community - AI-extracted road segments from imagery |
| TIGER Roads Time Series | `projects/sat-io/open-datasets/TIGER/[YEAR]/Roads` | USA + territories | 2009-2025 | Annual | Vector lines | Community - annual road-network releases |
| TIGER US Census Roads | `TIGER/2016/Roads` | USA + territories | 2016 | Single snapshot | Vector lines | Official - road runoff proxy for salts, metals, and urban drainage |

### Atmospheric Deposition and Fire Proxies

| Dataset | Asset ID | Spatial Extent | Temporal Extent | Temporal Resolution | Spatial Resolution | Status / Notes |
|---|---|---|---|---|---|---|
| Sentinel-5P OFFL NO2 | `COPERNICUS/S5P/OFFL/L3_NO2` | Global | 2018-present | Near-daily | 1113.2 m | Official - core atmospheric nitrogen loading proxy |
| Sentinel-5P OFFL SO2 | `COPERNICUS/S5P/OFFL/L3_SO2` | Global | 2018-present | Near-daily | 1113.2 m | Official - core atmospheric sulfur loading proxy |
| TEMPO NO2 L3 QA | `NASA/TEMPO/NO2_L3_QA` | North America field of regard | 2023-08-01 to 2025-09-16 (catalog) | Hourly / daytime sampling | 2226 m | Official - higher-frequency North America air-quality proxy |
| MTBS Burn Severity Mosaics | `USFS/GTAC/MTBS/annual_burn_severity_mosaics/v1` | CONUS + AK + HI + PR | 1984-2024 | Annual | 30 m | Official - fire disturbance context for US sites |

### Nighttime Lights

| Dataset | Asset ID | Spatial Extent | Temporal Extent | Temporal Resolution | Spatial Resolution | Status / Notes |
|---|---|---|---|---|---|---|
| VIIRS DNB | Various official VIIRS collections | Global | 2014-present | Monthly / annual composites | ~500 m (15 arc-sec) | Official - post-DMSP nighttime lights family |
| Simulated NPP-VIIRS (SVNL) | Community catalog | Global | 1992-2023 | Annual | ~500 m (15 arc-sec) | Community - extended VIIRS-like record |
| Harmonized Global Night Time Lights | Community catalog | Global | 1992-2021 continuous | Time series | ~1 km / 500 m | Community - harmonized DMSP and VIIRS record |
| DMSP-OLS Nighttime Lights | `NOAA/DMSP-OLS/NIGHTTIME_LIGHTS` | Global | 1992-2013 | Annual composites | ~1 km | Official - long historical urbanization proxy |

### Climate Support

| Dataset | Asset ID | Spatial Extent | Temporal Extent | Temporal Resolution | Spatial Resolution | Status / Notes |
|---|---|---|---|---|---|---|
| ERA5-Land Hourly | `ECMWF/ERA5_LAND/HOURLY` | Global land | 1950-present | Hourly | 11132 m | Official - hourly hydroclimate context |
| ERA5-Land Daily Aggregated | `ECMWF/ERA5_LAND/DAILY_AGGR` | Global land | 1950-present | Daily | 11132 m | Official - daily hydroclimate covariates |
| ERA5-Land Monthly Aggregated | `ECMWF/ERA5_LAND/MONTHLY_AGGR` | Global land | 1950-present | Monthly | 11132 m | Official - monthly hydroclimate summaries |

### Topographic Support

| Dataset | Asset ID | Spatial Extent | Temporal Extent | Temporal Resolution | Spatial Resolution | Status / Notes |
|---|---|---|---|---|---|---|
| ALOS PALSAR DEM | JAXA product family | Global | Various | Static / product family | 12.5 m to 30 m | Official - higher-accuracy elevation family |
| Copernicus DEM GLO-30 | `COPERNICUS/DEM/GLO30` | Global | 2010-2015 | Static | 30 m | Official - more recent global DEM |
| SRTM DEM 30m | `USGS/SRTMGL1_003` | Global (60N-56S) | 2000 | Static | 30 m (1 arc-sec) | Official - baseline elevation surface |
| SRTM DEM 90m | `CGIAR/SRTM90_V4` | Global (60N-56S) | 2000 | Static | 90 m (3 arc-sec) | Official - coarser elevation surface |

## Obvious Public-EE Gaps / Upload Candidates

This section is separate from the active GEE inventory above. These are gaps after checking the current official and community catalogs for this pass.

| Dataset / theme | Current public EE status | Why it is an obvious gap | Upload note |
|---|---|---|---|
| Latest Gridded Livestock of the World release | Not in public EE in the catalog searches used for this pass | Canonical global livestock pressure layer for manure and grazing intensity | Strong community-upload candidate if licensing and hosting are straightforward |
| Road salt / deicer application layers | No public EE dataset found in the official/community searches used for this pass | Important for chloride and sodium impacts near cold-region roads | Important gap, but I did not identify a single global open gridded product ready for one-step upload |
| Septic systems / onsite sanitation density | No public EE dataset found in the official/community searches used for this pass | Important diffuse human waste pressure in peri-urban and rural watersheds | Important gap, but I did not identify a standard global open product ready for straightforward community upload |

## Catalog Scope Note

The Earth Engine official catalog is only one part of the usable inventory. This restored table intentionally keeps:

- official catalog datasets
- community catalog datasets
- project assets and external layers that may require manual import

## Key Sources

- https://developers.google.com/earth-engine/datasets
- https://developers.google.com/earth-engine/datasets/catalog
- https://developers.google.com/earth-engine/datasets/community
- https://gee-community-catalog.org/
- https://gee-community-catalog.org/projects/landscan/
- https://gee-community-catalog.org/projects/npk/
- https://gee-community-catalog.org/projects/pest_chemgrids/
- https://gee-community-catalog.org/projects/hydrowaste/
- https://gee-community-catalog.org/projects/tiger_roads/
- https://gee-community-catalog.org/projects/ogim/
- https://gee-community-catalog.org/projects/climate_trace/

---

**Last Updated:** 2026-04-07
**Researcher:** Sidney Bush

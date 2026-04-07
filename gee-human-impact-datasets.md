# Google Earth Engine Human Impact Datasets for Watershed Applications

This is a working reference for basin and watershed studies in Google Earth Engine. The emphasis is on layers that are practical to join to catchments, interpretable in a hydrologic setting, and useful for explaining likely human influence on stream chemistry, flow alteration, or watershed condition.

## First-Pass Layers for Watershed Screening

These are the layers I would reach for first in a global screening workflow. Together they cover the main pressure types without forcing a very specialized analysis from the start.

| Dataset | EE Source | Asset ID | Spatial Extent | Temporal Extent | Temporal Resolution | Spatial Resolution | Key Attributes |
|---|---|---|---|---|---|---|---|
| GAIA (Year of Change to Impervious) | Official | `Tsinghua/FROM-GLC/GAIA/v10` | Global | 1985-2018 | Encoded annual transition year | 30 m | Year each pixel first converted to impervious cover |
| Global Human Modification v3 | Community | `projects/sat-io/open-datasets/ghm-v3` | Global | 1990-2022 (5-year steps) | 5-year epochs | 300 m and 90 m | Time-varying human pressure index |
| GHSL Built-up Surface | Official | `JRC/GHSL/P2023A/GHS_BUILT_S` | Global | 1975-2030 | 5-year epochs | 100 m | Built-up fraction and urban footprint |
| GHSL Population | Official | `JRC/GHSL/P2023A/GHS_POP` | Global | 1975-2030 | 5-year epochs | 100 m | Population counts and density |
| Sentinel-5P OFFL NO2 | Official | `COPERNICUS/S5P/OFFL/L3_NO2` | Global | 2018-present | Near-daily | 1113.2 m | Tropospheric NO2 burden |
| Sentinel-5P OFFL SO2 | Official | `COPERNICUS/S5P/OFFL/L3_SO2` | Global | 2018-present | Near-daily | 1113.2 m | SO2 burden |
| Global Human Modification (gHM) | Official | `CSP/HM/GlobalHumanModification` | Global terrestrial | 2016 | Single year | 1000 m | Composite human modification index |
| NPKGRIDS | Community | `projects/sat-io/open-datasets/NPKGRIDS` | Global | 2015-2020 (circa 2020) | Static snapshot | 0.05 deg (~5.6 km) | N, P2O5, and K2O application rates |
| Global Dam Watch (GDW) | Community | `projects/sat-io/open-datasets/GDW/GDW_BARRIERS_V1_0` | Global | Current | Static snapshot | Vector points | Barrier locations and basic dam attributes |
| HydroATLAS Basins L06 | Official | `WWF/HydroATLAS/v1/Basins/level06` | Global | Static | Static table | Vector basins | Basin-scale anthropogenic covariates |
| TIGER US Census Roads | Official | `TIGER/2016/Roads` | USA + territories | 2016 | Single snapshot | Vector lines | Mapped road network geometry |

## Useful Add-Ons for More Specific Questions

These are the layers I would pull in once the question narrows, for example wastewater, pesticides, urban form, roads, or fire history.

| Dataset | EE Source | Asset ID | Spatial Extent | Temporal Extent | Temporal Resolution | Spatial Resolution | Best Use |
|---|---|---|---|---|---|---|---|
| GHSL Settlement Characteristics | Official | `JRC/GHSL/P2023A/GHS_BUILT_C` | Global | 2018 | Single epoch | 10 m | Useful when settlement form matters, not just footprint |
| WorldPop Residential Population | Official | `WorldPop/GP/100m/pop` | Global | 2000-2021 | Annual | 92.77 m | Better choice when fine population gradients matter |
| GHSL Building Height 2018 | Official | `JRC/GHSL/P2023A/GHS_BUILT_H` | Global | 2018 | Single epoch | 100 m | Adds vertical urban intensity that footprint layers miss |
| GHSL Building Volume | Official | `JRC/GHSL/P2023A/GHS_BUILT_V` | Global | 1975-2030 | 5-year epochs | 100 m | Helps separate dense built fabric from low-rise spread |
| ESA WorldCover v200 | Official | `ESA/WorldCover/v200` | Global | 2021 | Single epoch | 10 m | Quick support layer for cropland, urban land, and general land cover |
| HydroWASTE v1.0 | Community | `projects/sat-io/open-datasets/HydroWaste/HydroWASTE_v10` | Global | 2022 release | Static snapshot | Vector points | Good first pass for wastewater infrastructure and likely point discharges |
| PEST-CHEMGRIDS | Community | `projects/sat-io/open-datasets/PEST-CHEMGRIDS/application_rates` | Global | 2015-2025 | Multi-epoch | ~10 km (5 arc-min) | Useful when pesticide pressure matters alongside fertilizer |
| LandScan Population Data Global 1km | Community | `projects/sat-io/open-datasets/ORNL/LANDSCAN_GLOBAL` | Global | 2000-2023 | Annual | ~1 km (30 arc-sec) | Annual population alternative with a different modeling approach |
| Global Power | Community | `projects/sat-io/open-datasets/predictive-global-power-system/*` | Global | 2020 release | Static snapshot | 250 m raster plus vector lines | Good infrastructure context around grid corridors and power access |
| Oil and Gas Infrastructure Mapping (OGIM) | Community | `projects/sat-io/open-datasets/OGIM/*` | Global | Current (inputs through 2025-02) | Static snapshot | Mixed vector geometries | Useful around oil and gas basins, pipelines, and production fields |
| Climate TRACE Global Emissions Data | Community | `projects/sat-io/open-datasets/CLIMATE-TRACE/EMISSIONS/*` | Global | Recent multi-year inventory | Time series / sector-dependent | Mixed vector geometries | Adds sector-specific emissions context when source sectors matter |
| Global Roads Inventory Project (GRIP4) | Community | `projects/sat-io/open-datasets/GRIP4/[region]` | Global (by region) | Current | Static snapshot | ~8 km density plus vector regional assets | Good road coverage outside the US where TIGER is not relevant |
| GHSL Degree of Urbanization V2-0 | Official | `JRC/GHSL/P2023A/GHS_SMOD_V2-0` | Global | 1975-2030 | 5-year epochs | 1000 m | Helpful for consistent urban-rural class splits |
| GISD30 | Community | `projects/sat-io/open-datasets/GISD30_1985_2020` | Global | 1985-2020 | Multi-year time series | 30 m | Alternate impervious history for sensitivity checks |
| GISA | Community | `projects/sat-io/open-datasets/GISA_1972_2021` | Global | 1972-2021 | Multi-year time series | 30 m | Longest screened built-up time series |
| USDA NASS CDL | Official | `USDA/NASS/CDL` | CONUS | 2008-2024 | Annual | 10 m (2024), 30 m (prior) | Best crop detail for US basins |
| TIGER Roads Time Series | Community | `projects/sat-io/open-datasets/TIGER/[YEAR]/Roads` | USA + territories | 2009-2025 | Annual | Vector lines | Use this when road timing matters more than a single static road map |
| MTBS Burn Severity Mosaics | Official | `USFS/GTAC/MTBS/annual_burn_severity_mosaics/v1` | CONUS + AK + HI + PR | 1984-2024 | Annual | 30 m | Useful fire-disturbance context for US watersheds |
| TEMPO NO2 L3 QA | Official | `NASA/TEMPO/NO2_L3_QA` | North America field of regard | 2023-08-01 to 2025-09-16 (catalog) | Hourly / daytime sampling | 2226 m | Better temporal detail than Sentinel-5P for North America |

## Working Inventory

Companion CSV in the Box documentation folder:
`/Users/sidneybush/Library/CloudStorage/Box-Box/Sidney_Bush/SiSyn/data_checking/documentation/gee-human-impact-datasets-global-join.csv`

CSV fields: `theme`, `dataset`, `asset_id`, `catalog_type`, `spatial_extent`, `temporal_extent`, `temporal_cadence`, `nominal_resolution`, `scale_similarity_vs_era5_modis`, `stream_chemistry_relevance`, `recommendation`, `global_join_notes`.

In the CSV, `catalog_type` is kept as `Official`, `Community`, `Project asset`, or `Not in public EE`.

### Population and Settlement Baselines

| Dataset | EE Source | Asset ID | Spatial Extent | Temporal Extent | Temporal Resolution | Spatial Resolution | Application Notes |
|---|---|---|---|---|---|---|---|
| GHSL Settlement Characteristics | Official | `JRC/GHSL/P2023A/GHS_BUILT_C` | Global | 2018 | Single epoch | 10 m | Best when settlement texture or built form matters |
| WorldPop Residential Population | Official | `WorldPop/GP/100m/pop` | Global | 2000-2021 | Annual | 92.77 m | Good high-detail population surface for catchment screening |
| GHSL Built-up Surface (P2023A) | Official | `JRC/GHSL/P2023A/GHS_BUILT_S` | Global | 1975-2030 | 5-year epochs | 100 m | Solid default built-up baseline with time slices back to 1975 |
| GHSL Building Height 2018 (P2023A) | Official | `JRC/GHSL/P2023A/GHS_BUILT_H` | Global | 2018 | Single epoch | 100 m | Adds vertical urban intensity in dense settlements |
| GHSL Building Volume (P2023A) | Official | `JRC/GHSL/P2023A/GHS_BUILT_V` | Global | 1975-2030 | 5-year epochs | 100 m | Useful where total built volume matters more than footprint alone |
| GHSL Population (P2023A) | Official | `JRC/GHSL/P2023A/GHS_POP` | Global | 1975-2030 | 5-year epochs | 100 m | Good global population baseline with consistent time slices |
| WorldPop Age/Sex | Official | `WorldPop/GP/100m/pop_age_sex` | Global | 2020-2021 | Annual snapshot | 100 m | Use when demographic structure matters, not just total population |
| GPWv4.11 Population Count | Official | `CIESIN/GPWv411/GPW_Population_Count` | Global | 2000-2020 | 5-year epochs | 927.67 m | Stable coarse population reference with transparent inputs |
| GPWv4.11 Population Density | Official | `CIESIN/GPWv411/GPW_Population_Density` | Global | 2000-2020 | 5-year epochs | 927.67 m | Same GPW baseline in density form |
| LandScan Population Data Global 1km | Community | `projects/sat-io/open-datasets/ORNL/LANDSCAN_GLOBAL` | Global | 2000-2023 | Annual | ~1 km (30 arc-sec) | Annual population option with a different modeling approach |
| GHSL Degree of Urbanization V2-0 | Official | `JRC/GHSL/P2023A/GHS_SMOD_V2-0` | Global | 1975-2030 | 5-year epochs | 1000 m | Helpful for consistent urban-rural splits across regions |

### Water Infrastructure and Basin Context

| Dataset | EE Source | Asset ID | Spatial Extent | Temporal Extent | Temporal Resolution | Spatial Resolution | Application Notes |
|---|---|---|---|---|---|---|---|
| HydroWASTE v1.0 | Community | `projects/sat-io/open-datasets/HydroWaste/HydroWASTE_v10` | Global | 2022 release | Static snapshot | Vector points | Good first pass for wastewater facilities and likely discharge points |
| Global Dam Watch (GDW) | Community | `projects/sat-io/open-datasets/GDW/GDW_BARRIERS_V1_0` | Global | Current | Static snapshot | Vector points | Strong default layer for dams and other barriers |
| GOODD Dams | Community | `projects/sat-io/open-datasets/GOODD/GOOD2_dams` | Global | Current | Static snapshot | Vector points | Useful alternate dam inventory for cross-checking coverage |
| Global Dam Tracker (GDAT) | Community | Community catalog (GDAT) | Global | 1990s-2020s | Event time series / updates | Vector points | Worth using when commissioning timing or status changes matter |
| GDW Reservoirs | Community | `projects/sat-io/open-datasets/GDW/GDW_RESERVOIRS_V1_0` | Global | Current | Static snapshot | Vector polygons | Adds inundation and reservoir footprint context |
| GOODD Catchments | Community | `projects/sat-io/open-datasets/GOODD/GOOD2_catchments` | Global | Current | Static snapshot | Vector polygons | Convenient upstream catchments tied to mapped dams |
| HydroATLAS Basins L06 | Official | `WWF/HydroATLAS/v1/Basins/level06` | Global | Static | Static table | Vector basins | Good basin table for anthropogenic context and watershed covariates |

### Agriculture, Fertilizer, Pesticides, and Grazing

| Dataset | EE Source | Asset ID | Spatial Extent | Temporal Extent | Temporal Resolution | Spatial Resolution | Application Notes |
|---|---|---|---|---|---|---|---|
| ESA WorldCover v200 | Official | `ESA/WorldCover/v200` | Global | 2021 | Single epoch | 10 m | Quick land-cover support layer for cropland and built land |
| GCEP30 Cropland Extent | Community | `projects/sat-io/open-datasets/gcep30` | Global | ~2015 | Single epoch | 30 m | Useful high-resolution cropland mask |
| LGRIP30 Irrigated/Rainfed | Community | `projects/sat-io/open-datasets/lgrip30` | Global | 2014-2017 (nominal 2015) | Single epoch | 30 m | Separates irrigated from rainfed agriculture |
| GCI30 Cropping Intensity | Community | `projects/sat-io/open-datasets/gci30` | Global | Recent | Single epoch | 30 m | Useful where cropping intensity matters more than crop identity |
| GLC_FCS30D | Community | `projects/sat-io/open-datasets/GLC-FCS30D/annual` | Global | 1985-2022 (annual from 2000 onward) | Annual / multi-epoch | 30 m | Best screened global crop-type detail in this inventory |
| Global Pasture Watch | Community | `global-pasture-watch/*` collections | Global | 2000-2022 | Annual | 30 m | Good grazing and managed pasture context |
| GFSAD1000 Cropland Extent | Official | `USGS/GFSAD1000_V1` | Global | ~2010 (2007-2012 source window) | Single epoch | 1000 m | Coarse cropland baseline when fine products are unnecessary |
| NPKGRIDS | Community | `projects/sat-io/open-datasets/NPKGRIDS` | Global | 2015-2020 (circa 2020) | Static snapshot | 0.05 deg (~5.6 km) | Most direct fertilizer pressure layer in the public GEE set |
| PEST-CHEMGRIDS | Community | `projects/sat-io/open-datasets/PEST-CHEMGRIDS/application_rates` | Global | 2015-2025 | Multi-epoch | ~10 km (5 arc-min) | Useful complement when pesticide pressure is plausible |
| Gridded Livestock of the World (GLW3) | Not in public EE | External (FAO/Harvard) | Global | 2010 | Single epoch | ~10 km (5 arc-min) | Still worth importing manually for livestock and manure pressure |
| Global Fertilizer by Crop | Community | Community catalog CSV | Global | 2017-2018 period | Periodic summary | Country/crop tables | Reference dataset only; not suitable for direct spatial joins |
| EUCROPMAP | Official | `JRC/D5/EUCROPMAP/V1` | Europe (EU) | 2018, 2022 | Multi-epoch | 10 m | Good crop detail for European basins |
| USDA NASS CDL | Official | `USDA/NASS/CDL` | CONUS | 2008-2024 | Annual | 10 m (2024), 30 m (prior) | Best crop and pasture detail for US basins |
| Canada AAFC ACI | Official | `AAFC/ACI` | Canada | 2009-2023 | Annual | 30 m (56 m in 2009-2010) | Good crop detail for Canadian basins |

### Human Modification, Accessibility, and Impervious Change

| Dataset | EE Source | Asset ID | Spatial Extent | Temporal Extent | Temporal Resolution | Spatial Resolution | Application Notes |
|---|---|---|---|---|---|---|---|
| World Settlement Footprint 2015 | Official | `DLR/WSF/WSF2015/v1` | Global | 2014-2015 | Single epoch | 10 m | High-resolution settlement footprint snapshot |
| World Settlement Footprint 2019 | Community | `projects/sat-io/open-datasets/WSF/WSF_2019` | Global | 2019 | Single epoch | 10 m | Updated settlement footprint for more recent conditions |
| GAIA (Year of Change to Impervious) | Official | `Tsinghua/FROM-GLC/GAIA/v10` | Global | 1985-2018 | Encoded annual transition year | 30 m | Good default for tracking when impervious cover appeared |
| WSF Evolution | Community | `projects/sat-io/open-datasets/WSF/WSF_EVO` | Global | 1985-2015 | Annual | 30 m | Annual settlement change alternative to GAIA |
| GISD30 | Community | `projects/sat-io/open-datasets/GISD30_1985_2020` | Global | 1985-2020 | Multi-year time series | 30 m | Useful secondary impervious trajectory product |
| GISA | Community | `projects/sat-io/open-datasets/GISA_1972_2021` | Global | 1972-2021 | Multi-year time series | 30 m | Longest built-up time series in this screened set |
| Global Human Modification v3 | Community | `projects/sat-io/open-datasets/ghm-v3` | Global | 1990-2022 (5-year steps) | 5-year epochs | 300 m and 90 m | Strong time-varying human pressure layer for broad screening |
| Global Human Modification (gHM) | Official | `CSP/HM/GlobalHumanModification` | Global terrestrial | 2016 | Single year | 1000 m | Simple composite pressure layer when one summary index is enough |
| WCS Human Impact Index | Project asset | `projects/HII/v1/hii` | Global | Time series | Time series | Variable | Useful internal layer if that workflow is already established |
| Accessibility to Cities 2015 | Official | `Oxford/MAP/accessibility_to_cities_2015_v1_0` | Broad global (-60 to 85 latitude) | 2015 | Single epoch | 927.67 m | Travel-time proxy that is still useful, but dated |
| NLCD Impervious | Official | `USGS/NLCD_RELEASES/2021_REL/NLCD` | CONUS + Alaska | 2001-2021 (multiple epochs) | Multi-epoch | 30 m | Best regional impervious product for US analyses |

### Roads, Industry, Mining, and Emissions

| Dataset | EE Source | Asset ID | Spatial Extent | Temporal Extent | Temporal Resolution | Spatial Resolution | Application Notes |
|---|---|---|---|---|---|---|---|
| Oil and Gas Infrastructure Mapping (OGIM) | Community | `projects/sat-io/open-datasets/OGIM/*` | Global | Current (inputs through 2025-02) | Static snapshot | Mixed vector geometries | Good oil and gas footprint layer for production basins |
| Global Mining Footprints | Community | `projects/sat-io/open-datasets/global-mining/global_mining_footprints` | Global | Current | Static snapshot | High-resolution polygons | High-resolution map of active or recent mining footprints |
| Global Power Plant Database | Official | `WRI/GPPD/power_plants` | Global | 2018 | Single snapshot | Vector points | Good point-source layer for thermal and industrial facilities |
| Climate TRACE Global Emissions Data | Community | `projects/sat-io/open-datasets/CLIMATE-TRACE/EMISSIONS/*` | Global | Recent multi-year inventory | Time series / sector-dependent | Mixed vector geometries | Useful when sector-specific emissions context matters |
| Global Mining Areas | Community | `projects/sat-io/open-datasets/global-mining/global_mining_polygons` | Global | 2000-2017 | Static inventory | Vector polygons | Broader mining inventory with type and area context |
| Global Power | Community | `projects/sat-io/open-datasets/predictive-global-power-system/*` | Global | 2020 release | Static snapshot | 250 m raster plus vector lines | Useful infrastructure context around grids and transmission |
| Global Roads Inventory Project (GRIP4) | Community | `projects/sat-io/open-datasets/GRIP4/[region]` | Global (by region) | Current | Static snapshot | ~8 km density plus vector regional assets | Useful global road coverage outside the US |
| Microsoft Bing Global Mined Roads | Community | Community catalog | Global | 2020-2022 | Recent snapshot | Vector | Additional road coverage, but worth checking carefully before use |
| TIGER Roads Time Series | Community | `projects/sat-io/open-datasets/TIGER/[YEAR]/Roads` | USA + territories | 2009-2025 | Annual | Vector lines | Best US option when road timing matters |
| TIGER US Census Roads | Official | `TIGER/2016/Roads` | USA + territories | 2016 | Single snapshot | Vector lines | Straightforward road proxy for runoff and urban drainage in the US |

### Atmospheric Deposition and Fire Proxies

| Dataset | EE Source | Asset ID | Spatial Extent | Temporal Extent | Temporal Resolution | Spatial Resolution | Application Notes |
|---|---|---|---|---|---|---|---|
| Sentinel-5P OFFL NO2 | Official | `COPERNICUS/S5P/OFFL/L3_NO2` | Global | 2018-present | Near-daily | 1113.2 m | Good atmospheric nitrogen loading proxy near combustion sources |
| Sentinel-5P OFFL SO2 | Official | `COPERNICUS/S5P/OFFL/L3_SO2` | Global | 2018-present | Near-daily | 1113.2 m | Good sulfur and combustion proxy around power and industrial sources |
| TEMPO NO2 L3 QA | Official | `NASA/TEMPO/NO2_L3_QA` | North America field of regard | 2023-08-01 to 2025-09-16 (catalog) | Hourly / daytime sampling | 2226 m | Best high-frequency NO2 option for North American sites |
| MTBS Burn Severity Mosaics | Official | `USFS/GTAC/MTBS/annual_burn_severity_mosaics/v1` | CONUS + AK + HI + PR | 1984-2024 | Annual | 30 m | Useful fire-disturbance context for US watersheds |

### Nighttime Lights

| Dataset | EE Source | Asset ID | Spatial Extent | Temporal Extent | Temporal Resolution | Spatial Resolution | Application Notes |
|---|---|---|---|---|---|---|---|
| VIIRS DNB | Official | Various official VIIRS collections | Global | 2014-present | Monthly / annual composites | ~500 m (15 arc-sec) | Default modern nighttime lights product |
| Simulated NPP-VIIRS (SVNL) | Community | Community catalog | Global | 1992-2023 | Annual | ~500 m (15 arc-sec) | Extended VIIRS-like record back before 2014 |
| Harmonized Global Night Time Lights | Community | Community catalog | Global | 1992-2021 continuous | Time series | ~1 km / 500 m | Useful for long continuous light trends |
| DMSP-OLS Nighttime Lights | Official | `NOAA/DMSP-OLS/NIGHTTIME_LIGHTS` | Global | 1992-2013 | Annual composites | ~1 km | Long historical urbanization and electrification proxy |

### Climate Support

| Dataset | EE Source | Asset ID | Spatial Extent | Temporal Extent | Temporal Resolution | Spatial Resolution | Application Notes |
|---|---|---|---|---|---|---|---|
| ERA5-Land Hourly | Official | `ECMWF/ERA5_LAND/HOURLY` | Global land | 1950-present | Hourly | 11132 m | Useful when matching short hydroclimate windows |
| ERA5-Land Daily Aggregated | Official | `ECMWF/ERA5_LAND/DAILY_AGGR` | Global land | 1950-present | Daily | 11132 m | Good default climate covariate table for basin summaries |
| ERA5-Land Monthly Aggregated | Official | `ECMWF/ERA5_LAND/MONTHLY_AGGR` | Global land | 1950-present | Monthly | 11132 m | Useful for broad climate normals and seasonal summaries |

### Topographic Support

| Dataset | EE Source | Asset ID | Spatial Extent | Temporal Extent | Temporal Resolution | Spatial Resolution | Application Notes |
|---|---|---|---|---|---|---|---|
| ALOS PALSAR DEM | Official | JAXA product family | Global | Various | Static / product family | 12.5 m to 30 m | Good higher-detail elevation family where available |
| Copernicus DEM GLO-30 | Official | `COPERNICUS/DEM/GLO30` | Global | 2010-2015 | Static | 30 m | Good default recent global DEM |
| SRTM DEM 30m | Official | `USGS/SRTMGL1_003` | Global (60N-56S) | 2000 | Static | 30 m (1 arc-sec) | Baseline elevation surface with broad familiarity |
| SRTM DEM 90m | Official | `CGIAR/SRTM90_V4` | Global (60N-56S) | 2000 | Static | 90 m (3 arc-sec) | Coarser fallback when 30 m detail is unnecessary |

## Gaps Worth Uploading

This section is separate from the active public-EE inventory above. These are still the clearest holes for watershed applications after checking the official and community catalogs in this pass.

| Dataset / theme | Public EE status | Why it matters for watershed work | Possible next step |
|---|---|---|---|
| Latest Gridded Livestock of the World release | Not currently in public EE | Standard global livestock pressure layer for manure and grazing intensity | Worth checking for a community upload if the current release can be hosted cleanly |
| Road salt / deicer application layers | No public EE layer identified in this pass | Important for chloride and sodium work in cold-region road networks | More likely a regional compilation problem than a single global upload |
| Septic systems / onsite sanitation density | No public EE layer identified in this pass | Important diffuse wastewater pressure in peri-urban and rural catchments | Strong candidate if a consistent open gridded product can be assembled |

## Scope

This inventory intentionally mixes official Earth Engine layers, community catalog layers, and a few project or external datasets that are still useful in real workflows. The goal here is practical coverage for watershed applications, not a catalog-only list.

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

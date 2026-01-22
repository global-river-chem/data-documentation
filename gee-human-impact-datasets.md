# Google Earth Engine Human Impact Datasets

Research findings for human impact datasets available on Google Earth Engine relevant to river chemistry analysis.

## Dataset Inventory

### Population Datasets

| Dataset Name | GEE Asset ID | Spatial Extent | Temporal Coverage | Resolution | Key Variables | Notes |
|--------------|--------------|----------------|-------------------|------------|---------------|-------|
| GHSL Population (P2023A) | `JRC/GHSL/P2023A/GHS_POP` | Global | 1975-2030 (5-yr intervals) | 100m | Population count, density | Projections to 2025, 2030 |
| WorldPop Global Project | `WorldPop/GP/100m/pop` | Global | Annual, recent years | 100m | Residential population | Census-disaggregated |
| WorldPop Age/Sex | `WorldPop/GP/100m/pop_age_sex` | Global | Annual, recent years | 100m | Population by age/sex | Demographic structure |
| GPWv4.11 Population Count | `CIESIN/GPWv411/GPW_Population_Count` | Global | 2000, 2005, 2010, 2015, 2020 | ~1km (30 arc-sec) | Population count | Standard reference |
| GPWv4.11 Population Density | `CIESIN/GPWv411/GPW_Population_Density` | Global | 2000, 2005, 2010, 2015, 2020 | ~1km (30 arc-sec) | People per km² | Standard reference |

### Dams and Reservoirs

| Dataset Name | GEE Asset ID | Spatial Extent | Temporal Coverage | Resolution | Key Variables | Notes |
|--------------|--------------|----------------|-------------------|------------|---------------|-------|
| Global Dam Watch (GDW) | `projects/sat-io/open-datasets/GDW/GDW_BARRIERS_V1_0` | Global | Current (41,145 barriers) | Vector points | Dam location, attributes | Harmonized with river networks |
| GDW Reservoirs | `projects/sat-io/open-datasets/GDW/GDW_RESERVOIRS_V1_0` | Global | Current (35,295 reservoirs) | Vector polygons | Reservoir area, volume | Associated with barriers |
| GOODD Dams | `projects/sat-io/open-datasets/GOODD/GOOD2_dams` | Global | Current (38,000+ dams) | Vector points | Dam attributes | Includes catchments |
| GOODD Catchments | `projects/sat-io/open-datasets/GOODD/GOOD2_catchments` | Global | Current | Vector polygons | Catchment area | Dam-specific catchments |
| Global Dam Tracker (GDAT) | Community catalog | Global | 1990s-2020s | Vector points | Height, capacity, purpose | Temporal analysis capable |

### Agriculture and Cropland - Global

| Dataset Name | GEE Asset ID | Spatial Extent | Temporal Coverage | Resolution | Crop Type Detail | Notes |
|--------------|--------------|----------------|-------------------|------------|------------------|-------|
| GFSAD1000 Cropland | `USGS/GFSAD1000_V1` | Global | ~2010 (2007-2012 data) | 1km | Binary cropland/non-cropland | No crop types |
| GCEP30 Cropland Extent | `projects/sat-io/open-datasets/gcep30` | Global | ~2015 | 30m | Binary cropland/non-cropland | No crop types or pasture |
| LGRIP30 Irrigated/Rainfed | `projects/sat-io/open-datasets/lgrip30` | Global | 2014-2017 (nominal 2015) | 30m | Irrigated vs rainfed cropland | No crop types or pasture |
| GCI30 Cropping Intensity | `projects/sat-io/open-datasets/gci30` | Global | Recent | 30m | Crop frequency | Multi-cropping intensity |
| GLC_FCS30D | `projects/sat-io/open-datasets/GLC-FCS30D/annual` | Global | 1985-2022 (annual 2000+) | 30m | 4 cropland types: rainfed, herbaceous, orchard, irrigated | Also grassland, 8 forest types, wetlands |

### Agriculture and Cropland - Regional (High Detail)

| Dataset Name | GEE Asset ID | Spatial Extent | Temporal Coverage | Resolution | Crop Type Detail | Notes |
|--------------|--------------|----------------|-------------------|------------|------------------|-------|
| USDA NASS CDL | `USDA/NASS/CDL` | CONUS (USA) | Annual 2008-2024 | 10m (2024), 30m (prior) | 254 classes: corn, soybeans, wheat, cotton, rice, hay, pasture, 50+ crop types | Includes pasture/hay distinction |
| Canada AAFC ACI | `AAFC/ACI` | Canada | Annual 2009-2023 | 30m (56m in 2009-10) | 40+ crops: grains, oilseeds, pulses, forage, pasture, vegetables | Includes pasture, fallow |
| EUCROPMAP | `JRC/D5/EUCROPMAP/V1` | Europe (EU) | 2018, 2022 | 10m | Multiple crop types from Sentinel | Detailed crop classification |

### Fertilizer Application

| Dataset Name | GEE Asset ID | Spatial Extent | Temporal Coverage | Resolution | Key Variables | Notes |
|--------------|--------------|----------------|-------------------|------------|---------------|-------|
| NPKGRIDS | `projects/sat-io/open-datasets/NPKGRIDS` | Global | 2015-2020 (circa 2020) | 0.05° (~5.6km) | N, P₂O₅, K₂O by crop (173 crops) | Only gridded fertilizer dataset |
| Global Fertilizer by Crop | Community catalog CSV | Global | 2017-18 period | Country/crop level | NPK usage statistics | Non-spatial |

### Human Footprint and Modification

| Dataset Name | GEE Asset ID | Spatial Extent | Temporal Coverage | Resolution | Key Variables | Notes |
|--------------|--------------|----------------|-------------------|------------|---------------|-------|
| Global Human Modification | `CSP/HM/GlobalHumanModification` | Global (terrestrial) | 2016 | 1km | Modification index (0-1) | 5 stressor types |
| Global Human Modification v3 | `projects/sat-io/open-datasets/ghm-v3` | Global | 1990-2022 (5-yr steps) | 300m & 90m | Modification index | Temporal change analysis |
| World Settlement Footprint 2015 | `DLR/WSF/WSF2015/v1` | Global | 2014-2015 | 10m | Binary settlement mask | Landsat + Sentinel-1 |
| World Settlement Footprint 2019 | `projects/sat-io/open-datasets/WSF/WSF_2019` | Global | 2019 | 10m | Binary settlement mask | Sentinel-1 & 2 |
| WSF Evolution | `projects/sat-io/open-datasets/WSF/WSF_EVO` | Global | 1985-2015 (annual) | 30m | Settlement change | Urban expansion tracking |
| WCS Human Impact Index | `projects/HII/v1/hii` | Global | Time series | Variable | Infrastructure, land use, etc. | Multi-driver index |

### Roads and Infrastructure

| Dataset Name | GEE Asset ID | Spatial Extent | Temporal Coverage | Resolution | Key Variables | Notes |
|--------------|--------------|----------------|-------------------|------------|---------------|-------|
| Global Roads Inventory Project (GRIP4) | `projects/sat-io/open-datasets/GRIP4/[region]` | Global (by region) | Current | ~8km for density; vectors | Road type, density | Regional asset structure |
| Microsoft Bing Global Mined Roads | Community catalog | Global | 2020-2022 | Vector | Road segments (47.8M km) | AI-extracted from imagery |

### Nighttime Lights (Urbanization Proxy)

| Dataset Name | GEE Asset ID | Spatial Extent | Temporal Coverage | Resolution | Key Variables | Notes |
|--------------|--------------|----------------|-------------------|------------|---------------|-------|
| DMSP-OLS Nighttime Lights | `NOAA/DMSP-OLS/NIGHTTIME_LIGHTS` | Global | 1992-2013 | ~1km | Stable lights, avg visible | Long time series |
| VIIRS DNB | Various VIIRS collections | Global | 2014-present | ~500m (15 arc-sec) | Radiance | Monthly/annual |
| Harmonized Global Night Time Lights | Community catalog | Global | 1992-2021 continuous | ~1km/500m | Radiance | DMSP + VIIRS harmonized |
| Simulated NPP-VIIRS (SVNL) | Community catalog | Global | 1992-2023 | ~500m (15 arc-sec) | Simulated radiance | Extended time series |

### Impervious Surfaces and Urban Extent

| Dataset Name | GEE Asset ID | Spatial Extent | Temporal Coverage | Resolution | Key Variables | Notes |
|--------------|--------------|----------------|-------------------|------------|---------------|-------|
| GISD30 | `projects/sat-io/open-datasets/GISD30_1985_2020` | Global | 1985-2020 | 30m | Impervious surface area | Landsat-based dynamics |
| GISA | `projects/sat-io/open-datasets/GISA_1972_2021` | Global | 1972-2021 | 30m | Impervious surface (93% accuracy) | Longest time series |
| FROM-GLC/GAIA | `Tsinghua/FROM-GLC/GAIA/v10` | Global | 1985-2018 | 30m | Year of transition to impervious | Annual change |
| NLCD Impervious | `USGS/NLCD_RELEASES/2021_REL/NLCD` | CONUS + Alaska | 2001-2021 (multiple epochs) | 30m | % impervious, impervious descriptor | Separates roads from urban |

### Livestock Density

| Dataset Name | GEE Asset ID | Spatial Extent | Temporal Coverage | Resolution | Key Variables | Notes |
|--------------|--------------|----------------|-------------------|------------|---------------|-------|
| Gridded Livestock of the World (GLW3) | External (FAO/Harvard) | Global | 2010 | ~10km (5 arc-min) | Cattle, sheep, goats, pigs, poultry | Not in GEE catalog, requires import |
| Global Pasture Watch | `global-pasture-watch/*` collections | Global | 2000-2022 | 30m | Cultivated/natural grassland | Grazing lands |

### Mining and Extraction

| Dataset Name | GEE Asset ID | Spatial Extent | Temporal Coverage | Resolution | Key Variables | Notes |
|--------------|--------------|----------------|-------------------|------------|---------------|-------|
| Global Mining Areas | `projects/sat-io/open-datasets/global-mining/global_mining_polygons` | Global | 2000-2017 (21,000+ polygons) | Vector polygons | Mining type, area | Includes tailings, waste dumps |
| Global Mining Footprints | `projects/sat-io/open-datasets/global-mining/global_mining_footprints` | Global | Current | High-res | Mining extent | High-resolution footprints |

### Climate and Environmental Variables

| Dataset Name | GEE Asset ID | Spatial Extent | Temporal Coverage | Resolution | Key Variables | Notes |
|--------------|--------------|----------------|-------------------|------------|---------------|-------|
| ERA5-Land Hourly | `ECMWF/ERA5_LAND/HOURLY` | Global (land) | 1950-present | ~11km (0.1°) | 50 vars: temp, precip, soil moisture, runoff, etc. | Climate reanalysis |
| ERA5-Land Daily | `ECMWF/ERA5_LAND/DAILY_AGGR` | Global (land) | 1950-present | ~11km (0.1°) | Same as hourly, daily aggregated | Daily summaries |
| ERA5-Land Monthly | `ECMWF/ERA5_LAND/MONTHLY_AGGR` | Global (land) | 1950-present | ~11km (0.1°) | Same as hourly, monthly aggregated | Monthly summaries |

### Topography and Elevation

| Dataset Name | GEE Asset ID | Spatial Extent | Temporal Coverage | Resolution | Key Variables | Notes |
|--------------|--------------|----------------|-------------------|------------|---------------|-------|
| SRTM DEM 30m | `USGS/SRTMGL1_003` | Global (60°N-56°S) | 2000 (one-time) | 30m (1 arc-sec) | Elevation | Void-filled |
| SRTM DEM 90m | `CGIAR/SRTM90_V4` | Global (60°N-56°S) | 2000 (one-time) | 90m (3 arc-sec) | Elevation | Lower resolution |
| Copernicus DEM GLO-30 | `COPERNICUS/DEM/GLO30` | Global | 2010-2015 | 30m | Elevation (DSM with vegetation) | More recent than SRTM |
| ALOS PALSAR DEM | JAXA products | Global | Various | 12.5m-30m | Elevation | Higher accuracy (5m RMSE) |

## Notes

### Data Access
- Official GEE catalog datasets: Accessible directly through Earth Engine
- Community catalog datasets: Require specific asset IDs (shown above)
- Most datasets are free for research, education, and nonprofit use
- Some datasets require citation and proper attribution

### Key Observations - Crop Type Detail
- **Global datasets**: Generally provide binary cropland/non-cropland or simple irrigated/rainfed (GCEP30, LGRIP30)
- **GLC_FCS30D**: Best global crop detail - distinguishes 4 cropland types (rainfed, herbaceous, orchard, irrigated) plus grassland
- **Regional high-detail**: USDA CDL (254 classes), Canada AAFC (40+ crops), EUCROPMAP all distinguish specific crops, pasture, hay
- **Pasture vs row crops**: Only available in regional datasets (CONUS CDL, Canada AAFC); global datasets lack this distinction
- **USDA CDL**: Most detailed - distinguishes corn, soybeans, wheat, cotton, alfalfa, "other hay", pasture/grass, plus 50+ specialty crops

### Key Observations - General
- **Population data**: Multiple high-quality options with different temporal coverage and resolution
- **Dams**: Excellent coverage with GDW being most comprehensive and harmonized with river networks
- **Agriculture resolution**: 30m resolution datasets (GCEP30, LGRIP30, GLC_FCS30D) offer best detail for global cropland; 10-30m for regional
- **Fertilizer**: NPKGRIDS is the only gridded fertilizer application dataset, highly valuable for nutrient analysis
- **Human footprint**: Multiple temporal options allow for change analysis from 1990-2022
- **Urban development**: Three major approaches - nighttime lights (proxy), impervious surfaces (direct), settlement footprints (binary)
- **Roads**: GRIP4 provides global coverage but regional asset structure; Microsoft roads offer recent AI-extracted network
- **Mining**: Comprehensive polygon datasets covering 2000-2017 period with global extent
- **Temporal depth**: Impervious surface data extends back to 1972 (GISA), nighttime lights to 1992, climate to 1950 (ERA5)
- **Climate**: ERA5-Land provides comprehensive meteorological variables at ~11km resolution from 1950-present

### Missing Data and Gaps
- **Wastewater treatment/discharge**: No global gridded datasets
- **Road salt application**: No direct datasets (could derive from road density + climate zones)
- **Point-source industrial pollution**: Facility-level discharge data not available
- **Livestock in GEE**: GLW3 available externally but requires manual import to GEE
- **Aquaculture facilities**: Limited global coverage
- **Septic systems**: No global density/usage data
- **Detailed pesticide application**: Not available at global scale (only fertilizer via NPKGRIDS)
- **Crop types globally**: Most global datasets don't distinguish pasture vs row crops vs specific crop types (except GLC_FCS30D with 4 types)

## Recommended Datasets

### Top Priority (Very High Relevance):
1. **NPKGRIDS** - Direct link to nutrient inputs from fertilizer (only gridded option)
2. **Global Human Modification v3** - Comprehensive temporal human impact assessment (1990-2022, 90-300m)
3. **GISD30/GISA** - High-resolution impervious surface dynamics for urbanization (30m, back to 1972)
4. **Global Dam Watch** - Best dam database, harmonized with river networks (41k+ barriers)
5. **GHSL Population** - Most complete population dataset with projections to 2030 (100m)
6. **ERA5-Land** - Comprehensive climate/runoff data for water balance (~11km, 1950-present)

### Secondary Priority (High Relevance):
7. **USDA CDL** (for CONUS) - Detailed crop types including pasture/hay distinction (254 classes, 10-30m)
8. **GLC_FCS30D** (global) - Best global land cover with 4 cropland types + grassland (30m, 1985-2022)
9. **Harmonized Night Time Lights** - Long-term urbanization proxy (1992-2021)
10. **LGRIP30** - Detailed irrigation mapping (water use implications, 30m)
11. **Global Roads (GRIP4)** - Infrastructure density and connectivity (~8km)
12. **Global Mining Areas** - Direct extraction impacts on water quality (21k+ polygons)
13. **WCS Human Impact Index** - Multi-driver impact assessment
14. **Copernicus/SRTM DEM** - Topographic controls (30m global)

## Data Gaps Identified

- **Wastewater treatment/discharge**: No global gridded datasets
- **Road salt application**: No direct datasets (could derive from road density + climate zones)
- **Point-source industrial pollution**: Facility-level discharge data not available
- **Livestock in GEE**: GLW3 available externally but requires manual import to GEE
- **Aquaculture facilities**: Limited global coverage
- **Septic systems**: No global density/usage data
- **Detailed pesticide application**: Not available at global scale (only fertilizer via NPKGRIDS)
- **Global crop types**: Most datasets binary cropland/non-cropland; GLC_FCS30D has 4 types but not specific crops
- **Pasture vs row crops globally**: Only available regionally (CONUS, Canada, Europe)

## Code Examples

Access in Google Earth Engine:
```javascript
// Population
var pop = ee.ImageCollection('JRC/GHSL/P2023A/GHS_POP');

// Dams
var dams = ee.FeatureCollection("projects/sat-io/open-datasets/GDW/GDW_BARRIERS_V1_0");
var reservoirs = ee.FeatureCollection("projects/sat-io/open-datasets/GDW/GDW_RESERVOIRS_V1_0");

// Fertilizer
var npk = ee.ImageCollection("projects/sat-io/open-datasets/NPKGRIDS");

// Human modification
var ghm = ee.Image('CSP/HM/GlobalHumanModification');
var ghm_v3 = ee.ImageCollection("projects/sat-io/open-datasets/ghm-v3");

// Impervious surfaces
var gisd30 = ee.Image("projects/sat-io/open-datasets/GISD30_1985_2020");
var gisa = ee.ImageCollection("projects/sat-io/open-datasets/GISA_1972_2021");

// Roads (by region)
var roads_africa = ee.FeatureCollection("projects/sat-io/open-datasets/GRIP4/Africa");
var roads_namerica = ee.FeatureCollection("projects/sat-io/open-datasets/GRIP4/North-America");

// Mining
var mining = ee.FeatureCollection("projects/sat-io/open-datasets/global-mining/global_mining_polygons");

// Nighttime lights (DMSP-OLS)
var ntl = ee.ImageCollection('NOAA/DMSP-OLS/NIGHTTIME_LIGHTS');

// Settlement footprint
var wsf2019 = ee.ImageCollection("projects/sat-io/open-datasets/WSF/WSF_2019");

// Agriculture - Global
var cropland_global = ee.ImageCollection("projects/sat-io/open-datasets/gcep30");
var irrigated = ee.ImageCollection("projects/sat-io/open-datasets/lgrip30");
var glc_fcs = ee.ImageCollection("projects/sat-io/open-datasets/GLC-FCS30D/annual");

// Agriculture - Regional (detailed crop types)
var cdl_usa = ee.ImageCollection('USDA/NASS/CDL'); // CONUS - 254 classes
var aafc_canada = ee.ImageCollection('AAFC/ACI'); // Canada - 40+ crops

// Climate
var era5_hourly = ee.ImageCollection('ECMWF/ERA5_LAND/HOURLY');
var era5_daily = ee.ImageCollection('ECMWF/ERA5_LAND/DAILY_AGGR');

// Topography
var srtm = ee.Image('USGS/SRTMGL1_003');
var copernicus_dem = ee.Image('COPERNICUS/DEM/GLO30');

// Impervious - CONUS
var nlcd = ee.ImageCollection('USGS/NLCD_RELEASES/2021_REL/NLCD');
```

---

**Last Updated:** 2026-01-22
**Researcher:** Sidney Bush

## Sources

### Population & Demographics
- [GEE Population Datasets](https://developers.google.com/earth-engine/datasets/tags/population)
- [GHSL Population Data Catalog](https://developers.google.com/earth-engine/datasets/catalog/JRC_GHSL_P2023A_GHS_POP)

### Water Infrastructure
- [Global Dam Watch Database](https://gee-community-catalog.org/projects/gdw/)
- [GOODD Database](https://gee-community-catalog.org/projects/goodd/)
- [Global Dam Tracker](https://gee-community-catalog.org/projects/gdat/)

### Agriculture & Fertilizer
- [GEE Agriculture Datasets](https://developers.google.com/earth-engine/datasets/tags/agriculture)
- [NPKGRIDS Fertilizer Data](https://gee-community-catalog.org/projects/npk/)
- [USDA NASS CDL](https://developers.google.com/earth-engine/datasets/catalog/USDA_NASS_CDL)
- [Canada AAFC ACI](https://developers.google.com/earth-engine/datasets/catalog/AAFC_ACI)
- [EUCROPMAP](https://developers.google.com/earth-engine/datasets/catalog/JRC_D5_EUCROPMAP_V1)
- [GLC_FCS30D](https://gee-community-catalog.org/projects/glc_fcs/)

### Human Footprint & Modification
- [Global Human Modification](https://developers.google.com/earth-engine/datasets/catalog/CSP_HM_GlobalHumanModification)
- [Global Human Modification v3](https://gee-community-catalog.org/projects/ghm-v3/)
- [World Settlement Footprint](https://gee-community-catalog.org/projects/wsf/)

### Roads & Infrastructure
- [Global Roads Inventory Project](https://gee-community-catalog.org/projects/grip/)
- [Microsoft Bing Global Mined Roads](https://gee-community-catalog.org/projects/msroads/)

### Nighttime Lights
- [GEE Nighttime Lights Datasets](https://developers.google.com/earth-engine/datasets/tags/nighttime)
- [Harmonized Global Night Time Lights](https://gee-community-catalog.org/projects/hntl/)

### Urban & Impervious Surfaces
- [GISD30 Dataset](https://gee-community-catalog.org/projects/gisd30/)
- [GISA Dataset](https://gee-community-catalog.org/projects/gisa/)
- [NLCD](https://developers.google.com/earth-engine/datasets/catalog/USGS_NLCD_RELEASES_2021_REL_NLCD)

### Mining & Extraction
- [Global Mining Areas](https://gee-community-catalog.org/projects/global_mining/)
- [Global Mining Footprints](https://gee-community-catalog.org/projects/global-mining/)

### Climate
- [ERA5-Land](https://developers.google.com/earth-engine/datasets/catalog/ECMWF_ERA5_LAND_HOURLY)

### Topography
- [SRTM DEM](https://developers.google.com/earth-engine/datasets/catalog/USGS_SRTMGL1_003)
- [Copernicus DEM](https://developers.google.com/earth-engine/datasets/catalog/COPERNICUS_DEM_GLO30)

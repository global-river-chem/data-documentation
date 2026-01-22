# Google Earth Engine Human Impact Datasets

Research findings for human impact datasets available on Google Earth Engine relevant to river chemistry analysis.

## Dataset Inventory

### Population Datasets

| Dataset Name | GEE Asset ID | Description | Spatial Coverage | Temporal Coverage | Resolution | Key Variables | Status |
|--------------|--------------|-------------|------------------|-------------------|------------|---------------|--------|
| GHSL Population (P2023A) | `JRC/GHSL/P2023A/GHS_POP` | Global population distribution and density | Global | 1975-2030 (5-yr intervals) | 100m | Population count, density | High relevance |
| WorldPop Global Project | `WorldPop/GP/100m/pop` | Census-disaggregated population counts | Global | Annual, recent years | 100m | Residential population | High relevance |
| WorldPop Age/Sex | `WorldPop/GP/100m/pop_age_sex` | Age and sex structure of population | Global | Annual, recent years | 100m | Population by age/sex | Medium relevance |
| GPWv4.11 Population Count | `CIESIN/GPWv411/GPW_Population_Count` | Gridded population of the world | Global | 2000, 2005, 2010, 2015, 2020 | ~1km (30 arc-sec) | Population count | High relevance |
| GPWv4.11 Population Density | `CIESIN/GPWv411/GPW_Population_Density` | Population density grid | Global | 2000, 2005, 2010, 2015, 2020 | ~1km (30 arc-sec) | People per km² | High relevance |

### Dams and Reservoirs

| Dataset Name | GEE Asset ID | Description | Spatial Coverage | Temporal Coverage | Resolution | Key Variables | Status |
|--------------|--------------|-------------|------------------|-------------------|------------|---------------|--------|
| Global Dam Watch (GDW) | `projects/sat-io/open-datasets/GDW/GDW_BARRIERS_V1_0` | Comprehensive river barriers database | Global | Current (41,145 barriers) | Vector points | Dam location, attributes | High relevance |
| GDW Reservoirs | `projects/sat-io/open-datasets/GDW/GDW_RESERVOIRS_V1_0` | Associated reservoir polygons | Global | Current (35,295 reservoirs) | Vector polygons | Reservoir area, volume | High relevance |
| GOODD Dams | `projects/sat-io/open-datasets/GOODD/GOOD2_dams` | Georeferenced dams database | Global | Current (38,000+ dams) | Vector points | Dam attributes | High relevance |
| GOODD Catchments | `projects/sat-io/open-datasets/GOODD/GOOD2_catchments` | Dam catchment areas | Global | Current | Vector polygons | Catchment area | High relevance |
| Global Dam Tracker (GDAT) | Community catalog | Dams with detailed attributes | Global | 1990s-2020s | Vector points | Height, capacity, purpose | High relevance |

### Agriculture and Cropland

| Dataset Name | GEE Asset ID | Description | Spatial Coverage | Temporal Coverage | Resolution | Key Variables | Status |
|--------------|--------------|-------------|------------------|-------------------|------------|---------------|--------|
| GFSAD1000 Cropland | `USGS/GFSAD1000_V1` | Global cropland extent | Global | ~2010 (2007-2012 data) | 1km | Cropland/non-cropland | Medium relevance |
| GCEP30 Cropland Extent | `projects/sat-io/open-datasets/gcep30` | High-res cropland mapping | Global | ~2015 | 30m | Cropland extent | High relevance |
| LGRIP30 Irrigated/Rainfed | `projects/sat-io/open-datasets/lgrip30` | Irrigated vs rainfed cropland | Global | 2014-2017 (nominal 2015) | 30m | Irrigation type | High relevance |
| GCI30 Cropping Intensity | `projects/sat-io/open-datasets/gci30` | Cropping intensity/frequency | Global | Recent | 30m | Crop frequency | Medium relevance |

### Fertilizer Application

| Dataset Name | GEE Asset ID | Description | Spatial Coverage | Temporal Coverage | Resolution | Key Variables | Status |
|--------------|--------------|-------------|------------------|-------------------|------------|---------------|--------|
| NPKGRIDS | `projects/sat-io/open-datasets/NPKGRIDS` | N, P, K fertilizer application rates | Global | 2015-2020 (circa 2020) | 0.05° (~5.6km) | N, P₂O₅, K₂O by crop | Very high relevance |
| Global Fertilizer by Crop | Community catalog CSV | Fertilizer usage by crop/country | Global | 2017-18 period | Country/crop level | NPK usage statistics | Medium relevance |

### Human Footprint and Modification

| Dataset Name | GEE Asset ID | Description | Spatial Coverage | Temporal Coverage | Resolution | Key Variables | Status |
|--------------|--------------|-------------|------------------|-------------------|------------|---------------|--------|
| Global Human Modification | `CSP/HM/GlobalHumanModification` | Cumulative human modification | Global (terrestrial) | 2016 | 1km | Modification index (0-1) | Very high relevance |
| Global Human Modification v3 | `projects/sat-io/open-datasets/ghm-v3` | Temporal human modification | Global | 1990-2022 (5-yr steps) | 300m & 90m | Modification index | Very high relevance |
| World Settlement Footprint 2015 | `DLR/WSF/WSF2015/v1` | Human settlement extent | Global | 2014-2015 | 10m | Binary settlement mask | High relevance |
| World Settlement Footprint 2019 | `projects/sat-io/open-datasets/WSF/WSF_2019` | Human settlement extent | Global | 2019 | 10m | Binary settlement mask | High relevance |
| WSF Evolution | `projects/sat-io/open-datasets/WSF/WSF_EVO` | Settlement extent time series | Global | 1985-2015 (annual) | 30m | Settlement change | High relevance |
| WCS Human Impact Index | `projects/HII/v1/hii` | Multi-driver human impact | Global | Time series | Variable | Infrastructure, land use, etc. | Very high relevance |

### Roads and Infrastructure

| Dataset Name | GEE Asset ID | Description | Spatial Coverage | Temporal Coverage | Resolution | Key Variables | Status |
|--------------|--------------|-------------|------------------|-------------------|------------|---------------|--------|
| Global Roads Inventory Project (GRIP4) | `projects/sat-io/open-datasets/GRIP4/[region]` | Global roads network by region | Global (by region) | Current | ~8km for density; vectors | Road type, density | High relevance |
| Microsoft Bing Global Mined Roads | Community catalog | AI-extracted roads from imagery | Global (47.8M km) | 2020-2022 | Vector | Road segments | Medium relevance |

### Nighttime Lights (Urbanization Proxy)

| Dataset Name | GEE Asset ID | Description | Spatial Coverage | Temporal Coverage | Resolution | Key Variables | Status |
|--------------|--------------|-------------|------------------|-------------------|------------|---------------|--------|
| DMSP-OLS Nighttime Lights | `NOAA/DMSP-OLS/NIGHTTIME_LIGHTS` | Nighttime visible lights | Global | 1992-2013 | ~1km | Stable lights, avg visible | High relevance |
| VIIRS DNB | Various VIIRS collections | Day/Night Band nighttime lights | Global | 2014-present | ~500m | Radiance | High relevance |
| Harmonized Global Night Time Lights | Community catalog | Harmonized DMSP + VIIRS | Global | 1992-2021 continuous | ~1km/500m | Radiance | Very high relevance |
| Simulated NPP-VIIRS (SVNL) | Community catalog | Extended VIIRS-like time series | Global | 1992-2023 | ~500m (15 arc-sec) | Simulated radiance | High relevance |

### Impervious Surfaces and Urban Extent

| Dataset Name | GEE Asset ID | Description | Spatial Coverage | Temporal Coverage | Resolution | Key Variables | Status |
|--------------|--------------|-------------|------------------|-------------------|------------|---------------|--------|
| GISD30 | `projects/sat-io/open-datasets/GISD30_1985_2020` | Global impervious surface dynamics | Global | 1985-2020 | 30m | Impervious surface area | Very high relevance |
| GISA | `projects/sat-io/open-datasets/GISA_1972_2021` | Global impervious surface area | Global | 1972-2021 | 30m | Impervious surface (93% accuracy) | Very high relevance |
| FROM-GLC/GAIA | `Tsinghua/FROM-GLC/GAIA/v10` | Global artificial impervious area | Global | 1985-2018 | 30m | Year of transition to impervious | High relevance |

### Livestock Density

| Dataset Name | GEE Asset ID | Description | Spatial Coverage | Temporal Coverage | Resolution | Key Variables | Status |
|--------------|--------------|-------------|------------------|-------------------|------------|---------------|--------|
| Gridded Livestock of the World (GLW3) | External (FAO/Harvard) | Cattle, sheep, goats, pigs, poultry | Global | 2010 | ~10km (5 arc-min) | Animals per pixel by species | Medium relevance |
| Global Pasture Watch | `global-pasture-watch/*` collections | Grasslands and grazing lands | Global | 2000-2022 | 30m | Cultivated/natural grassland | Medium relevance |

### Mining and Extraction

| Dataset Name | GEE Asset ID | Description | Spatial Coverage | Temporal Coverage | Resolution | Key Variables | Status |
|--------------|--------------|-------------|------------------|-------------------|------------|---------------|--------|
| Global Mining Areas | `projects/sat-io/open-datasets/global-mining/global_mining_polygons` | Surface mining polygons | Global (21,000+ polygons) | 2000-2017 | Vector polygons | Mining type, area | High relevance |
| Global Mining Footprints | `projects/sat-io/open-datasets/global-mining/global_mining_footprints` | High-resolution mining footprints | Global | Current | High-res | Mining extent | High relevance |

## Notes

### Data Access
- Official GEE catalog datasets: Accessible directly through Earth Engine
- Community catalog datasets: Require specific asset IDs (shown above)
- Most datasets are free for research, education, and nonprofit use
- Some datasets require citation and proper attribution

### Key Observations
- **Population data**: Multiple high-quality options with different temporal coverage and resolution
- **Dams**: Excellent coverage with GDW being most comprehensive and harmonized with river networks
- **Agriculture**: 30m resolution datasets (GCEP30, LGRIP30) offer best detail for cropland analysis
- **Fertilizer**: NPKGRIDS is the only gridded fertilizer application dataset, highly valuable for nutrient analysis
- **Human footprint**: Multiple temporal options allow for change analysis from 1990-2022
- **Urban development**: Three major approaches - nighttime lights (proxy), impervious surfaces (direct), settlement footprints (binary)
- **Roads**: GRIP4 provides global coverage but regional asset structure; Microsoft roads offer recent AI-extracted network
- **Mining**: Comprehensive polygon datasets covering 2000-2017 period with global extent
- **Temporal depth**: Impervious surface data extends back to 1972 (GISA), nighttime lights to 1992

### Missing Data and Gaps
- **Wastewater**: No global gridded wastewater treatment/discharge datasets found in GEE
- **Road salt**: No global road salt application datasets (would require deriving from road density + climate)
- **Point source pollution**: Industrial discharge data not available as global layer
- **Livestock in GEE**: GLW3 available externally but not directly in GEE official catalog (may need manual import)
- **Aquaculture**: Limited global aquaculture facility/production data

## Recommended Datasets

### Top Priority (Very High Relevance):
1. **NPKGRIDS** - Direct link to nutrient inputs from fertilizer
2. **Global Human Modification v3** - Comprehensive temporal human impact assessment (1990-2022)
3. **GISD30/GISA** - High-resolution impervious surface dynamics for urbanization
4. **Global Dam Watch** - Best dam database, harmonized with river networks
5. **GHSL Population** - Most complete population dataset with projections to 2030

### Secondary Priority (High Relevance):
6. **Harmonized Night Time Lights** - Long-term urbanization proxy (1992-2021)
7. **LGRIP30** - Detailed irrigation mapping (water use implications)
8. **Global Roads (GRIP4)** - Infrastructure density and connectivity
9. **Global Mining Areas** - Direct extraction impacts on water quality
10. **WCS Human Impact Index** - Multi-driver impact assessment

## Data Gaps Identified

- **Wastewater treatment/discharge**: No global gridded datasets
- **Road salt application**: No direct datasets (could derive from road density + climate zones)
- **Point-source industrial pollution**: Facility-level discharge data not available
- **Livestock in GEE**: GLW3 available externally but requires manual import to GEE
- **Aquaculture facilities**: Limited global coverage
- **Septic systems**: No global density/usage data
- **Detailed pesticide application**: Not available at global scale (only fertilizer)

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

// Mining
var mining = ee.FeatureCollection("projects/sat-io/open-datasets/global-mining/global_mining_polygons");

// Nighttime lights (DMSP-OLS)
var ntl = ee.ImageCollection('NOAA/DMSP-OLS/NIGHTTIME_LIGHTS');

// Settlement footprint
var wsf2019 = ee.ImageCollection("projects/sat-io/open-datasets/WSF/WSF_2019");
```

---

**Last Updated:** 2026-01-21
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

### Mining & Extraction
- [Global Mining Areas](https://gee-community-catalog.org/projects/global_mining/)
- [Global Mining Footprints](https://gee-community-catalog.org/projects/global-mining/)

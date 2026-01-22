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

### Missing Data
- **Wastewater**: No global gridded wastewater/sewage datasets found in GEE
- **Point source pollution**: Industrial discharge data not available as global layer
- **Detailed livestock**: Some agricultural datasets exist but not comprehensively cataloged here

## Recommended Datasets

### Top Priority (Very High Relevance):
1. **NPKGRIDS** - Direct link to nutrient inputs from fertilizer
2. **Global Human Modification v3** - Comprehensive temporal human impact assessment
3. **Global Dam Watch** - Best dam database, harmonized with river networks
4. **GHSL Population** - Most complete population dataset with projections to 2030

### Secondary Priority (High Relevance):
5. **LGRIP30** - Detailed irrigation mapping (water use implications)
6. **WCS Human Impact Index** - Multi-driver impact assessment
7. **GPWv4.11 Population Density** - Standard population reference
8. **World Settlement Footprint Evolution** - Urban expansion tracking

## Data Gaps Identified

- No global wastewater treatment or discharge datasets
- Limited point-source industrial pollution data
- Livestock density data not comprehensively available

## Code Examples

Access in Google Earth Engine:
```javascript
// Population
var pop = ee.ImageCollection('JRC/GHSL/P2023A/GHS_POP');

// Dams
var dams = ee.FeatureCollection("projects/sat-io/open-datasets/GDW/GDW_BARRIERS_V1_0");

// Fertilizer
var npk = ee.ImageCollection("projects/sat-io/open-datasets/NPKGRIDS");

// Human modification
var ghm = ee.Image('CSP/HM/GlobalHumanModification');
```

---

**Last Updated:** 2026-01-21
**Researcher:** Sidney Bush

## Sources

- [GEE Population Datasets](https://developers.google.com/earth-engine/datasets/tags/population)
- [Global Dam Watch Database](https://gee-community-catalog.org/projects/gdw/)
- [GOODD Database](https://gee-community-catalog.org/projects/goodd/)
- [Global Dam Tracker](https://gee-community-catalog.org/projects/gdat/)
- [GEE Agriculture Datasets](https://developers.google.com/earth-engine/datasets/tags/agriculture)
- [NPKGRIDS Fertilizer Data](https://gee-community-catalog.org/projects/npk/)
- [Global Human Modification](https://developers.google.com/earth-engine/datasets/catalog/CSP_HM_GlobalHumanModification)
- [Global Human Modification v3](https://gee-community-catalog.org/projects/ghm-v3/)
- [World Settlement Footprint](https://gee-community-catalog.org/projects/wsf/)

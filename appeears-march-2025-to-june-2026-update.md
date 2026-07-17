# AppEEARS Spatial Data: March 2025 to June 2026 Update

Date checked: July 1, 2026

This note tracks the main differences between the March 2025 spatial extraction file and the June 2026 spatial extraction file.

## Files Compared

- March 2025 wide file: `all-data_si-extract_2_20250325.csv`
- June 2026 wide file: `all-data_si-extract_3_20260629.csv`

Shared copies are in the
[Google Drive data release folder](https://drive.google.com/drive/folders/1zF_Itljwn0bUWSTHEkwkMDyNOiKPXRF1).

## Main Changes

- The March 2025 wide file has 570 rows and 497 unique `LTER + Stream_Name` sites.
- The June 2026 wide file has 543 rows and 543 unique `LTER + Stream_Name` sites.
- The checked June 2026 new-site file has 65 rows with spatial data. A raw comparison finds 70 new rows, but 5 of those are MCM rows that are not being used for this spatial-data handoff.
- The June 2026 wide file adds 16 columns:
  - `Stream_ID`
  - `hydrosheds_used`
  - `drainage_area`
  - `drainage_area_source`
  - `RBI`
  - `RCS`
  - `land_Bare`
  - `land_Cropland`
  - `land_Forest`
  - `land_Grassland_Shrubland`
  - `land_Ice_Snow`
  - `land_Impervious`
  - `land_Salt_Water`
  - `land_Tidal_Wetland`
  - `land_Water`
  - `land_Wetland_Marsh`

## Years Covered

In the June 2026 wide file:

| Variable group | Years represented |
|---|---|
| snow | 2002-2025 |
| greenup | 2001-2023 |
| evapotrans | 2001-2023 |
| npp | 2001-2024 |
| temp | 1948-2022 |
| precip | 1979-2022 |

The separate annual WRTDS layout is not being kept as a shared spatial-data file. This note tracks the shared wide spatial file.

## GEE/GLC Land Cover

The June 2026 rebuild uses Keira's corrected GEE/GLC V2 file for land cover. This fixed the Canada and Murray-Darling duplicate-row issue.

The selected GEE/GLC product is GLC_FCS30D annual land cover:

`projects/sat-io/open-datasets/GLC-FCS30D/annual`

That product is listed through 2022.

## Site Checks

The main check files are:

- `new-sites_20260629.csv`: 65 new spatial rows after excluding MCM
- `sizer-rerun-sites_20260630.csv`: 27 sites with June spatial data plus overlapping DSi and discharge that may be added to SiZer/CQ work
- `missing-shapefiles-with-chem-discharge_20260630.csv`: 9 sites with chemistry and discharge that still need shapefiles or another spatial-data plan
- `missing-shapefiles-with-chem-only_20260630.csv`: 241 sites with chemistry only that still need shapefiles or another spatial-data plan

The shared new-sites CSV is in the Google Drive data release folder.

## Notes From Final Checks

- `ColoradoAlpine / loch` is not missing spatial data. It is included in the June 2026 spatial file and remains in the SiZer candidate file because it has June spatial data plus overlapping DSi and discharge.
- UMR sites that looked missing in filename-only checks are not missing; their geometries are in `artisanal-shapefiles-2`.
- Murray-Darling HydroSHEDS sites are not listed as missing shapefiles because the June 2026 spatial file marks them as `hydrosheds_used = TRUE`.
- MCM rows are excluded from the new-site and missing-shapefile handoff files.

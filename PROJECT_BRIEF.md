# Project Brief: Health Facility Accessibility in Akure North LGA

## Spatial Question

**Which communities in Akure North Local Government Area (LGA), Ondo State,
Nigeria, are located more than 5 km from the nearest functional public health
facility, and which wards carry the largest share of this underserved
population?**

This matters because Akure North is a semi-urban/rural LGA next to the state
capital, Akure, and health-facility siting decisions there affect real
travel burdens for residents. Answering the question requires combining
point locations of health facilities with settlement locations and the road
network, then measuring distance (straight-line and/or network) from each
settlement to its nearest facility.

## Study Area

- **Name:** Akure North Local Government Area (LGA), Ondo State, Nigeria
- **Headquarters:** Iju/Itaogbolu
- **Approximate centre:** 7.30°N, 5.10°E
- **Area:** ~660 km²
- **Population:** ~131,587 (2006 census; higher today — current-year figures
  will be pulled from GRID3/WorldPop rather than assumed)
- **Context:** Akure North shares a boundary with Akure South (the state
  capital) and Ifedore LGA. It is predominantly agrarian with a mix of small
  towns (Iju, Itaogbolu, Ogbese, Ilado, Isinigbo, Ayede-Ogbese) and
  dispersed rural settlements — a useful contrast to the denser, more
  serviced Akure South.

## Datasets

| # | Dataset | What it provides | Format | Source link |
|---|---------|-------------------|--------|-------------|
| 1 | GRID3 NGA – Health Facilities (v3.0) | Point locations of public/private health facilities, incl. facility type | Point (shapefile/GeoJSON) | https://data.grid3.org/datasets/1b358b47e41244cbaaccb640d9a4bfc9 |
| 2 | GRID3 NGA – Operational LGA Boundaries | Polygon boundary used to clip the study area to Akure North | Polygon | https://data.grid3.org/datasets/GRID3::grid3-nga-operational-lga-boundaries/about |
| 3 | GRID3 NGA – Operational Wards | Ward-level boundaries within the LGA, for reporting results by ward | Polygon | https://data.grid3.org/datasets/GRID3::grid3-nga-operational-wards-v3-0/explore |
| 4 | GRID3 NGA – Settlement Extents | Settlement footprints/points used as a proxy for where population is concentrated | Polygon/point | https://data.grid3.org/datasets/GRID3::grid3-nga-settlement-extents-v3-1/about |
| 5 | OpenStreetMap Nigeria road network (via Geofabrik) | Road network for network-distance/travel-time accessibility analysis | Line (shapefile/PBF) | https://download.geofabrik.de/africa/nigeria.html |

All GRID3 datasets are released under a CC BY 4.0 licence (credit: GRID3,
CIESIN, eHealth Africa, WorldPop). OpenStreetMap data is © OpenStreetMap
contributors, ODbL.

## Planned Method (brief)

1. Clip health facilities, wards, and settlement layers to the Akure North
   LGA boundary.
2. Reproject everything to EPSG:32631 (UTM Zone 31N, appropriate for this
   part of Ondo State) for accurate metric distance measurement.
3. Compute straight-line (and, time permitting, network) distance from each
   settlement to its nearest health facility.
4. Flag settlements beyond a 5 km threshold and summarise the underserved
   population share by ward.
5. Produce a map and summary table of results.

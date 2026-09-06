# Health Facility Accessibility in Akure North LGA

A GIS project examining how far communities in Akure North Local Government
Area, Ondo State, Nigeria, are from the nearest functional public health
facility.

See [`PROJECT_BRIEF.md`](PROJECT_BRIEF.md) for the spatial question, the
study area description, and the full list of datasets with source links.

## Repository Structure

```
.
├── PROJECT_BRIEF.md              # Spatial question, study area, datasets
├── README.md                     # This file
├── requirements.txt              # Python dependencies
├── data/
│   └── akure_north_boundary_approx.geojson   # Rough boundary for demo purposes
├── src/
│   └── plot_study_area.py        # Loads and plots the study area
└── outputs/
    └── study_area_map.png        # Generated map (created by the script)
```

## Setup

1. Clone the repository:
   ```
   git clone https://github.com/<your-username>/akure-north-health-access.git
   cd akure-north-health-access
   ```
2. Install the dependencies:
   ```
   pip install -r requirements.txt
   ```

## Running the Project

From the repository root:
```
python3 src/plot_study_area.py
```
This loads the study area boundary and saves a map to
`outputs/study_area_map.png`.

## Data Note

The boundary shipped in `data/akure_north_boundary_approx.geojson` is a
simplified bounding box, included only so the pipeline runs without
external downloads. It is **not** the authoritative LGA boundary. For real
analysis, download the datasets listed in `PROJECT_BRIEF.md` (GRID3 health
facilities, LGA/ward boundaries, settlement extents, and the OpenStreetMap
road network) and replace the placeholder file.

## Data Licensing

- GRID3 datasets: CC BY 4.0 (credit: GRID3, CIESIN, eHealth Africa, WorldPop)
- OpenStreetMap data: © OpenStreetMap contributors, ODbL

## Status

Project brief complete. Accessibility analysis (distance calculation,
threshold flagging, ward-level summary) is the next stage of work.

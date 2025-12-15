# Hopewell Road LiDAR Analysis

A comprehensive study of LiDAR and satellite evidence for remnants of the ancient Great Hopewell Road between Newark, Ohio, and Chillicothe.
## 🌐 Interactive Map

**[View the Interactive Map →](https://cubap.github.io/Hopewell)** 

Explore LiDAR-detected features on an interactive Leaflet map with satellite imagery, confidence levels, and detailed descriptions.

---


## 🗺️ Overview

The Great Hopewell Road (GHR) is one of North America's most enigmatic prehistoric landscape features—a hypothesized monumental, parallel-walled roadway constructed by the Hopewell culture between approximately 100 BCE and 400 CE. This repository documents the analysis of publicly available LiDAR datasets, satellite imagery, and historical maps to identify and assess remnants of this ancient road.

## 📂 Repository Structure

- **[report/](report/)** - Detailed Markdown analysis with tables of coordinates, descriptions, and confidence levels
  - [Hopewell_Road_LiDAR_Report](report/Hopewell_Road_LiDAR_Report.html) - Complete analysis
  - [figures/](report/figures/) - Annotated maps and comparison imagery
- **[data/](data/)** - Source references, coordinate datasets, and GIS files
  - `lidar_sources.md` - References to USGS 3DEP, OGRIP, and county GIS datasets
  - `coordinates.csv` - Table of key locations with confidence levels
  - `path_projection.geojson` - GeoJSON projection of the possible path
- **[maps/](maps/)** - QGIS project and shapefiles for spatial analysis
  - `annotated_path.qgz` - QGIS project file
  - [shapefiles/](maps/shapefiles/) - Vector data for road segments

## 🔬 Key Findings

The analysis identifies **7 significant locations** where LiDAR and supporting evidence reveal features consistent with the Hopewell Road:

| Location | Coordinates | Confidence |
|----------|-------------|------------|
| Van Voorhis Walls | 40.0580°N, 82.4415°W | Excellent |
| Cynthia Street Park, Heath | 40.0456°N, 82.4332°W | Good |
| South of woodlot, Newark Airport | 40.0372°N, 82.4300°W | Good |
| Near Newark Airport | 40.0320°N, 82.4270°W | Excellent |
| South of James Parkway | 40.0210°N, 82.4200°W | Fair |
| Agricultural field (5350m S of Ramp Creek) | 40.0150°N, 82.4150°W | Good |
| Near Mound City, Chillicothe | 39.3763°N, 82.9919°W | Fair |

**Evidence Summary:**
- **North of Ramp Creek**: 8 Excellent, 3 Good observations (best preservation)
- **South of Ramp Creek**: 0 Excellent, 9 Good, 2 Fair, 1 Poor (more fragmented)

## 🛠️ Methodology

- **LiDAR Processing**: USGS 3DEP and OGRIP datasets (1-meter resolution), processed with QGIS and CloudCompare
- **Visualization**: Hillshade, slope models, Sky View Factor, and Principal Component Analysis
- **Satellite Comparison**: NAIP, Google Earth, and historic aerial photography (1930s–present)
- **Confidence Assessment**: Four-level scale (Excellent, Good, Fair, Poor) based on multi-source corroboration

## 📊 Data Sources

### LiDAR Datasets
- USGS 3D Elevation Program (3DEP)
- Ohio Geographically Referenced Information Program (OGRIP)
- County GIS offices (Licking, Fairfield, Pickaway, Ross)

### Satellite Imagery
- National Agriculture Imagery Program (NAIP)
- Google Earth and Bing Maps
- Historic aerial photographs (1930s, 1980s)

### Historic Maps
- Squier and Davis (1848)
- Salisbury and Salisbury (1862)
- Reeves (1936)

## 🚀 Getting Started

### Explore Online

1. **[Interactive Web Map](https://cubap.github.io/Hopewell)** - Browse locations with satellite/topographic base layers
2. **[GitHub GeoJSON Viewer](data/path_projection.geojson)** - Automatic map rendering on GitHub
3. **[Google Earth (KML)](data/hopewell_road.kml)** - Download and open in Google Earth desktop or mobile

### Work with the Data

1. **[Read the Full Report →](report/Hopewell_Road_LiDAR_Report.md)** - Complete analysis with methodology
2. **Load in GIS Software** - Use `data/path_projection.geojson` in QGIS, ArcGIS, or other tools
3. **Analyze in QGIS** - Open `maps/annotated_path.qgz` for LiDAR overlays and annotations
4. **Reference Coordinates** - Download `data/coordinates.csv` for spreadsheet analysis

## 🗺️ Visualization Options

### Interactive Web Map Features
- Switchable base layers (Streets, Satellite, Topographic)
- Color-coded markers by confidence level
- Clickable popups with feature details
- Projected path overlay
- Mobile-responsive design

### GIS Project Features

The QGIS project includes:
- **LiDAR overlays**: Highlighted linear embankments and parallel walls
- **Satellite comparison layers**: Multi-temporal imagery showing feature persistence
- **Projected path**: Dashed polyline connecting Newark Earthworks → Circleville Works → Chillicothe

### Google Earth KML
- Organized folders for remnants, projected path, and major sites
- Color-coded by confidence level
- Detailed descriptions with report links
- 3D terrain visualization

## 📜 Citation

If you use this data or analysis, please cite:

```
Hopewell Road LiDAR Analysis (2025)
LiDAR-Based Detection and Analysis of the Ancient Hopewell Road: 
Public Datasets, Feature Identification, and Path Projection from Newark to Chillicothe, Ohio
https://github.com/cubap/Hopewell
```

## 📄 License

Open data and analysis are shared under [CC-BY 4.0](LICENSE).

## 🤝 Contributing

We welcome contributions from archaeologists, GIS specialists, local historians, and anyone with relevant data! 

### How to Contribute

- **Report New Features** - Found remnants in LiDAR data? [Use our template →](https://github.com/cubap/Hopewell/issues/new?template=new-feature-report.md)
- **Submit Corrections** - Improved coordinates or data? [Report here →](https://github.com/cubap/Hopewell/issues/new?template=coordinate-correction.md)
- **Share Ground Verification** - Visited a location? [Share your observations →](https://github.com/cubap/Hopewell/issues/new?template=ground-verification-report.md)
- **Add Data Sources** - Know of new LiDAR datasets? [Submit here →](https://github.com/cubap/Hopewell/issues/new?template=data-source-submission.md)

**[Read Full Contribution Guidelines →](CONTRIBUTING.md)**

## 📚 References

See the [full report](report/Hopewell_Road_LiDAR_Report.md) for detailed references to archaeological studies by Lepper, Romain, Burks, Schwarz, and others.

---

**Note**: This is an independent academic analysis using publicly available datasets. The Hopewell Road is a subject of ongoing archaeological research and debate. Ground-truthing and field verification remain essential for confirming interpretations.

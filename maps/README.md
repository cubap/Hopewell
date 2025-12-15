# Maps Directory

This directory contains QGIS projects and shapefiles for visualizing the Hopewell Road analysis.

## Contents

### QGIS Project File
- **annotated_path.qgz** - Complete QGIS project with:
  - LiDAR DEM layers
  - Hillshade visualizations
  - Satellite imagery overlays
  - Projected path polyline
  - Point markers for key locations
  - Historic map georeferencing

### Shapefiles
The `shapefiles/` directory contains vector data:
- **hopewell_segments.shp** - Line features representing identified road segments
- Supporting files (.dbf, .shx, .prj)

## Creating the QGIS Project

To create the annotated map project:

1. **Open QGIS** (version 3.x recommended)

2. **Add Base Layers**:
   - Download LiDAR DEMs from USGS 3DEP or OGRIP
   - Add DEM as raster layer
   - Apply hillshade rendering (multiple azimuths: 315°, 45°, 135°, 225°)

3. **Add Satellite Imagery**:
   - Add XYZ tiles: Google Satellite or Bing Aerial
   - Or download NAIP imagery from USGS Earth Explorer

4. **Import GeoJSON**:
   - Load `../data/path_projection.geojson`
   - Style projected path as dashed red line
   - Style point markers with confidence level colors:
     - Excellent: Dark green
     - Good: Light green
     - Fair: Yellow
     - Poor: Red

5. **Add Historic Maps** (optional):
   - Georeference Squier & Davis (1848) and Salisbury (1862) maps
   - Add as semi-transparent overlay layers

6. **Save Project**:
   - Save as `annotated_path.qgz`

## Exporting Figures

To create publication-quality figures:

1. **Layout Manager**: Create print layouts with:
   - North arrow
   - Scale bar
   - Legend
   - Title and attribution

2. **Export Settings**:
   - Format: PNG (300 dpi) or PDF
   - Save to `../report/figures/`

3. **Suggested Exports**:
   - `lidar_annotations.png` - Overview map with all features
   - `satellite_comparison.png` - Side-by-side LiDAR vs satellite
   - `projected_path_map.png` - Full corridor Newark to Chillicothe

## GIS Analysis Tools

Useful QGIS tools for analysis:
- **Relief Visualization Toolbox**: Sky View Factor, Local Relief Model
- **Profile Tool**: Create elevation cross-sections of embankments
- **Distance Matrix**: Measure spacing between parallel walls
- **Georeferencer**: Align historic maps to modern coordinate systems

## Data Sources

See [../data/lidar_sources.md](../data/lidar_sources.md) for links to:
- USGS 3DEP LiDAR downloads
- OGRIP Ohio datasets
- County GIS portals
- NAIP satellite imagery

## Creating Shapefiles

To create the shapefiles from scratch:

1. **New Shapefile Layer**: Geometry type = LineString, CRS = EPSG:4326
2. **Digitize Features**: Trace road segments from LiDAR and satellite imagery
3. **Add Attributes**:
   - `segment_id` (integer)
   - `confidence` (text: Excellent/Good/Fair/Poor)
   - `source` (text: LiDAR/Satellite/Historic)
   - `notes` (text: Description)
4. **Save**: As `hopewell_segments.shp`

## Coordinate Reference Systems

- **Input Data**: NAD83 State Plane Ohio South/North (EPSG:3735, EPSG:3734)
- **Output GeoJSON**: WGS84 (EPSG:4326)
- **Web Maps**: Web Mercator (EPSG:3857)

## License

Map data and derived products are shared under CC-BY 4.0. Base data sources (USGS, OGRIP) are public domain.

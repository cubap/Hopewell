# Figures Directory

This directory contains annotated maps, comparison imagery, and visualizations for the Hopewell Road LiDAR analysis.

## Planned Figures

### LiDAR Annotations
- **lidar_annotations.png** - Overview map showing all identified features with confidence level color coding
- **van_voorhis_detail.png** - Detailed hillshade of Van Voorhis Walls showing parallel embankments
- **cross_section.png** - Elevation profile across parallel walls

### Satellite Comparisons
- **satellite_comparison.png** - Side-by-side comparison of LiDAR DEM and satellite imagery
- **historic_aerials.png** - Multi-temporal aerial photography (1934, 1988, 2020)
- **infrared_traces.png** - 1988 infrared aerial showing crop marks

### Path Projection
- **projected_path_map.png** - Full corridor map from Newark to Chillicothe
- **corridor_overview.png** - Regional context showing Hopewellian earthworks

### Confidence Mapping
- **confidence_map.png** - Spatial distribution of evidence quality

## Creating Figures

Use the QGIS project at `../maps/annotated_path.qgz` to generate these figures:

1. Open the QGIS project
2. Navigate to **Project > Layouts**
3. Export each layout as PNG (300 dpi) or PDF
4. Save to this directory

## Image Specifications

- **Format**: PNG for web, PDF for print
- **Resolution**: 300 dpi minimum for publications
- **Color Space**: RGB for digital, CMYK for print
- **Attribution**: Include data sources in caption or on figure

## Example Captions

**Figure 1**: LiDAR-derived hillshade showing Van Voorhis Walls segment of the Hopewell Road. Parallel embankments (red arrows) are approximately 50 meters apart with a central depression. Data: USGS 3DEP 1-meter DEM.

**Figure 2**: Comparison of LiDAR DEM (left) and NAIP satellite imagery (right) at Cynthia Street Park, Heath, Ohio. Linear anomalies visible in both datasets (dashed lines) align with projected Hopewell Road path.

**Figure 3**: Projected path of the Great Hopewell Road from Newark Octagon Earthworks to Mound City Group near Chillicothe. Point markers indicate confidence levels: green = Excellent, yellow = Good, orange = Fair.

## License

Figures derived from public domain data (USGS, OGRIP) are shared under CC-BY 4.0. Include attribution when using.

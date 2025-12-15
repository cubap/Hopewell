# LiDAR Data Sources for Hopewell Road Analysis

## Federal and State Programs

### USGS 3D Elevation Program (3DEP)
- **Website**: https://www.usgs.gov/3d-elevation-program
- **Access Portals**:
  - The National Map: https://apps.nationalmap.gov/downloader/
  - LidarExplorer: https://prd-tnm.s3.amazonaws.com/LidarExplorer/index.html
  - EarthExplorer: https://earthexplorer.usgs.gov/
- **Resolution**: 1-meter DEMs, sub-meter in select areas
- **Point Density**: 2–8 points/m²
- **Coverage**: Complete coverage for Licking, Fairfield, Pickaway, and Ross counties
- **Acquisition Dates**: 2015–2020 (most recent high-quality datasets)
- **Format**: LAS/LAZ point clouds, GeoTIFF DEMs
- **Projection**: NAD83 State Plane Ohio South/North (ftUS)

### Ohio Geographically Referenced Information Program (OGRIP)
- **Website**: https://ogrip.oit.ohio.gov/
- **Portal**: Ohio Geospatial Data Portal
- **Resolution**: 1-meter standard, 0.5-meter in county buy-up areas
- **Point Density**: 4–8 points/m² (higher in priority areas)
- **Special Features**: Archaeology-specific DEMs (Digital Feature Models) available for select regions
- **Format**: LAS/LAZ point clouds, GeoTIFF DEMs, classified ground points (ASPRS Class 2)

## County GIS Offices

### Licking County GIS
- **Website**: https://lickingcounty.gov/gis/
- **LiDAR Resolution**: 0.5–1.0 meter
- **Additional Data**: County orthophotos, historic aerials
- **Coverage**: Complete coverage of Newark Earthworks and Van Voorhis Walls

### Fairfield County GIS
- **Website**: https://www.co.fairfield.oh.us/gis/
- **LiDAR Resolution**: 1-meter
- **Coverage**: Southern extent of projected Hopewell Road path

### Pickaway County GIS
- **Website**: https://www.pickaway.org/gis/
- **LiDAR Resolution**: 1-meter
- **Coverage**: Mid-corridor section

### Ross County GIS
- **Website**: https://www.rosscountyohio.gov/
- **LiDAR Resolution**: 1-meter
- **Additional Data**: Proximity to Mound City and High Bank Works earthworks

## Satellite and Aerial Imagery Sources

### National Agriculture Imagery Program (NAIP)
- **Website**: https://www.fsa.usda.gov/programs-and-services/aerial-photography/
- **Resolution**: 1-meter (2010–2015), 0.6-meter (2016–present)
- **Temporal Coverage**: Multi-year datasets (leaf-on conditions)
- **Access**: USGS Earth Explorer, Google Earth Engine

### Google Earth
- **Website**: https://earth.google.com/
- **Historical Imagery**: Available from 2005–present
- **Use**: Multi-temporal analysis, crop mark detection

### Bing Maps
- **Website**: https://www.bing.com/maps/
- **Use**: High-resolution satellite and aerial imagery

### Historic Aerial Photographs
- **USDA Historical Aerial Photography**: 1930s–1980s
- **Access**: USDA APFO, university archives
- **Notable Sets**: 1934 Reeves photography, 1988 infrared aerials

## Processing Software

### QGIS
- **Website**: https://qgis.org/
- **Use**: DEM generation, hillshade, slope analysis, georeferencing historic maps
- **Plugins**: Relief Visualization Toolbox, QGIS2threejs

### CloudCompare
- **Website**: https://www.cloudcompare.org/
- **Use**: LAS/LAZ point cloud processing, cross-section analysis

### RVT (Relief Visualization Toolbox)
- **Repository**: https://github.com/EarthObservation/RVT_py
- **Use**: Sky View Factor, Local Relief Model, Principal Component Analysis

## Data Quality Notes

- **Best Resolution Areas**: Licking County (0.5–1.0 m), Fairfield County (1.0 m)
- **Ground Classification**: ASPRS Class 2 (ground points) filtered for bare-earth DEMs
- **Confidence Mapping**: Based on point density, slope, and vegetation cover
- **Recommended Visualization**: Multi-directional hillshade, SVF, slope models

## Download Instructions

1. **USGS 3DEP**: Use The National Map downloader, select "Elevation Products (3DEP)", filter by "LiDAR Point Cloud" or "1-meter DEM"
2. **OGRIP**: Navigate to Ohio Geospatial Data Portal, search by county name, download LAS/LAZ or DEM products
3. **County GIS**: Contact county GIS offices directly for high-resolution datasets and custom buy-up data

## Data Processing Workflow

1. Download LAS/LAZ point clouds for area of interest
2. Filter ground points (ASPRS Class 2) using QGIS or CloudCompare
3. Generate bare-earth DEM at 0.5–1.0 m resolution
4. Apply visualization techniques (hillshade, slope, SVF)
5. Compare with satellite imagery and historic maps
6. Ground-truth selected features via field survey or geophysical methods

## Citation and Attribution

When using these datasets, cite:
- USGS 3DEP: U.S. Geological Survey 3D Elevation Program
- OGRIP: Ohio Geographically Referenced Information Program
- County GIS: Specify county office and dataset year

## Legal and Ethical Considerations

- Archaeological investigations on public and private lands in Ohio are governed by Section 106 of the National Historic Preservation Act and Ohio Administrative Code 149-1-02
- Obtain appropriate permissions for fieldwork and data collection
- Respect site integrity and confidentiality of sensitive locations

# Contributing to Hopewell Road LiDAR Analysis

Thank you for your interest in contributing to this archaeological research project! This repository documents LiDAR and satellite evidence for the ancient Great Hopewell Road. We welcome contributions from archaeologists, GIS specialists, local historians, and anyone with relevant data or observations.

## 🤝 How to Contribute

### Types of Contributions We Welcome

1. **New LiDAR Findings** - Additional features or segments you've identified
2. **Ground-Truthing Reports** - Field verification of mapped features
3. **Historic Map References** - Georeferenced historic maps or survey data
4. **Coordinate Corrections** - Improvements to existing location data
5. **Satellite Imagery Analysis** - Additional temporal comparisons
6. **Data Source Links** - New or updated LiDAR dataset availability
7. **Documentation Improvements** - Clarifications, typos, formatting

## 📝 Contribution Guidelines

### Before You Start

1. **Search existing issues** to avoid duplicates
2. **Review the [report](report/Hopewell_Road_LiDAR_Report.md)** to understand current findings
3. **Check the [interactive map](https://cubap.github.io/Hopewell)** for existing data

### Reporting New Features

Use the **"New Feature Report"** issue template and include:

- **Coordinates** (WGS84 decimal degrees)
- **Feature Description** (parallel embankments, linear depressions, etc.)
- **Data Sources** (LiDAR dataset, satellite imagery, aerial photos)
- **Confidence Assessment** (Excellent/Good/Fair/Poor)
- **Images/Screenshots** (if possible)
- **Cross-references** (alignment with known segments, historic maps)

#### Example:

```markdown
**Location**: 40.0234°N, 82.4178°W
**Description**: Faint linear depression visible in USGS 3DEP 1m DEM, 
aligned with projected GHR path
**Data Source**: USGS 3DEP (2018), Licking County LiDAR
**Confidence**: Fair
**Notes**: Visible in hillshade but obscured by modern agriculture
```

### Submitting Coordinate Corrections

Use the **"Coordinate Correction"** issue template and provide:

- **Current coordinates** (from data/coordinates.csv)
- **Proposed coordinates** (corrected values)
- **Reason for correction** (better data source, georeferencing error, etc.)
- **Supporting evidence** (dataset reference, measurement method)

### Ground-Truthing Contributions

Field verification is invaluable! Use the **"Ground Verification Report"** template:

- **Location verified** (from existing dataset)
- **Date of visit**
- **Observations** (visible surface features, land use, disturbances)
- **Photos** (if appropriate and permitted)
- **Landowner permission** (confirm permission was obtained)
- **GPS coordinates** (if measured in field)

**Important**: Always obtain landowner permission before entering private property. Respect archaeological site integrity - do not disturb or collect artifacts.

### Adding Data Sources

If you discover new LiDAR datasets or high-resolution imagery:

1. Open an issue titled "New Data Source: [County/Region]"
2. Include:
   - Dataset name and provider
   - Resolution and point density
   - Acquisition date
   - Access URL or portal
   - Coverage area
   - Any restrictions or licensing notes

## 🔄 Pull Request Process

### For Data Contributions

1. **Fork the repository**
2. **Create a feature branch**: `git checkout -b feature/new-location-data`
3. **Make your changes**:
   - Update `data/coordinates.csv` with new rows
   - Add points to `data/path_projection.geojson`
   - Document sources in `data/lidar_sources.md`
4. **Test the map**: Open `index.html` locally to verify GeoJSON renders correctly
5. **Commit with clear messages**: `git commit -m "Add Van Buren linear feature (Fair confidence)"`
6. **Push and create PR**: Include detailed description

### For Documentation

1. Fork and branch as above
2. Edit Markdown files with corrections or additions
3. Preview locally to check formatting
4. Submit PR with description of changes

### Pull Request Checklist

- [ ] Coordinates are in WGS84 decimal degrees
- [ ] Confidence level assigned (Excellent/Good/Fair/Poor)
- [ ] Data sources documented
- [ ] GeoJSON syntax validated (use [geojson.io](https://geojson.io) or similar)
- [ ] CSV format maintained (no extra columns without discussion)
- [ ] Commit messages are clear and descriptive
- [ ] PR description explains rationale for changes

## 📊 Data Standards

### Coordinate Format

- **System**: WGS84 (EPSG:4326)
- **Format**: Decimal degrees
- **Precision**: 4 decimal places (~11 meters)
- **Example**: `40.0580°N, 82.4415°W` or `40.0580, -82.4415`

### Confidence Levels

| Level | Criteria |
|-------|----------|
| **Excellent** | Clear parallel embankments, multiple data sources, historic map confirmation |
| **Good** | Strong linear anomalies, LiDAR + at least one other dataset, aligned with projected path |
| **Fair** | Subtle features, possible disturbance, limited corroboration |
| **Poor** | Weak, discontinuous, heavily altered, or ambiguous features |

### Feature Descriptions

Be specific and objective:
- ✅ "Parallel embankments 45m apart, 0.4m high, visible in 2018 LiDAR hillshade"
- ❌ "Looks like it might be the road"

## 🗺️ GeoJSON Contribution Format

When adding features to `path_projection.geojson`:

```json
{
  "type": "Feature",
  "properties": {
    "name": "Location Name",
    "confidence": "Good",
    "feature_type": "Parallel embankments"
  },
  "geometry": {
    "type": "Point",
    "coordinates": [-82.4415, 40.0580]
  }
}
```

Validate your GeoJSON before submitting:
- [geojson.io](https://geojson.io)
- [GeoJSONLint](https://geojsonlint.com/)

## 🔬 Scientific Rigor

This project values:
- **Reproducibility**: Document data sources and methods
- **Objectivity**: Distinguish observation from interpretation
- **Transparency**: Acknowledge uncertainties and limitations
- **Collaboration**: Engage respectfully with other contributors

## 🚫 What Not to Contribute

- **Exact locations of sensitive sites** (coordinate precision may be reduced for protection)
- **Copyrighted maps or imagery** (unless properly licensed or public domain)
- **Speculation without data** (interpretations should be supported by evidence)
- **Trespassing reports** (ensure legal access to properties)

## 📜 Legal and Ethical Considerations

- All data contributions are shared under **CC-BY 4.0** license
- Archaeological sites in Ohio are protected under state and federal law
- Obtain appropriate permissions for fieldwork
- Respect tribal consultation processes for culturally significant sites
- Do not disturb, collect, or remove artifacts

## 💬 Communication

- **GitHub Issues**: For feature reports, corrections, and discussion
- **Pull Requests**: For data and documentation changes
- **Discussions**: For broader topics, research questions, and collaboration

## 🙏 Acknowledgments

Contributors will be acknowledged in:
- Repository contributors list (automatic via GitHub)
- Future publications derived from this dataset (with permission)
- The community contributors section (if we create one)

## 📚 Resources

- [Full Report](report/Hopewell_Road_LiDAR_Report.md)
- [Interactive Map](https://cubap.github.io/Hopewell)
- [USGS 3DEP Portal](https://apps.nationalmap.gov/downloader/)
- [OGRIP Data Portal](https://ogrip.oit.ohio.gov/)
- [Ohio History Connection](https://www.ohiohistory.org/)

## Questions?

Open an issue with the "Question" label, and we'll help you get started!

---

Thank you for helping preserve and document this remarkable piece of North American prehistory! 🏛️

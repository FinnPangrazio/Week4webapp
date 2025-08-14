# Melbourne NDVI Web App

This web app allows users to explore the NDVI (Normalized Difference Vegetation Index) across the north, south, east, and west localities of Melbourne. It provides interactive mapping, statistics per locality, and easy export options.

---

## Features

### Explore NDVI
- Select an SA4 (a statistical area in Melbourne)
- Visualize NDVI on the map
- Highlight boundaries of the selected locality

### Export Options
- Download NDVI raster as GeoTIFF
- Export per-SA2 NDVI statistics as CSV

### User Interface
- Dropdown menu for selecting SA4
- Buttons for running NDVI calculation and exporting data
- Interactive map display

---

## Usage

1. Open the web app.
2. Select the SA4 region of interest (north, south, east, or west Melbourne).
3. Click **Run NDVI** to generate the NDVI map.
4. Export results:
   - Click **Export NDVI GeoTIFF (SA4)** to download the raster.
   - Click **Export NDVI Stats CSV (SA2s within SA4)** to download the statistics.

---

## Technologies Used

- [Google Earth Engine](https://earthengine.google.com/) for satellite imagery and NDVI calculation
- JavaScript for web app interface and functionality
- GEE UI components (`ui.Panel`, `ui.Button`, `ui.Select`, etc.)

---

## Example Code

Inline code example: `calcNDVI(image)`

Block of code example:

```javascript
function calcNDVI(img){
  return img.normalizedDifference(['B8','B4']).rename('NDVI');

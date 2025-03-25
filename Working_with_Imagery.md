# Working with Imagery 

## Types of Files

- COG
- OGC CoverageJSON

## Web Image Service

- ArcGIS Image Services
- OGC Web Coverage Services

## ArcGIS Web Imagery Layer Items

- Dynamic Imagery
- Tiled Imagery
- WCS Imagery

## Understand the Imagery

### Dynamic Imagery

- On-demand processed at the server  
  - Resample, reproject, render, query, identify pixel value.
- Single Image / a collection of images  
  - ArcGIS Dynamic Imagery Layer Item, ArcGIS dynamic Image service, OGC WCS…
- Dynamic imagery works by sending a bbox and spatial reference and returns an image.
- Could we not tile things out sometimes?

### Tiled Imagery

- Static tile-based images processed at client
- More than just jpeg/png map tiles  
  - Raster tiles (including transposed tiles): LERC2D, JPEG Plus, JPGPNG
- Single Image as tile cache  
  - ArcGIS tiled imagery layer item, ArcGIS Cached image service, COG

## Imagery Layer Types

### Imagery Layer -- is dynamic

- Displays image with server-side pixel processing and rendering
- Reproject at server-side to align with base map
- Get raster info
- Get legend
- View and query footprint attributes
- Identify pixel values and other raster attributes.
- Dynamically compute statistics and histograms
- Measure distance/area/volume in 2D/3D
- Multidimensional and dynamic mosaicking support.

### Imagery Tile Layer -- is tiled

- Interact with image server's tile API/image file directory
- Display image with client-side pixel processing and rendering  
  - Local/focal raster functions
  - Reproject at client-side to align with base map
  - Identify pixel values and other raster attributes  
    - Raw/processed  
    - Get basic raster info  
    - Get legend
- Bigger deep dive…  
  - Can get `serviceRasterInfo` property to describe the raster
  - Can use different renderers in web maps to show different bands, etc. of the imagery.
  - Can define raster functions and chain them together. See [`esri/layers/support/RasterFunction`](https://developers.arcgis.com/javascript/) and `rasterFunctionUtils`.

### WCS Layer

- Interact with WCS API
- Display coverage/image
- Reproject client-side or server-side
- Get basic raster info
- Identify pixel values
- Multidimensional image support
- `wcsUtils` (`esri/layers/ogc/wcsUtils`)  
  - Coverage names/types  
  - Versions

### Additional Notes

- **Dynamic Imagery Layer** has the ability to mosaic and can use mosaic rules to determine which image should display on top.  
  - Could we use something like this in Vexcel/GeoServer idea?
- **Layers can have multidimensional data** (time, elevation, etc).
- **Pixel fetching**  
  - Fetch a pixel block after being processed by the server.

## Demo

[Elevation Analysis](https://developers.arcgis.com/javascript/latest/sample-code/elevation-analysis/)

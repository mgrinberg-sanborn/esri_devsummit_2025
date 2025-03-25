## 3D Web Apps in ArcGIS

- **Custom Code (SDK for JavaScript)** but lots of other apps…ArcGIS GeoBIM, Experience Builder, ArcGIS Urban, 360 VR, Storymaps

### Core Concepts: Getting Started in 3D

- **Best resources for getting started are the samples:**
  - [ArcGIS Sample Code: Analysis Viewshed](https://developers.arcgis.com/javascript/latest/sample-code/analysis-viewshed/)
  - Samples also have a sandbox where you can refresh (CodePen/Sandbox)
  - Search "3D" to look through all the samples

### 3D Visualization and Data
#### What does it take to build a 3D app?

1. Initialize the ESRI JavaScript API and CSS
2. Import the modules (`npm install @arcgis/core`)
3. Call the map component
4. Call the sceneview component

#### Key 3D Concepts to Understand:

- **Elevation**
  - Add elevation by including a `ground` tag in the map component. The `ground` tag acts like a basemap.  
  - `"world-elevation"` is the most common one. Bathymetry is also used for depth data.
  - 3D scenes can exist without elevation, but it's commonly used to reflect elevation.

- **3D Basemaps**
  - Similar to 2D basemaps but include 3D building data, trees, etc.

- **Environmental Factors**
  - Flooding / Weather / Cloud Cover
  - Ability to turn off atmosphere/stars

- **Symbols**
  - Flat and volumetric symbology for 2D and 3D data

- **Scene Layers**
  - Time-enabled scene layers work similarly to time-enabled feature layers.
  - **3D Object Layer**: Allows editing the feature layer behind the scenes, reflecting edits in the cached scene layer. If the scene layer is present, you can use `applyEdits` on it.

### 3D Editing

- Supports **3D Object Feature Service** for modifications.

### 3D Analysis

- **Line of Sight Analysis** – Can you see certain things from a specific point?
- **Measurement Tool** – Supports measuring lines, areas of polygons.
- **Observer**
- **Viewshed Analysis** – Helps visualize the physical view in the scene.

### Collaboration

- **Catalog Layer** – Centralized reference service without needing to add the service layer.
- Web scenes can be edited directly from the **Scene Viewer**.

### Demo: Custom 3D Web App for Urban Planning

- **"Participatory Planning"** – Example of a custom web app for urban development  
  - [Create Your Next Neighborhood in 3D](https://www.esri.com/arcgis-blog/products/js-api-arcgis/3d-gis/create-your-next-neighborhood-in-3d/)


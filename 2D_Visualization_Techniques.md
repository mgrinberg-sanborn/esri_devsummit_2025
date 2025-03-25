## What Can We Visualize?

- **PictureMakerSymbol**
- **PictureFillSymbols**  
  - Can use GIFs, SVGs, or hatch fill symbols within polygons.

## CIMSymbol - Cartographic Information Model Symbol

- A standard for symbology.
- Images should be scalable, which is why SVGs are useful.
- CIM introduces the concept of **symbol layers** (a symbol made up of several layers like our BB clusters).
- Can do **primitive overrides**—on any property you can override with an Arcade expression.

## ESRI Symbol Resources

- ESRI has a **giant list of symbols** that you can use out of the box:  
  [ESRI Web Style Symbols](https://developers.arcgis.com/javascript/latest/visualization/symbols-color-ramps/esri-web-style-symbols-2d)
- You can remove a layer from a **multi-layer CIM symbol**—example: a Parks symbol without the circle.

🔗 **Renderer API Reference:**  
[ESRI Renderers](https://developers.arcgis.com/javascript/latest/api-reference/esri-renderers-Renderer.html)

## Smart Mapping

- Helps determine which colors to pick for a color ramp and what data points make the most sense.
- APIs provide assistance with built-in color ramps.
- **Inefficient for production maps.**
- ⚠️ **"Thick outlines can really crush a map."**

## Renderer vs. Web Map

- **When should you use a renderer vs. a Web Map that you pull in?**  
  - Use a **renderer** when you need more flexibility in styling.  
  - Use a **Web Map** when you want to **interact with the legend** or perform **more complicated tasks**.

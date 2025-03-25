# Dealing with Time Data w/ ESRI Javascript API

## Poll vs. Push

- How frequently does your data change? How quickly do you need updates?  
  - **Layer.refreshInterval = 1** for polling  
  - For pushing, you create a new **StreamLayer** from ArcGIS Velocity or Enterprise Streaming (Websockets).

- Two kinds of updates:
  - **Attribute Updates**
  - **Geometry Updates**

## StreamLayer Basics

- 2D and 3D support
- Track-aware (multiple options can make a line…)
- Define a renderer
- Can pass custom parameters
- Purge options: How to manage stale features?
  - Max observations
  - Max age of features
  - Max number of features
- Same client-side capabilities as other layers.

## StreamLayer Rendering

- All feature/stream data goes through the same pipelines as feature layers.

## Stability & Performance

- **Before:**  
  Difficult for users to dial in the right push rate for a variety of clients.

- **Now:**
  - Stream processing has been overhauled to handle backpressure.
  - Automatic throttling for slow clients.
  - Will attempt to drop obsolete messages first.
  - Use the **update-rate event** to see server and client update rates.
  - Further customize maximum client speed with the new **updateInterval** property.

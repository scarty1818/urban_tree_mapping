🌳 Urban Tree Detection with Remote Sensing & YOLOv8

Automated crown + shadow–aware detection pipeline
Graduate Research — Saint Louis University GIS

Stack: Google Colab · ArcGIS Online · Ultralytics YOLOv8 · rasterio · geopandas

🚀 Overview

This project builds a fully automated deep learning pipeline for urban tree crown detection using:

High-resolution RGB aerial GeoTIFFs

Esri Feature Service (ArcGIS REST) as ground truth

Smart tiling + shadow-aware label generation

YOLOv8 training + GIS-ready prediction exports

✅ Designed for municipal forestry workflows

✅ Shadow-occlusion robust (critical for urban scenes)

✅ Outputs GeoJSON for ArcGIS / QGIS

✅ Extensible for canopy %, carbon, semi-supervised expansion

📦 Pipeline Flow
flowchart LR

| Step | Stage                                       | Notes                                     |
| ---- | ------------------------------------------- | ----------------------------------------- |
| 1    | Aerial RGB GeoTIFFs + ArcGIS Tree Inventory | Inputs                                    |
| 2    | Auto Tiling & Label Generation              | Rect / Circle, shadow-aware               |
| 3    | Balanced Train / Val / Test Split           | Reproducible splits                       |
| 4    | YOLOv8 Training & Evaluation                | mAP, PR curves                            |
| 5    | GIS-Ready Outputs                           | Visual overlays + GeoJSON / ArcGIS export |



📁 Project Structure
| Path                                  | Description                                        |
| ------------------------------------- | -------------------------------------------------- |
| `notebooks/urban_tree_pipeline.ipynb` | Full Colab workflow                                |
| `model_runs/`                         | Auto-saved tiles, labels, weights, metrics         |
| `requirements.txt`                    | rasterio, ultralytics, shapely, geopandas, arcgis… |
| `README.md`                           | You are here                                       |


| Capability                                              | Status    |
| ------------------------------------------------------- | --------- |
| Auto-tiling (640×640, overlap-aware)                    | ✅         |
| Shadow-aware rectangular OR circular labels             | ✅         |
| Live Esri Feature Service ingestion                     | ✅         |
| YOLOv8 training + evaluation (mAP, PR curves, overlays) | ✅         |
| Export predictions to GeoJSON / ArcGIS-ready            | ✅         |
| NDVI masking & shadow suppression                       | 🔄 next   |
| Semi-supervised label validation                        | 🔄 future |

🌍 Real-World Use Cases

Municipal forestry decision support

Urban canopy + heat & flood resilience modeling

Automated storm damage assessment

Climate reporting / ESG automation

👤 Author

Stefany Carty
Graduate Researcher — Saint Louis University GIS
_ Geospatial AI · Remote Sensing · Environmental Security_
🔗 linkedin.com/in/stefanycarty

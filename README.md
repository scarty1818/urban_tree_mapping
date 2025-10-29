🌳 Urban Tree Detection with Remote Sensing & YOLOv8

Automated Crown & Shadow–Aware Tree Detection from High-Resolution Aerial Imagery
Graduate Research — Saint Louis University GIS | Google Colab + ArcGIS + Ultralytics

📌 Overview

This project builds a fully automated urban tree detection pipeline using Google Colab, ArcGIS Online, geospatial tiling, and YOLOv8 deep learning.

It ingests aerial RGB GeoTIFFs and Esri Feature Service tree inventory points, converts them into intelligently labeled object detection tiles (with shadow-aware rectangular or circular bounding boxes), and trains a YOLOv8 model for crown detection in dense urban environments.

✅ Designed for real municipal forestry workflows
✅ Shadow-aware labeling (important for urban imagery)
✅ Can export GeoJSON for GIS visualization in ArcGIS/QGIS
✅ Extensible for canopy cover, carbon estimates, or semi-supervised labeling

| flowchart LR                                                                                     |
|  ----------------------------------------------------------------------------------------------- |
|    A[ArcGIS Feature Service<br/>+ RGB Aerial GeoTIFFs] | --> | B[Auto Tiling<br/>640×640 w/ overlap] |
|   B --> C[Label Generation<br/>Rectangular or Circular] |                                      
|    C --> D[Balanced Train/Val/Test Split]
|    D --> E[YOLOv8 Training & Evaluation]
|    E --> F[Prediction Export<br/>(visual & GeoJSON/ArcGIS-ready)]

urban-tree-detection/
│
├── notebooks/
│   └── urban_tree_pipeline.ipynb   ← full Google Colab workflow
├── model_runs/                     ← auto-created per run (tiles, labels, weights, viz, metrics)
├── README.md                       ← you are here
└── requirements.txt                ← ultralytics, rasterio, shapely, geopandas, arcgis, etc.

| Capability                                                 | Status    |
| ---------------------------------------------------------- | --------- |
| Auto-tiling of aerial imagery (640×640, overlap-aware)     | ✅         |
| Shadow-aware rectangular OR circular bounding boxes        | ✅         |
| Esri Feature Service support (ArcGIS Online REST endpoint) | ✅         |
| YOLOv8 dataset restructuring & training                    | ✅         |
| Evaluation: mAP50/95, PR curves, overlays                  | ✅         |
| Export detections to **GeoJSON (for GIS use)**             | ✅         |
| Planned: NDVI/pre-filtering & shadow masking               | 🔄 next   |
| Planned: Semi-supervised auto-label validation             | 🔄 future |

🎯 Real-World Use Cases

- Municipal forestry workflows
- Urban canopy monitoring & stormwater planning
- Post-storm vegetation damage assessment
- Climate resilience / heat mitigation models

📢 Author

Stefany Carty
Graduate Researcher — Saint Louis University GIS
📍 Geospatial AI | Remote Sensing | Disaster Reponse | Threat Mapping
🔗 linkedin.com/in/stefanycarty

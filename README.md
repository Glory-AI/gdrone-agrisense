# GDrone AgriSense
### Precision Agriculture via UAV Remote Sensing and AI

> Part of the [GDrone Initiative]

---

## Overview

Smallholder farmers across Africa manage over 70% of the region's food production 
with virtually no field-level data. Crop stress, disease, and soil degradation are identified 
only after yield loss is irreversible.

**GDrone AgriSense** is a UAV-based precision agriculture platform that combines multispectral 
remote sensing and lightweight AI to detect crop stress, nutrient deficiency, and disease 
signatures before they become visible; and before they cost a harvest.

---

## The Problem

| Challenge | Scale |
|---|---|
| Smallholder farms with no monitoring data | >70% of Africa's food production |
| Crop stress detected only after damage | avg. 10–14 days too late |
| Fertiliser/pesticide applied uniformly | high input waste, low precision |
| Agricultural extension officers per farmer | critically understaffed |

---

## Proposed System Architecture
UAV Flight Mission

⬇️

Multispectral Imaging (NIR, Red Edge, Thermal, RGB) 

⬇️

Orthomosaic Generation (OpenDroneMap)

⬇️

Index Computation (NDVI, NDRE, Canopy Temp Difference)

⬇️

AI Inference; CNN Stress Classifier

Stress Type (water / nutrient / disease / pest)

Severity Map (field-level, sub-metre resolution)

Intervention Recommendation

⬇️

Farmer-Facing Output (field map + decision)


---

## Remote Sensing Indices

| Index | What It Detects | Bands Used |
|---|---|---|
| NDVI | General crop health / biomass | NIR, Red |
| NDRE | Nitrogen / chlorophyll deficiency | NIR, Red Edge |
| CWSI | Water stress (canopy temperature) | Thermal |
| GNDVI | Early stress, chlorophyll content | NIR, Green |

---

## AI Component

- **Model:** Lightweight CNN trained on multispectral crop imagery
- **Task:** Multi-class stress classification + severity estimation
- **Target deployment:** Edge device (NVIDIA Jetson Nano); no cloud dependency
- **Training data:** Open datasets (PlantVillage, Sentinel-2 crop health, field-collected UAV imagery)
- **Output:** Georeferenced field maps with per-zone recommendations

---

## UAV Platform Experience

The GDrone experience developed through Alpha Flight Club:

- Hexacopter / quadcopter airframe build
- Flight controller: ArduPilot / PX4
- Payload: Camera
- Navigation: Autonomous waypoint missions with consistent altitude hold
- Ground software: Mission Planner / GroundControl

---

## Why Africa

- Smallholder plot sizes suit drone-scale sensing (satellites lack resolution)
- High input costs make precision application directly economical
- Limited connectivity makes edge-AI deployment essential
- Extension services are understaffed; automation multiplies reach

---

## Current Status

| Phase | Status |
|---|---|
| System architecture & research design | 🔄 In Progress |
| Literature review & index selection | 🔄 In Progress |
| UAV platform  | 🔄 In Progress |
| Multispectral data pipeline (simulation) | 🔄 In Progress |
| CNN model — training & validation | 🔄 In Progress |
| Field testing | 🔄 In Progress |
| Farmer-facing output interface | 🔄 In Progress |

---

## Relation to GDrone

GDrone AgriSense is the agricultural extension of the broader GDrone initiative; 
applying the same measurement-driven UAV platform philosophy to food security and 
smallholder farming making crop monitoring system trustworthy.

---

## Fellowship Context

This repository documents the technical foundation of my application to the 
**IAP Precision Applied AI & Remote Sensing Fellowship**, where I propose to develop 
and validate the GDrone AgriSense pipeline;  from multispectral data acquisition 
to edge-AI inference; with direct deployment relevance across African agricultural contexts.

---

## References & Resources

- [GDrone Initiative]
- [OpenDroneMap](https://opendronemap.org) — open-source photogrammetry
- [PlantVillage Dataset](https://plantvillage.psu.edu) — crop disease training data
- [MicaSense RedEdge](https://micasense.com) — multispectral payload reference
- [QGIS](https://qgis.org) — geospatial analysis

---

*Glory Akanbi · OAU Ile-Ife · GDrone Initiative · 2026*
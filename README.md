# Fall 2025, PSTAT231 Final Project: Gaussian Mixture Models

## Overview
This project investigates clustering methods for real-world earthquake data using both probabilistic and density-based approaches. 
Our primary methodological foundation is DBSCAN, following the original KDD 1996 paper 
[*A Density-Based Algorithm for Discovering Clusters in Large Spatial Databases with Noise*](https://www.dbs.ifi.lmu.de/Publikationen/Papers/KDD-96.final.frame.pdf).

To highlight the contrast between density-based and model-based clustering, we additionally apply 
Gaussian Mixture Models (GMMs) as a baseline method. The goal is to compare how these two approaches 
handle spatial earthquake patterns, cluster shapes, and noise.

We analyze global earthquake data obtained from the 
[USGS Earthquake Catalog](https://earthquake.usgs.gov/earthquakes/search/), perform clustering using both DBSCAN and GMM, 
and visualize the resulting seismic clusters to interpret real-world tectonic structure.

The final deliverables include:
- A reproducible R Markdown analysis (`project.Rmd`)
- Replication experiments for the JMLR paper
- An extension experiment using real earthquake data
- Visualizations and discussion of theory vs. practice

---

## Division of Work

### Zifeng Zhan
- **Theory Section (Main Paper: DBSCAN, KDD 1996)**
  - Explain density-based clustering concepts
  - Define Eps-neighborhood, core/border/noise points
  - Describe density-reachability and density-connectivity
  - Summarize DBSCAN algorithm and the k-dist method for parameter selection
  - Discuss why DBSCAN is suitable for spatial datasets such as earthquake epicenters
- **Background (Lightweight GMM overview for comparison)**
  - Provide brief intuition behind Gaussian Mixture Models (GMMs)
  - Explain EM-based clustering at a high level (no detailed derivation needed)
- **Writing**
  - Write Sections 1–2 of the report (DBSCAN theory + brief GMM background)
  - Contribute to the Introduction and Conclusion

### Jasper Luo
- **Dataset Collection & Preprocessing**
  - Retrieve earthquake data from the USGS Earthquake Catalog API
  - Clean and prepare variables (longitude, latitude, depth, magnitude)
- **Main Experiment**
  - Apply DBSCAN to earthquake data
    - Tune parameters (Eps, MinPts) using k-distance plots
    - Identify clusters and noise patterns
    - Generate spatial and scatter visualizations
  - Apply GMM as a baseline clustering method
    - Fit models with different numbers of components
    - Visualize and compare cluster assignments
- **Comparison & Analysis**
  - Compare DBSCAN and GMM in terms of:
    - cluster shape flexibility
    - noise detection
    - sensitivity to density variations
    - ability to represent real seismic structures
- **Writing**
  - Write Sections 3–4 of the report (experiments + GMM vs DBSCAN comparison)
  - Contribute to the Introduction and Conclusion

---

## File Structure

```
project/
│── README.md
│── project.Rmd
│── data/
│ └── earthquakes.csv
│── src/
│ ├── download_usgs_data.R
│ ├── PLACE_HOLDER.R
│ ├── PLACE_HOLDER.R
│ └── PLACE_HOLDER.R
└── figures/
    ├── PLACE_HOLDER.png
    ├── PLACE_HOLDER.png
    └── PLACE_HOLDER.png
```
---

## Reproducibility
All code is written in R and can be executed by knitting `project.Rmd`. 
The USGS data can be downloaded automatically via `src/download_usgs_data.R`.

---

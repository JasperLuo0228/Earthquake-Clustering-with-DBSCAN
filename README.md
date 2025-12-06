# Fall 2025, PSTAT231 Final Project: Gaussian Mixture Models

## Overview
This project investigates Gaussian Mixture Models (GMMs) from both theoretical and computational perspectives. 
We reproduce key results from the JMLR paper [*Optimal Rates for Learning Mixtures of Spherical Gaussians*](https://jmlr.org/papers/v20/18-470.html)
and extend the study by applying GMMs to real-world earthquake data obtained from the 
[USGS Earthquake Catalog](https://earthquake.usgs.gov/earthquakes/search/). 
We additionally compare GMM with DBSCAN, a density-based clustering method.

The final deliverables include:
- A reproducible R Markdown analysis (`project.Rmd`)
- Replication experiments for the JMLR paper
- An extension experiment using real earthquake data
- Visualizations and discussion of theory vs. practice

---

## Division of Work

### Zifeng Zhan
- **Theory Section**
  - Background on Gaussian mixtures
  - EM algorithm derivation
  - Summary of JMLR paper's theoretical contributions
- **Paper Replication**
  - Implement EM for GMM
  - Experiments on separation, sample complexity, estimation error
  - BIC/AIC model selection analysis
  - Generate plots and result summaries
- **Writing**
  - Sections 1–3 of the report (theory + replication)
  - Joint writing of Introduction and Conclusion

### Jasper Luo
- **Dataset Collection & Preprocessing**
  - Retrieve earthquake dataset via USGS API
  - Clean and prepare (longitude, latitude, depth, magnitude)
- **Extension Experiment**
  - Apply GMM to earthquake data
  - Run DBSCAN and tune parameters
  - Compare clustering methods and generate visualizations
- **Writing**
  - Section 4 (extension experiment)
  - Joint writing of Introduction and Conclusion

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

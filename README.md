# Fall 2025, PSTAT231 Final Project: DBSCAN and Earthquake Clustering

## Overview
This project investigates density-based clustering using DBSCAN and applies it to real-world earthquake data. 
Our theoretical foundation is the original KDD 1996 paper 
[*A Density-Based Algorithm for Discovering Clusters in Large Spatial Databases with Noise*](https://www.dbs.ifi.lmu.de/Publikationen/Papers/KDD-96.final.frame.pdf),
which introduced the key concepts of core points, border points, noise points, density-reachability, and density-connectivity.

We first reproduce the main ideas and illustrative examples from the DBSCAN paper using synthetic datasets.  
Then, we apply DBSCAN to global earthquake data obtained from the 
[USGS Earthquake Catalog](https://earthquake.usgs.gov/earthquakes/search/) 
to identify seismic clusters and analyze their spatial patterns.

The final deliverables include:
- A reproducible R Markdown analysis (`project.Rmd`)
- Replication of DBSCAN theory and synthetic examples
- An extension experiment using real earthquake data
- Visualizations and discussion of clustering behavior in theory vs. practice

---

## Division of Work

### **Zifeng Zhan**
- **Theory Section**
  - Explain density-based clustering concepts
  - Define Eps-neighborhood, core/border/noise points
  - Describe density-reachability and density-connectivity
  - Summarize DBSCAN algorithm and the k-dist method for parameter tuning
  - Discuss why DBSCAN is suitable for spatial datasets such as earthquake epicenters
- **Writing**
  - Write Sections 1–2 (theory)
  - Contribute to Introduction and Conclusion

---

### **Jasper Luo**
- **Dataset Collection & Preprocessing**
  - Retrieve earthquake data via the USGS API
  - Clean and prepare variables (longitude, latitude, depth, magnitude)
- **Experiments**
  - Generate synthetic datasets similar to those in the DBSCAN paper
  - Apply DBSCAN to synthetic and real earthquake datasets
  - Tune parameters (Eps, MinPts) using k-distance plots
  - Visualize clusters and noise patterns
- **Writing**
  - Write Section 3 (experiments + results)
  - Contribute to Introduction and Conclusion

---

## File Structure

```
project/
│── README.md
│── project.Rmd
│── data/
│   └── earthquakes.csv
│── src/
│   ├── download_usgs_data.R
│   ├── synthetic_data_db1.R
│   ├── synthetic_data_db2.R
│   ├── synthetic_data_db3.R
│   └── run_dbscan.R
└── figures/
    ├── dbscan_db1.png
    ├── dbscan_db2.png
    ├── dbscan_db3.png
    ├── earthquake_clusters.png
    └── kdist_plot.png
```

---

## Reproducibility
All code is written in R and can be executed by knitting `project.Rmd`.  
The USGS earthquake dataset is automatically downloaded using `src/download_usgs_data.R`.

---

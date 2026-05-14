## Overview

This repository contains the Jupyter notebooks and outputs for my Bachelor Thesis on the TOPIX reform at the University of St. Gallen (HSG). The code builds a pro‑forma post‑reform TOPIX and compares it with the pre‑reform index on benchmark quality, investability, and derivatives suitability.

## Abstract

**TBD**

## How to run

1. Clone the repository.  
2. Create a Python environment with `pandas`, `numpy`, `matplotlib`, `seaborn`, `scipy`, `statsmodels`, and the LSEG / Refinitiv Eikon Python package.  
3. Obtain an LSEG Refinitiv Workspace API key and insert it locally where indicated in `00_data_ingestion.ipynb` (do not commit your real key).  
4. Set `PROJECT_DIR` and `DATA_DIR` to your local paths (for example `PROJECT_DIR = '.'`, `DATA_DIR = './data'`) and create the `data/` folder if it does not exist.  
5. Run the notebooks in order:  
   1. `00_data_ingestion.ipynb`  
   2. `01_hhi.ipynb` → `02_sectoral_distribution.ipynb` → `03_fama_french.ipynb` →  
      `04_amihud.ipynb` → `05_dtt.ipynb` → `06_basket_spread.ipynb` → `07_descriptive_statistics.ipynb`  
6. Licensed LSEG data and raw JPX files are not included and must be re‑created via your own institutional access.

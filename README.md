## Overview

This repository contains the Jupyter notebooks and outputs for my Bachelor Thesis on the TOPIX reform at the University of St. Gallen (HSG). The code builds a pro‑forma post‑reform TOPIX and compares it with the pre‑reform index on benchmark quality, investability, and derivatives suitability.

## Abstract

The ongoing reform of the Tokyo Stock Price Index (TOPIX), executed across two phases between 2022 and 2028, represents the most fundamental redesign of a primary equity benchmark at this scale, combining methodological refinements, tighter eligibility screens, governance-linked criteria, and a deliberate contraction of the constituent universe in a way no prior intervention has matched. Despite the index governing over ¥110 trillion in linked assets, the reform has received no dedicated academic treatment. This thesis contextualises the reform within index design theory and the empirical literature on structural index changes, then constructs a pro-forma index applying the published phase 2 eligibility criteria to the current constituent universe and evaluates it against the pre-reform original across benchmark quality, investability, and derivatives suitability. The results show that the reform delivers meaningful but unevenly distributed improvements. Concentration remains unchanged despite halving the constituent base, while investability improves substantially. At the constituent level, median illiquidity falls 87%, yet aggregate index-level metrics suggest a far more modest improvement, obscuring the true magnitude of the change. Operational replicability also improves meaningfully, with bottleneck stocks falling 14.6% in execution time and halving in number from 99 to 41, directly addressing the constituents that previously posed the greatest execution challenges for institutional investors. The reformed index also exhibits with a moderate sectoral reorientation and a modest large-cap and growth tilt, while basket-level transaction costs tighten only marginally (1.28 bps). Taken together, the reformed TOPIX emerges as a meaningfully more liquid and operationally viable benchmark, though it remains a broad market index rather than a selective premium one. This thesis offers the first integrated academic treatment of the reform, advancing a clearer understanding of the post-reform TOPIX's character and likely properties, and argues that distinguishing between index-level and constituent-level effects is essential both for evaluating this reform and for structural index change analysis more broadly.

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

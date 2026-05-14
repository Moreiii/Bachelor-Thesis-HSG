This repository contains the Jupyter notebooks and exported outputs used for the empirical analysis in my Bachelor Thesis on the TOPIX reform at the University of St. Gallen (HSG). The code reconstructs a pro‑forma post‑reform TOPIX and compares it with the pre‑reform index along benchmark quality, investability, and derivatives‑suitability dimensions, using LSEG Refinitiv Workspace data and official JPX constituent lists.
How to run
Clone the repository.

Create a Python environment with the usual scientific stack (pandas, numpy, matplotlib, seaborn, scipy, statsmodels) and the LSEG / Refinitiv Eikon Python package.

Obtain an LSEG Refinitiv Workspace API key and insert it locally where indicated in 00_data_ingestion.ipynb (do not commit your real key).

Set PROJECT_DIR and DATA_DIR to your local paths (for example PROJECT_DIR = '.', DATA_DIR = './data') and create the data/ folder if it does not exist.

Run the notebooks in order:

00_data_ingestion.ipynb (creates all parquet/CSV files in data/)

01_hhi.ipynb → 02_sectoral_distribution.ipynb → 03_fama_french.ipynb →
04_amihud.ipynb → 05_dtt.ipynb → 06_basket_spread.ipynb → 07_descriptive_statistics.ipynb

Due to licensing, underlying LSEG data and raw JPX files are not included and must be re‑created via your own institutional access.

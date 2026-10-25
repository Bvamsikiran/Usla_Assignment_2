Machine Learning Model Performance Evaluation — Mauna Loa Weekly CO2

Files
- ML_Model_Performance_Mauna_Loa_CO2.ipynb: Google Colab/Jupyter notebook.
- mauna_loa_co2_weekly.csv: original weekly Mauna Loa CO2 observations used by the notebook.

Dataset provenance
The CSV is exported from the statsmodels package's public-domain Mauna Loa Weekly Atmospheric CO2 dataset. The dataset covers March 1958 to December 2001. Missing CO2 values are preserved as blank cells.

Official dataset documentation and citation:
https://www.statsmodels.org/stable/datasets/generated/co2.html
Keeling, C. D., and T. P. Whorf (2004). Atmospheric CO2 concentrations derived from flask air samples at sites in the SIO network. In Trends: A Compendium of Data on Global Change.

Important methodology note
The classification outcome is derived from actual adjacent measurements: whether next week's CO2 reading is greater than this week's reading. The regression outcome is the next week's CO2 concentration. No synthetic observations are generated. The notebook uses a chronological train/test split to avoid shuffling time-series data.

How to use in Colab
1. Upload both the notebook and CSV to your GitHub repository.
2. Open the notebook in Google Colab.
3. Run cells from top to bottom.
4. If the CSV is not found in the Colab runtime, the first data-loading cell prompts you to upload mauna_loa_co2_weekly.csv.

Required libraries: pandas, numpy, scikit-learn, matplotlib. These are normally available in Google Colab.

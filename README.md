# Machine Learning Model Performance Evaluation — Mauna Loa Weekly CO₂

This project evaluates machine-learning models using real-world atmospheric carbon dioxide (CO₂) measurements collected at Mauna Loa Observatory. It is designed for a machine-learning performance metrics assignment and uses a public dataset rather than artificially generated observations.

## Project files

- `ML_Model_Performance_Mauna_Loa_CO2.ipynb` — Google Colab/Jupyter notebook containing the code, evaluation metrics, result tables, and visualizations.
- `mauna_loa_co2_weekly.csv` — weekly Mauna Loa CO₂ observations used by the notebook.

## Dataset

The CSV is based on the public Mauna Loa Weekly Atmospheric CO₂ dataset distributed with `statsmodels`. It covers March 1958 through December 2001. Missing CO₂ readings are preserved as blank values in the CSV; the notebook handles incomplete observations during preparation.

**Dataset documentation:** https://www.statsmodels.org/stable/datasets/generated/co2.html

**Dataset reference:** Keeling, C. D., and T. P. Whorf (2004). *Atmospheric CO₂ concentrations derived from flask air samples at sites in the SIO network.* In *Trends: A Compendium of Data on Global Change*.

## Evaluation metrics

The notebook covers the assignment's requested metrics:

1. Accuracy
2. Confusion matrix
3. Precision and recall
4. Receiver Operating Characteristic (ROC) curve
5. Log-loss
6. Mean Absolute Deviation (MAD) error
7. Coefficient of determination (R²)
8. Distribution of errors using plots

Because these metrics cover both classification and regression, the notebook defines two prediction tasks using the real measurements:

- **Classification:** predict whether the next week's CO₂ reading is higher than the current week's reading.
- **Regression:** predict the next week's CO₂ concentration.

A chronological train/test split is used to respect the time order of the observations. No synthetic samples or artificial target values are created.

## Run in Google Colab

1. Upload the `.ipynb` notebook and `.csv` dataset to your GitHub repository, or download both files to your computer.
2. Open [Google Colab](https://colab.research.google.com/).
3. Upload and open `ML_Model_Performance_Mauna_Loa_CO2.ipynb`.
4. Run the notebook cells from top to bottom.
5. If the dataset is not detected automatically, follow the notebook's prompt to upload `mauna_loa_co2_weekly.csv`.
6. Save or download the executed notebook so its outputs and graphs are included before submitting it.

## Libraries

The notebook uses:

- pandas
- NumPy
- scikit-learn
- Matplotlib

These libraries are generally available in Google Colab.

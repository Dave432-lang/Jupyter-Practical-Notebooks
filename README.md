# Jupyter Practical Notebooks

A collection of hands-on Jupyter practicals for exploring a health-measurements
dataset and practicing introductory regression workflows. The notebooks are
organized to support step-by-step learning, from data inspection through model
evaluation.

## Objectives

- Practice loading and inspecting tabular data with Python.
- Perform data-quality checks and exploratory data analysis (EDA).
- Visualize distributions, relationships, and correlations.
- Build and compare supervised regression models using a repeatable train/test
  split.
- Interpret model metrics and predictions in context.

## Project structure

```text
health-data-analysis/
├── health_data_analysis.ipynb
├── health_model_comparison.ipynb
└── health_measurements_100_observations.xlsx
```

The Excel workbook is the shared input dataset used by both notebooks. Its
observations are synthetic; the exercises are for learning and do not support
medical conclusions.

## Practical exercises

### Exploratory data analysis

[`health_data_analysis.ipynb`](health-data-analysis/health_data_analysis.ipynb)
walks through loading the workbook, inspecting its structure, checking data
quality, calculating descriptive statistics, plotting distributions and
relationships, reviewing correlations, and summarizing observations.

### Regression model comparison

[`health_model_comparison.ipynb`](health-data-analysis/health_model_comparison.ipynb)
cleans and explores the data, predicts `Pulse_rate_bpm`, and compares:

- Linear regression
- Random forest regression
- k-nearest neighbors regression (`k=5`)

The notebook uses an 80/20 train/test split with a fixed random seed and
compares results with MAE, RMSE, and R-squared, including actual-versus-predicted
visualizations.

## Tools

- Python 3
- Jupyter Notebook or JupyterLab
- pandas and NumPy for data manipulation
- Matplotlib and Seaborn for visualization
- scikit-learn for regression models and evaluation
- openpyxl for reading the Excel workbook

## Getting started

From the repository root, install the packages and start Jupyter:

```bash
python -m pip install jupyter pandas numpy matplotlib seaborn scikit-learn openpyxl
jupyter lab
```

Open either notebook in `health-data-analysis/` and run its cells in order. Keep
`health_measurements_100_observations.xlsx` alongside the notebooks so their
relative data paths resolve.

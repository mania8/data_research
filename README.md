# Correlating Working Time Duration and Productivity in EU and OECD Countries

This experiment aims to explore the connection between the average annual hours worked per employee and labour productivity (GDP per hour worked) across selected European and OECD countries for the period 2014-2024.

## Prerequisites

Prior to running the experiment make sure that the following folders exist:

* `data` - Folder to store the datasets (input and processed)
* `notebooks` - Folder containing the Jupyter Notebooks for analysis
* `results` - Target folder for the generated report and correlation plot

## Data Sources

* **Working Time:** Eurostat. (2025). *Hours worked per week of full-time employment* [Table: tps00071]. License: CC BY 4.0. 
  https://ec.europa.eu/eurostat/databrowser/view/tps00071/default/table
* **Productivity:** OECD. (2025). *Level of GDP per hour worked* [Dataset: Productivity and ULC]. Unit: US Dollars (PPP-adjusted). License: Open Data / CC BY 4.0 compatible.
  https://stats.oecd.org/

The cited datasources have already been added to this repository in the `data` folder.

Follow these instructions if you want to use updated versions of these datasources:

1. Download CSV files to folder `data`
2. Set paths to CSV files in the notebook `notebooks/pearsons.ipynb` (or `analysis.ipynb`) by changing the filename variables.

## Running the code

To run the code in this repository you will need to have access to a machine running `python` (at least version `3.5`) and `pip`.

Run `pip install -r requirements.txt` to install the required dependencies.

Once the dependencies have been installed, start the jupyter notebook server via `jupyter notebook` (or open in VS Code).

In the `notebooks` folder you'll find the following notebook:

### pearsons.ipynb (or analysis.ipynb)

Running this notebook generates a dataset consisting of harmonized working hours and productivity data by preprocessing, filtering, and fusing the data provided by the datasources mentioned above. It then performs a Pearson correlation analysis.

The resulting dataset is located at `data/final_data_for_analysis.csv`

This notebook also generates a plot to visualize correlations between the data points.

The resulting plot is stored at `results/scatter_plot.png`

## Results

The main results, including the statistical interpretation of the correlation coefficient ($r$), are summarized in the report:
`results/statistical_report.pdf`

## License

* **Code:** MIT License
* **Data & Documentation:** Creative Commons Attribution 4.0 International (CC BY 4.0)

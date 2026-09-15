<div align="center">
	<h1>New York City Airbnb Data Analytics</h1>
	<p>Exploratory analysis of Airbnb listing prices, availability, location, and guest engagement across New York City.</p>
</div>

## Overview

This project analyzes New York City Airbnb listings to identify patterns associated with nightly price, annual availability, and customer engagement. The analysis combines data cleaning, exploratory data analysis, visualization, and predictive modeling to produce practical insights for hosts, Airbnb market managers, pricing teams, and business strategy teams.

The project is designed to answer three business questions:

1. Which listing characteristics and locations are associated with price differences?
2. What factors are associated with annual listing availability?
3. How do location, room type, price, and other listing characteristics relate to reviews and guest satisfaction?

## Key Findings

- Average listing prices are relatively consistent across major categorical groups, including room type, neighborhood group, host verification, and cancellation policy.
- Manhattan and Brooklyn listings generally have lower annual availability than listings in outer boroughs, indicating stronger demand in central markets.
- Minimum-stay requirements are associated with changes in annual availability, with longer requirements linked to fewer available days.
- Longitude, latitude, and monthly review activity are among the strongest predictors of annual availability in the Random Forest analysis.
- Higher nightly prices do not appear to produce higher guest ratings.
- Hotel rooms show higher average review volume than several other room types in the analyzed data.

These findings are descriptive and should be interpreted as associations rather than proof of causal relationships.

## Repository Structure

```text
.
├── business_problem.md
├── data/
│   ├── clean_data/
│   │   └── clean_airbnb_listing.csv
│   └── raw_data/
│       └── Airbnb_Open_Data.csv
├── notebooks/
│   └── Airbnb_NYC_Data_Analytics_Data_Obatin_and_Scrubing.ipynb
├── presentation/
├── report/
│   ├── Aibin_listing_Analytical_report.md
│   └── visulization/
└── readme.md
```

## Data

The project uses Airbnb listing data for New York City. The repository contains both the original raw dataset and a cleaned dataset used for analysis:

- `data/raw_data/Airbnb_Open_Data.csv`: source data.
- `data/clean_data/clean_airbnb_listing.csv`: cleaned data prepared for analysis.

The analysis includes listing location, room type, neighborhood group, price, minimum nights, availability, reviews, host attributes, and related listing fields available in the source data.

## Analysis Workflow

The notebook documents the main preparation and analysis workflow:

1. Load and inspect the raw listing data.
2. Identify missing values, inconsistent values, and fields requiring cleaning.
3. Prepare the cleaned dataset for exploratory analysis.
4. Compare prices across categorical and geographic dimensions.
5. Analyze annual availability by borough, room type, reviews, price, and minimum nights.
6. Examine relationships between listing characteristics and guest engagement.
7. Train a Random Forest Regressor to evaluate predictors of annual availability.
8. Export visualizations and summarize the results in the analytical report.

## Documentation and Outputs

- [Business problem](business_problem.md)
- [Analytical report](report/Aibin_listing_Analytical_report.md)
- [Data preparation notebook](notebooks/Airbnb_NYC_Data_Analytics_Data_Obatin_and_Scrubing.ipynb)

The report includes the project conclusions, strategic recommendations, and visualizations generated during the analysis.

## Visualizations

The report references the following visual outputs:

- [Average price bar charts](report/visulization/Bar%20Charts%20Average%20Price.png)
- [Listing location scatterplot](report/visulization/Scatterplot_lan_lat.png)
- [Geographic heatmap](report/visulization/Geographic%20Heatmap.png)
- [Availability analysis](report/visulization/Availability%20by%20Room%20Type%2C%20Neighbourhood%20Group%2C%20Reviews%2C%20Price%2C%20Minimum%20Nights.png)
- [Random Forest feature importances](report/visulization/Feature%20Importances%20in%20Random%20Forest%20Regressor%20for%20predicting%20availability_36.png)
- [Customer engagement analysis](report/visulization/customer_engagement.png)

## Reproducing the Analysis

1. Clone or download this repository.
2. Open the notebook in Jupyter Notebook, JupyterLab, or Visual Studio Code.
3. Install the Python dependencies required by the notebook environment.
4. Run the notebook cells in order to reproduce the cleaning steps, analysis, model, and visualizations.

The notebook is the source of truth for the computational workflow. The cleaned CSV and report are included so that the prepared data and final findings can also be reviewed directly.

## Limitations

- The analysis describes relationships in the available dataset and does not establish causation.
- Reported price and availability patterns may be affected by missing values, outliers, data-entry issues, and the period represented by the source data.
- Results should be refreshed with current listing data before making operational or pricing decisions.

## License

See [LICENSE](LICENSE) for the licensing information associated with this repository.

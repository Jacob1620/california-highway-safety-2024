# California Highway Safety, 2024

A county-level analysis of highway safety patterns across California's 58 counties using **R** and **ArcGIS Pro**. The project compares absolute crash burden with exposure-adjusted crash and fatality rates to examine how highway-safety patterns change when vehicle travel is taken into account.

The analysis uses 2024 California state highway crash data from the **California Department of Transportation (Caltrans)**, supplemented with county-level pedestrian and bicycle fatality data. County geography is based on the **U.S. Census Bureau's 2024 TIGER/Line county boundaries**.

## Key Findings

- **Absolute burden and exposure-adjusted rates highlight different counties.** Los Angeles recorded 41,235 crashes and 218 fatalities, but its exposure-adjusted rates were substantially lower than those of several lower-volume counties.
- **Trinity County had the highest total crash rate** at 1.813 crashes per million vehicle miles traveled (VMT), despite recording only 208 crashes.
- **Lake County had the highest fatality rate** at 4.296 fatalities per 100 million VMT.
- **Calaveras, Lake, San Benito, and Trinity** ranked among the top 10 counties across all three primary exposure-adjusted safety measures.
- **Pedestrian fatalities were concentrated in high-population and high-traffic counties**, particularly in Southern California, while bicycle fatalities were considerably sparser statewide.

## Tools and Methods

- **R / R Markdown:** Data cleaning, transformation, exploratory analysis, ranking, summary tables, and report generation
- **tidyverse:** Data manipulation and preparation of the county-level analytical dataset
- **ArcGIS Pro:** Spatial joins, choropleth mapping, Natural Breaks (Jenks) classification, and final map layouts
- **U.S. Census TIGER/Line:** 2024 California county boundaries used for spatial analysis
- **GitHub:** Project documentation and reproducible file organization

Three primary exposure-adjusted safety measures were analyzed:

- **Total Crash Rate:** Total crashes per million VMT
- **Fatal-Injury Crash Rate:** Fatal and injury crashes per million VMT
- **Fatality Rate:** Fatalities per 100 million VMT

Pedestrian and bicycle fatalities were analyzed separately as raw county counts rather than exposure-adjusted rates.

## Featured Maps

### Total Crash Rate by California County

![Total Crash Rate by California County, 2024](Maps/Total_Crash_Rate_California_2024.png)

### Fatality Rate by California County

![Fatality Rate by California County, 2024](Maps/Fatality_Rate_California_2024.png)

Additional maps for fatal-injury crash rates, pedestrian fatalities, and bicycle fatalities are available in the [`Maps`](Maps/) directory.

## Repository Structure

```text
california-highway-safety-2024/
|-- Data/
|   `-- county-highway-safety-metrics-2024.csv
|-- Maps/
|   |-- Total_Crash_Rate_California_2024.png
|   |-- Fatal_Injury_Crash_Rate_California_2024.png
|   |-- Fatality_Rate_California_2024.png
|   |-- Pedestrian_Fatalities_California_2024.png
|   `-- Bicycle_Fatalities_California_2024.png
|-- California_Highway_Safety_2024.Rmd
|-- California_Highway_Safety_2024.pdf
|-- California_Highway_Safety_2024.html
|-- README.md
`-- .gitignore
```

## Data Sources

- **California Department of Transportation (Caltrans):** [2024 Crash Data on State Highway System](https://www.lab.data.ca.gov/dataset/2024-crash-data-on-state-highway-system), accessed through California Open Data
- **U.S. Census Bureau:** [2024 TIGER/Line Shapefiles — Counties (and Equivalent)](https://www.census.gov/cgi-bin/geo/shapefiles/index.php?layergroup=Counties%20%28and%20equivalent%29&year=2024)

The published `Data/` directory contains the cleaned county-level analytical dataset used by the final report. Source files and intermediate EDA files are not included in the repository.

## Reproducing the Analysis

The final county-level analytical dataset is provided in [`Data/county-highway-safety-metrics-2024.csv`](Data/county-highway-safety-metrics-2024.csv).

[`California_Highway_Safety_2024.Rmd`](California_Highway_Safety_2024.Rmd) contains the R workflow used to generate the report's tables, rankings, interpretation, and embedded map outputs. ArcGIS Pro was used separately for the spatial join, choropleth design, and exported map layouts.

The repository includes the final exported maps required by the R Markdown report.

## Final Report

- [PDF Report](California_Highway_Safety_2024.pdf)
- [HTML Report](California_Highway_Safety_2024.html)
- [R Markdown Source](California_Highway_Safety_2024.Rmd)

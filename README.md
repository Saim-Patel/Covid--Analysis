# 🦠 COVID-19 Exploratory Data Analysis

Exploring reported COVID-19 cases and deaths across 225 countries and territories with Python.

**Tools:** Python · pandas · Matplotlib · Seaborn · Jupyter / Google Colab

## Questions explored
- Which countries reported the most and fewest cases?
- Which reported the most deaths, and the highest death percentage?
- How do case totals compare across continents?
- How are population, cases and deaths related?

## Key findings
| Finding | Result |
|---|---|
| Most cases | USA (81.8M), India (43.0M), Brazil (30.0M) |
| Most deaths | USA (1.01M), Brazil (660K), India (521K) |
| Highest continent/region case total | Europe (180.3M), then Asia (141.0M) |
| Highest death percentage | Yemen (18.15%) |
| Total cases vs total deaths | Strong rank correlation (Spearman 0.94) |
| Population vs total cases | Moderate to strong rank correlation (Spearman 0.69) |

> These figures describe a static snapshot of *reported* data, not current numbers.
> Death percentage is deaths divided by reported cases. It is affected by testing and reporting, and is unstable for small counts (Western Sahara's 10% is 1 death in 10 cases).
> Correlation does not imply causation.

## Visualizations
### Top 5 countries by cases
![Top 5 cases](images/top5_cases.png)
### Top 5 countries by deaths
![Top 5 deaths](images/top5_deaths.png)
### Cases by continent / region
![Cases by continent](images/cases_by_continent.png)
### Highest death percentage
![Death percentage](images/top5_death_percentage.png)
### Lowest case counts
![Lowest cases](images/lowest5_cases.png)
### Population vs cases
![Population vs cases](images/population_vs_cases.png)
### Cases vs deaths
![Cases vs deaths](images/cases_vs_deaths.png)
### Correlation heatmap
![Heatmap](images/correlation_heatmap.png)

## Workflow
1. Load and inspect the data
2. Fill the one missing `Other names` value
3. Rename the ISO code column and recalculate death percentage
4. Rank, group and visualize
5. Measure Spearman correlations

## Run it
```bash
pip install -r requirements.txt
jupyter notebook notebooks/covid19_analysis.ipynb
```
First place `COVID-19 Coronavirus.csv` in `data/` (see [data/README.md](data/README.md)). In Colab, upload the CSV to `/content/`.

## Structure
```
├── data/            # dataset instructions
├── images/          # charts
├── notebooks/       # analysis notebook
├── index.html       # showcase page (GitHub Pages)
├── requirements.txt
└── README.md
```

## Author
**Saim Patel**, CSE undergraduate, Delhi

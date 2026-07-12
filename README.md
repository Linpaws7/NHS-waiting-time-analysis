# NHS Waiting Time Analysis

A Python-based analysis of NHS Referral to Treatment waiting-list trends, forecasting performance, specialty backlogs and Integrated Care Board pressures across England.

## Project overview

This project analyses NHS waiting-list pressure at three levels:

- national Referral to Treatment waiting-list trends
- specialty-level backlog and 18-week performance
- Integrated Care Board comparisons using raw and population-adjusted measures

The project also evaluates a 12-month national waiting-list forecast using a held-out historical test period.

## Research questions

1. How has the NHS waiting list changed over time?
2. How accurately can the national waiting list be forecast over a 12-month test period?
3. Which specialties have the largest backlogs?
4. Which specialties have the weakest 18-week performance?
5. Which Integrated Care Boards face the greatest waiting-list pressure?
6. How do ICB rankings change after adjusting for population size?

## Key findings

- National forecast MAPE: **1.23%**
- National forecast MAE: **89,075**
- National forecast RMSE: **113,131**
- Largest specialty backlog: **Trauma and Orthopaedic Service — 836,764**
- Weakest specialty by 18-week performance: **Oral Surgery Service — 52.4%**
- Largest raw ICB backlog: **NHS Greater Manchester Integrated Care Board — 826,752**
- Highest backlog per 100,000 population: **NHS Mid and South Essex Integrated Care Board — 32,012.3**
- Highest 52+ week waiting pressure per 100,000: **NHS Mid and South Essex Integrated Care Board — 2,187.1**

## Methods

The analytical workflow includes:

- data cleaning and validation
- national waiting-list trend analysis
- time-series visualisation
- time-series decomposition
- train-and-test forecast evaluation
- MAE, RMSE and MAPE calculation
- 12-month national forecasting
- specialty backlog ranking
- specialty 18-week performance analysis
- ICB-level backlog ranking
- population-adjusted waiting-list measures
- backlog and performance relationship analysis

## Data sources

The project uses publicly available NHS Referral to Treatment waiting-time data and Office for National Statistics population estimates.

The population workbook included in the repository is:

```text
data/raw/sapeicb20222024.xlsx
```

It is used to calculate population-adjusted ICB measures such as backlog per 100,000 residents.

Not every original NHS raw extract used during the complete analysis is included in this repository. The notebooks, figures and result tables are retained for review, but a complete end-to-end rerun may require downloading the relevant NHS source files again.

## Repository structure

```text
NHS-waiting-time-analysis/
├── data/
│   └── raw/
│       └── sapeicb20222024.xlsx
├── notebooks/
│   ├── README.md
│   ├── NHS_Waiting_Time_original.ipynb
│   └── NHS_Waiting_Time_clean_for_github.ipynb
├── outputs/
│   ├── figures/
│   ├── tables/
│   └── README.md
├── .gitignore
├── LICENSE
├── README.md
└── requirements.txt
```

## Main notebook

The cleaned public-facing notebook is:

[Open the main analysis notebook](notebooks/NHS_Waiting_Time_clean_for_github.ipynb)

The original working notebook is retained separately:

```text
notebooks/NHS_Waiting_Time_original.ipynb
```

## Main outputs

### Figures

The `outputs/figures/` folder includes:

- national NHS waiting-list trends
- post-2018 waiting-list trends
- time-series decomposition
- train-and-test forecast evaluation
- 12-month national forecast
- specialty backlog rankings
- specialty 18-week performance
- specialty bottleneck analysis
- ICB backlog rankings
- population-adjusted ICB rankings
- ICB backlog and performance comparisons

Important figure files include:

```text
england_nhs_rtt_waiting_list.png
england_nhs_rtt_waiting_list_2018_onward.png
england_nhs_rtt_decomposition_2018_onward.png
england_nhs_rtt_train_test_evaluation.png
england_nhs_rtt_forecast_12_months.png
specialty_top10_backlog_jan2026.png
specialty_worst18weeks_jan2026.png
specialty_bottleneck_scatter_jan2026.png
icb_top10_backlog.png
icb_top10_backlog_per100k.png
icb_top10_52plus_per100k.png
icb_backlog_per100k_vs_18weeks.png
icb_worst18weeks.png
```

### Tables

The `outputs/tables/` folder includes:

```text
england_nhs_rtt_test_results.csv
project_summary_table.csv
final_ranked_icbs.csv
icb_final_waiting_population_metrics.csv
icb_summary_jan2026.csv
icb_waiting_metrics_jan2026.csv
```

These files contain forecast evaluation results, project summary statistics, specialty analysis and ICB rankings.

## Running the project

Clone the repository:

```bash
git clone https://github.com/Linpaws7/NHS-waiting-time-analysis.git
cd NHS-waiting-time-analysis
```

Install the required Python packages:

```bash
pip install -r requirements.txt
```

Open the cleaned notebook:

```bash
jupyter notebook notebooks/NHS_Waiting_Time_clean_for_github.ipynb
```

## Reproducibility note

The cleaned notebook is the main public-facing analysis file.

Because not every original NHS raw extract is included, some parts of the workflow may require the relevant source data to be downloaded again before the full analysis can be rerun.

The exported figures and result tables are included so that the project findings can still be reviewed directly.

## Limitations

- Not every original NHS raw data file is included.
- Full reproduction may require downloading the original NHS source extracts.
- Forecast accuracy is based on a selected historical test period and does not guarantee future performance.
- ICB population-adjusted measures depend on the population estimates and geographic definitions used.
- Results describe aggregate system pressure and should not be interpreted as individual patient outcomes.
- Forecasting results may change when additional observations or alternative model specifications are used.

## Tools

- Python
- pandas
- NumPy
- Matplotlib
- statsmodels
- scikit-learn
- Jupyter Notebook

## Licence

The repository code is released under the MIT Licence.

The original NHS and ONS datasets remain subject to their respective source terms and licences.

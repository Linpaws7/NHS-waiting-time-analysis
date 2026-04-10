# NHS Waiting List Forecasting (England)

A structured research repository for national NHS RTT waiting list forecasting and ICB-level backlog pressure analysis in England.

## Overview

This repository contains the packaged outputs from a waiting list forecasting project focused on:

- England-level RTT waiting list trend analysis
- 12-month national forecast evaluation
- specialty-level backlog and 18-week performance review
- ICB-level ranking by raw backlog, backlog per 100,000 population, and 52+ week pressure

The current package is designed to be clean and uploadable to GitHub. It includes the main figures, result tables, repository metadata, and a project summary document.

## Key findings

- **National forecast accuracy:** MAPE = 1.23%, MAE = 89,075, RMSE = 113,131
- **Top specialty backlog:** Trauma and Orthopaedic Service (836,764)
- **Weakest specialty by 18-week performance:** Oral Surgery Service (52.4%)
- **Top ICB by raw backlog:** Nhs Greater Manchester Integrated Care Board (826,752)
- **Top ICB by backlog per 100k:** Nhs Mid And South Essex Integrated Care Board (32012.3)
- **Top ICB by 52+ weeks per 100k:** Nhs Mid And South Essex Integrated Care Board (2187.1)

## Included in this package

- curated output figures
- cleaned result tables
- raw population-denominator workbook used for ICB population analysis
- project summary `.docx`
- starter repository files (`README`, `LICENSE`, `.gitignore`, `requirements.txt`)

## Repository structure

```text
nhs_waiting_list_forecasting_github_ready/
├── README.md
├── LICENSE
├── .gitignore
├── requirements.txt
├── data/
│   └── raw/
│       └── sapeicb20222024.xlsx
├── notebooks/
│   ├── README.md
│   ├── NHS_Waiting_Time_original.ipynb
│   └── NHS_Waiting_Time_clean_for_github.ipynb
├── outputs/
│   ├── figures/
│   └── tables/
└── docs/
    └── NHS_Waiting_List_Forecasting_Project_Summary.docx
```

## Notes on data

The raw workbook included in this repository is:

- **`data/raw/sapeicb20222024.xlsx`**  
  ONS population estimates for 2024 Integrated Care Boards in England, used for denominator-based ICB metrics such as backlog per 100,000 population.

This package now includes the original notebook you uploaded and a cleaned GitHub-friendly notebook copy. That makes the repository much stronger for public upload, although it is still **not fully reproducible end-to-end** because not every original NHS raw extract is bundled here.

## Current limitation

This package still does **not** yet include:

- every original raw NHS extract used during the full workflow
- a frozen environment file verified against the original runtime

So this is suitable for:
- GitHub portfolio presentation
- sharing final outputs
- attaching to applications as a project repository

To make it fully reproducible later, add:
1. the exact raw NHS source file(s)
2. a validated environment file
3. any final project paper or presentation you want to cite from the repository

## Suggested GitHub repository name

`nhs-waiting-list-forecasting-england`

## Suggested GitHub description

Forecasting NHS RTT waiting list trends in England with specialty and ICB backlog analysis.

## Suggested tags

`python` `healthcare` `forecasting` `nhs` `time-series` `data-analysis` `public-health`

## Main output files

### Figures
- `england_nhs_rtt_waiting_list.png`
- `england_nhs_rtt_waiting_list_2018_onward.png`
- `england_nhs_rtt_decomposition_2018_onward.png`
- `england_nhs_rtt_train_test_evaluation.png`
- `england_nhs_rtt_forecast_12_months.png`
- `specialty_top10_backlog_jan2026.png`
- `specialty_worst18weeks_jan2026.png`
- `specialty_bottleneck_scatter_jan2026.png`
- `icb_top10_backlog.png`
- `icb_top10_backlog_per100k.png`
- `icb_top10_52plus_per100k.png`
- `icb_backlog_per100k_vs_18weeks.png`
- `icb_worst18weeks.png`

### Tables
- `england_nhs_rtt_test_results.csv`
- `project_summary_table.csv`
- `final_ranked_icbs.csv`
- `icb_final_waiting_population_metrics.csv`
- `icb_summary_jan2026.csv`
- `icb_waiting_metrics_jan2026.csv`

## Upload steps

1. Create a new GitHub repository.
2. Upload the contents of this folder.
3. Set the repository description using the text above.
4. Pin the repository on your profile if this is one of your main portfolio projects.
5. Use `NHS_Waiting_Time_clean_for_github.ipynb` as the main public notebook.
6. Keep `NHS_Waiting_Time_original.ipynb` in the repo if you want to preserve the original working file.

## Author note

Packaged for GitHub upload on 10 April 2026.

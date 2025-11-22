# Student Retention Analytics Portfolio (Anonymized)

This repository showcases an end-to-end analytics workflow for a synthetic university student retention dataset with 2,134 records. It is designed to mirror the kind of work I do in institutional research and enrollment analytics: data cleaning, exploratory analysis, modeling, and communication for non-technical decision makers.

All data are anonymized and synthetic. No PII or restricted institutional records are used.

## Project overview

The dataset simulates a realistic campus service environment with:

- Academic metrics: current and historical GPA, credits completed, academic warnings.
- Engagement indicators: attendance rate, advisor meetings, enrollment gaps.
- Demographics: age, gender, ethnicity, major.
- Administrative signals: financial aid status, dropout risk flags.
- Outcomes: next-semester dropout indicator, dropout type, dropout duration, dropout cause.

The analysis pipeline follows this path:

Raw data → Cleaning and feature prep → Visual dashboard → Statistical tests → Logistic model → Plain-language narrative for leaders.

## Key outputs for reviewers

- Dataset  
  `data/university_student_retention_dataset_2134.csv`

- Dashboard visuals  
  `figures/01_retention_vs_dropout.png`  
  `figures/02_dropout_by_major.png`  
  `figures/03_dropout_by_financial_aid.png`  
  `figures/04_dropout_by_gender.png`  
  `figures/05_dropout_by_ethnicity.png`  
  `figures/06_gpa_by_retention.png`  
  `figures/07_attendance_by_retention.png`  
  `figures/08_dropout_type_pie.png`  
  `figures/09_dropout_cause_pie.png`  
  `figures/10_gpa_trajectory_by_retention.png`  
  `figures/11_correlation_heatmap_red.png`

- Statistical outputs  
  `stats/descriptive_stats_key_vars.csv`  
  `stats/chi_square_financial_aid_vs_dropout.txt`  
  `stats/logistic_regression_dropout.txt`  
  `stats/correlation_matrix_numeric.csv`

## Methods

- Descriptive statistics for core variables: age, GPA, attendance, credits, enrollment gaps, warnings, meetings, dropout duration.
- Visual analysis by group: major, gender, ethnicity, financial aid.
- Chi-square test: financial aid status × next-semester dropout.
- Logistic regression to model next-semester dropout using GPA, attendance, warnings, and aid status.
- Correlation matrix and red heatmap for key numeric variables.

## How to view the portfolio site

The GitHub Pages site for this repo uses the `docs/` folder as the site root.

Once GitHub Pages is enabled (Settings → Pages → Source: `main`, Folder: `/docs`), the live site will be available at:

`https://YOUR-USERNAME.github.io/student-retention-analytics-portfolio/`

Replace `YOUR-USERNAME` with your GitHub handle.

## About

This project is intended as a realistic sample of higher-ed retention analytics suitable for institutional research, student success, and enrollment management roles.

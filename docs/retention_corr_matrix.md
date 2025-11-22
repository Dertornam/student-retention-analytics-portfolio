# Retention Correlation Matrix

## Anonymized Datasets, Data Cleaning, Dashboards & Automated Reporting

# Correlation Matrix

The full numeric matrix is available as:

`stats/correlation_matrix_numeric.csv`

The red heatmap version is shown on the main dashboard page as `figures/11_correlation_heatmap_red.png`.

Key relationships from the matrix:

- Current GPA and historical GPA correlate at about 0.98.  
- Dropout risk correlates around 0.72 with next-semester dropout.  
- Dropout duration correlates around 0.55 with next-semester dropout.  
- Almost all other variables have correlations with next-semester dropout near zero.

## Interpretation — Correlation Matrix

### What stands out

Academic performance measures move together very strongly. Current GPA and historical GPA are almost interchangeable in this dataset, which is what you would expect when prior performance predicts current performance.

The engineered dropout risk flag and dropout duration align closely with the next-semester dropout outcome. That shows the outcome variables are consistent with each other and with the way the synthetic risk scores were generated.

Most other variables, including attendance, credits, and advisor meetings, show very weak direct correlations with dropout. Their coefficients sit near zero rather than indicating strong linear relationships.

### What it means

Retention is not a single-variable phenomenon here. GPA, attendance, credits, and meetings each contribute small pieces of information, but none alone can explain why students stay or leave.

The strong clustering among risk, duration, and the dropout outcome tells us that the outcome definitions are coherent and that the synthetic dataset is internally consistent. This gives a solid foundation for modeling and segmentation.

For practice, this pattern encourages leaders to think in terms of profiles instead of single thresholds. Dashboards should visualize combinations of GPA, warnings, risk scores, and financial context rather than relying on one metric to drive intervention.

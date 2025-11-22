# Chi-square: Financial Aid Status × Next-semester Dropout

## Anonymized Datasets, Data Cleaning, Dashboards & Automated Reporting

This page summarizes a simple but realistic question.  
Is there an association between receiving financial aid and dropping out by the next semester?

All numbers come directly from the synthetic dataset of 2,134 students.

---

## Crosstab and test results

Contingency table from `stats/chi_square_financial_aid_vs_dropout.txt`:

```text
next_semester_dropout  False  True 
financial_aid_status               
False                    899    163
True                     874    198

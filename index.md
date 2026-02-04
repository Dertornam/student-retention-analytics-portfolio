---
title: ## Student Retention Analytics (Anonymized) — Higher-Ed Retention Case Study
---

**Tools:** Python (Pandas, NumPy, SciPy, Statsmodels, Matplotlib), SQL, SPSS (validation workflow)

<style>
.port-btn{
  display:inline-block;
  padding:.6rem 1rem;
  margin:.25rem .4rem 0 0;
  border-radius:8px;
  background:#0366d6;
  color:#fff !important;
  text-decoration:none !important;
  border:1px solid rgba(0,0,0,.08);
  box-shadow:0 1px 2px rgba(0,0,0,.05);
  font-weight:600;
}
.port-btn:hover{ filter:brightness(0.95); }
</style>

<div style="margin: 1rem 0;">
  <a class="port-btn" href="{{ '/executive-summary' | relative_url }}">Executive Summary</a>
  <a class="port-btn" href="{{ '/statistical-tables' | relative_url }}">Statistical Tables</a>
  <a class="port-btn" href="{{ '/datasets' | relative_url }}">Datasets</a>
  <a class="port-btn" href="{{ '/sql-and-syntaxes' | relative_url }}">SQL & Syntax</a>
  <a class="port-btn" href="{{ '/data-dictionary' | relative_url }}">Data Dictionary</a>
  <a class="port-btn" href="{{ '/reproducibility' | relative_url }}">Reproducibility</a>
</div>

<style>
.page-content img{
  max-width: 100%;
  height: auto;
  border-radius: 10px;
  box-shadow: 0 1px 2px rgba(0,0,0,.06);
  margin: .5rem 0 1rem 0;
}
</style>

---

## Introduction & Project Objective
The goal of this project was to translate retention risk into a set of defensible signals that an institutional leader can act on without reading code. I focused on the “So What?” question for a vice provost or dean: which groups show meaningful risk differences, what the underlying drivers appear to be, and what an institution should do next to reduce next-semester dropout.

This analysis uses a synthetic but realistic retention dataset of 2,134 students with academic, demographic, engagement, and outcome variables. The dataset is shaped to mirror modern higher-ed environments, including dropout types and self-reported dropout causes.

## Methodology
**Data Acquisition:** The dataset contains 2,134 student records with outcomes for next-semester dropout and related risk markers.  
**Data Engineering:** I prepared analysis-ready fields and derived summary measures for group comparisons.  
**Analytic Framework:**  
**Descriptive Analytics:** To establish baseline retention and subgroup rates.  
**Group Comparisons:** By major, financial aid, gender, and ethnicity to detect stratified risk patterns.  
**Correlation Review:** To quantify how strongly common predictors relate to dropout and to avoid overclaiming causality from weak relationships.  
**Inferential Testing and Modeling:** Detailed outputs are provided on the Statistical Tables page, including chi-square and logistic regression.

## Key Findings & Interpretation
### A. Baseline Retention and Institutional Exposure
**Results:** 1,773 students are retained and 361 do not return. That is roughly 83% retained and 17% dropout.  
**Interpretation:** The retained majority is expected in most institutions, but a 17% non-returner group is large enough to create budget, course planning, and student success impacts.  
**Conclusion:** This dataset supports meaningful risk segmentation because the dropout group is not trivially small.

### Visual: Overall retention vs dropout
![Retention vs Dropout]({{ '/figures/01_retention_vs_dropout.png' | relative_url }})

### B. Program-Level Variation Exists, but the Pattern is Modest
**Results:** Dropout rates by major range from about 15.8% (Business) to about 18.5% (Psychology), with most majors clustered in the 16–17% range.  
**Interpretation:** The spread is present but not dramatic, which suggests the institution should not treat retention as only a “program problem.”  
**Conclusion:** Program-level monitoring is warranted, but the risk story likely requires cross-cutting drivers (financial strain, engagement friction, advising continuity).

### Visual: Dropout rate by major
![Dropout Rate by Major]({{ '/figures/02_dropout_by_major.png' | relative_url }})

### C. Financial Aid Status Signals Elevated Risk
**Results:** Students without aid show a dropout rate around 15.3%, while students with aid are closer to 18.5%.  
**Interpretation:** This pattern aligns with the operational reality that aid status can proxy financial fragility, which increases sensitivity to shocks.  
**Conclusion:** Financial aid status is a practical risk flag for dashboards and early outreach, even when the gap is moderate rather than extreme.

### Visual: Dropout rate by financial aid
![Dropout Rate by Financial Aid Status]({{ '/figures/03_dropout_by_financial_aid.png' | relative_url }})

### D. Gender and Ethnicity Differences Justify Disaggregated Monitoring
**Results:** Female students show a dropout rate around 19.7% compared to about 14.6% for male students. Ethnicity rates vary, with White students lowest (~12.9%) and several other groups clustering around ~17.9% to ~18.8%.  
**Interpretation:** These are not “single-variable explanations,” but they are consistent enough to justify disaggregated dashboards and targeted diagnostics.  
**Conclusion:** A one-size-fits-all retention strategy risks missing subgroup-specific friction. Leaders should require reporting cuts that make these gaps visible.

### Visual: Dropout rate by gender
![Dropout Rate by Gender]({{ '/figures/04_dropout_by_gender.png' | relative_url }})

### Visual: Dropout rate by ethnicity
![Dropout Rate by Ethnicity]({{ '/figures/05_dropout_by_ethnicity.png' | relative_url }})

## Visual Highlights
**Academic Signals Are Not a Clean Cliff:** GPA and attendance distributions overlap between retained and dropout students.  
**Interpretation:** This is a realistic retention pattern. Many students who leave are not strictly failing, and single-threshold rules will miss risk.  
**Conclusion:** Early-warning systems should combine academic performance with engagement, advising continuity, and enrollment disruption variables.

### Visual: Current GPA by retention status
![GPA by Retention]({{ '/figures/06_gpa_by_retention.png' | relative_url }})

### Visual: Attendance rate by retention status
![Attendance by Retention]({{ '/figures/07_attendance_by_retention.png' | relative_url }})

## Outcome Structure: Why “Dropout” Is Not One Thing
**Results:** Among non-returners, the dataset includes temporary stop-outs, permanent withdrawals, and transfers. Reported causes are distributed across academic, financial, mental health, and other.  
**Interpretation:** These distinctions matter operationally because the institutional response and “loss” definition differs by type.  
**Conclusion:** Leaders should treat retention as a classification problem with different intervention pathways rather than a single homogeneous outcome.

### Visual: Dropout types
![Dropout Types]({{ '/figures/08_dropout_type_pie.png' | relative_url }})

### Visual: Reported dropout causes
![Dropout Causes]({{ '/figures/09_dropout_cause_pie.png' | relative_url }})

## Correlation and Risk Structure
**Results:** Most correlations with next-semester dropout are weak, while GPA measures correlate strongly with each other.  
**Interpretation:** Weak single-variable correlation is common in retention work and reinforces the need for multi-signal risk scoring rather than single-factor explanations.  
**Conclusion:** Prediction and intervention should be designed around layered signals, not a single KPI like GPA.

### Visual: Correlation matrix
![Correlation Matrix]({{ '/figures/11_correlation_heatmap.png' | relative_url }})

## Final Recommendations (The “So What?”)
**Build a Multi-Signal Early Warning Dashboard:** Combine academic standing, engagement, advising continuity, and enrollment disruption to avoid false confidence from one metric.  
**Use Disaggregated Risk Monitoring as a Standard:** Require routine reporting cuts by aid status, major, gender, and ethnicity to surface consistent gaps early.  
**Differentiate Intervention Paths by Dropout Type:** Transfers, stop-outs, and permanent withdrawals require different playbooks and should not be treated as the same operational “loss.”

## Dataset Profile & Data Quality Notes
The analytic file contains 2,134 synthetic students with a realistic dropout share (361 non-returners). The dataset includes both structured predictors and outcome subtypes (dropout type and cause), which supports a more operationally accurate retention narrative than a single binary outcome alone.

## Contact & Links
<div class="contact-links">
  <a class="port-btn" href="https://www.linkedin.com/in/derrick-dzormeku-mba-75288644" target="_blank" rel="noopener">LinkedIn</a>
  <a class="port-btn" href="https://mail.google.com/mail/?view=cm&fs=1&to=d.double76@icloud.com&su=Portfolio%20inquiry%20%E2%80%93%20Derrick%20Dzormeku&body=Hi%20Derrick,%0D%0A%0D%0AI%27m%20reaching%20out%20about%20your%20analytics%20portfolio.%20Could%20we%20schedule%20a%20brief%20call%3F" target="_blank" rel="noopener">Email</a>
  <a class="port-btn" href="https://dertornam.github.io/higher-ed-analytics-portfolio/" target="_blank" rel="noopener">Other Portfolios</a>
</div>

<style>
.contact-links { margin-top: .75rem; display:flex; flex-wrap:wrap; gap:.75rem; }
.port-btn { display:inline-block; background:#0066cc; color:#fff !important; padding:.75rem 1.75rem; border-radius:12px; font-weight:700; text-decoration:none; font-size:1rem; text-align:center; }
.port-btn:hover { background:#0053a6; }
</style>

This project is designed as a portfolio example of how retention analytics can be made decision-ready for academic leadership.

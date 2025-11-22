# Retention Descriptive Statistics

## Anonymized Datasets, Data Cleaning, Dashboards & Automated Reporting

# Descriptive Statistics

n = 2,134 students

| Variable                | Mean   | Std Dev | Min   | 25%   | 50%   | 75%   | Max   |
|-------------------------|--------|--------:|------:|------:|------:|------:|------:|
| age                     | 23.40  | 3.45    | 18.00 | 20.00 | 23.00 | 26.00 | 29.00 |
| gpa_current             | 2.76   | 0.72    | 1.50  | 2.14  | 2.77  | 3.37  | 4.00  |
| gpa_history             | 2.50   | 0.74    | 1.05  | 1.89  | 2.49  | 3.12  | 3.99  |
| attendance_rate         | 0.75   | 0.14    | 0.50  | 0.64  | 0.75  | 0.87  | 1.00  |
| enrollment_gap_months   | 0.99   | 1.14    | 0.00  | 0.00  | 1.00  | 2.00  | 3.00  |
| credits_completed       | 69.87  | 29.01   | 20.00 | 44.00 | 71.00 | 95.00 | 119.0 |
| academic_warning_count  | 1.54   | 1.12    | 0.00  | 1.00  | 2.00  | 3.00  | 3.00  |
| advisor_meeting_count   | 2.48   | 1.70    | 0.00  | 1.00  | 2.00  | 4.00  | 5.00  |
| dropout_duration        | 0.36   | 0.84    | 0.00  | 0.00  | 0.00  | 0.00  | 3.00  |

The table comes directly from `stats/descriptive_stats_key_vars.csv`.

## Interpretation — Descriptive Statistics

### What stands out

Most students are in their early twenties, with a tight age range around 23 years old. Current GPA centers around 2.8 on a 4.0 scale, with historical GPA only slightly lower.

Attendance is generally strong, with typical rates in the mid-70 to upper-80 percent range. Credits completed span from early-career students in the twenties into students nearing graduation with over one hundred credits.

Academic warning counts cluster between one and three. Advisor meetings average about two and a half per student, which suggests regular but not constant engagement.

Dropout duration has a mean well below one semester because most students do not drop out at all, and a smaller subgroup experience temporary or longer breaks.

### What it means

The sample looks like a mixed cohort of students spread across the degree lifecycle rather than only first-semester entrants. Most are progressing reasonably well academically and staying connected enough to advisors.

The combination of decent GPA, solid attendance, and regular advising hints at a baseline of student success with pockets of vulnerability. Dropout duration’s distribution reinforces that risk is concentrated in a minority rather than spread evenly.

For decision makers, this profile is the baseline. Any segmentation by major, gender, ethnicity, or financial aid should be interpreted against the fact that the “average” student is doing relatively well but still leaves room for targeted support.

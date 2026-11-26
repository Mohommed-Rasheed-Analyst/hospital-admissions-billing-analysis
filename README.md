# Hospital Admissions and Billing Analysis (Excel)

An Excel analysis of 10,000 hospital admission records (Oct 2018 to Oct 2023). It looks at who is being treated, what drives the cost of care, and how a hospital could plan its beds and staff. This was a practice case study from my data analytics course, so the dataset is a practice dataset and the findings are illustrations and not real hospital results.

## Questions I answered
1. Which medical conditions are most common in different patient groups?
2. What drives the billing amount, and what could patients do to reduce their cost?
3. How do admission types change over time, and how could the hospital manage its resources better?

## What I did
- Cleaned the data in Power Query: removed 11 empty columns, fixed 158 mistyped ages (like 8I for 81), standardised gender, blood type, admission type and condition spellings, fixed 11 billing amounts with a letter O instead of 0, and converted two text date columns (49 and 137 of them in a long format) to real dates.
- Built PivotTables and PivotCharts for each question, with helper columns for age group, length of stay and admission month.
- Left the 24 admissions with no bill out of the billing averages instead of treating them as zero.

## Key findings
- Hypertension is the most common condition overall (21.6% of admissions). Asthma is mostly a young person's condition: 26.7% of admissions at ages 18-34 against about 12% in older groups. Arthritis and cancer rise with age.
- The medical condition is what drives the bill. Cancer averages $39,688 per admission (70% above average), diabetes $30,097 (+29%) and obesity $12,512 (-46%). Insurer, medication, admission type, age group, test result and gender each move the average by only a few percent, and length of stay has no relationship with billing (correlation -0.003).
- Admissions are flat at about 2,000 a year from 2019 to 2022, and the mix of admission types is stable. Emergency and Urgent patients stay about 15.5 days against 10 for Elective, so they use about 78% of bed-days from 69% of admissions. Beds should be planned on bed-days and not admission counts.

## Screenshots
![Overview](images/overview.png)
![Demographics by age group](images/demographics-age.png)
![Demographics by gender](images/demographics-gender.png)
![Average billing by medical condition](images/billing-by-condition.png)
![Billing drivers](images/billing-drivers.png)
![Admission trends](images/admission-trends.png)

## Files
- US_Hospital_Admissions_Billing_Analysis.xlsx: the full workbook (Overview, Demographics, Billing_Drivers, Admission_Trends, Clean_Data, Raw_Data)
- images/: screenshots used above

## Limits
- The counts are admissions, not unique patients.
- 2018 and 2023 are partial years, so yearly trends use 2019 to 2022.
- Bills in this dataset do not rise with length of stay, which is unusual for real hospital data, so I treat the billing patterns as indicative.

## Tools
Excel, Power Query, PivotTables, PivotCharts

Author: Rasheed Mohommed | LinkedIn: linkedin.com/in/mohommed-rasheed-analyst

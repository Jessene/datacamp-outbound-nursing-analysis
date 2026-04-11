# Outbound Nursing Team Call Analysis

**DataCamp Data Analyst Professional Certification — Practical Exam**

## Business Problem

Universal Healthy Humans Company wants to increase screening compliance rates. An outbound nursing team contacts patients who have not completed their required health screenings. The hospital wants to understand:

- How many patients were successfully reached?
- Was there a difference in compliance based on how many screenings a patient was eligible for?
- Were patients more likely to complete their screening after the nursing team reached out?
- How should the outbound calls be optimized?

## Dataset

**`outbound_call_nursing_team.csv`** — 1,988 records of patient screening and outreach data.

| Column | Description |
|---|---|
| `patient_id` | Unique identifier for each patient |
| `screening_type` | Type of screening (BCS, CBP, COL, EED, OMW) |
| `screening_completed_ind` | Whether the screening was completed (1 = yes, 0 = no) |
| `latest_call_date` | Date of the most recent outbound call attempt |
| `reached_ind` | Whether the patient was reached by phone (1 = reached, 0 = not reached) |
| `screening_date` | Date the screening was scheduled or completed |

## Key Findings

- Of 166 patients, only 40% were successfully reached by the nursing team, while 44% were never called.
- Patients with more eligible screening types trended toward lower initial compliance (p = 0.058), suggesting the program should prioritize patients with multiple screenings.
- "Reached" and "Not Reached" patients had very similar completion rates — making contact may not be as important as simply making an attempt.
- A Scheduling Efficiency Ratio (SER) metric was proposed; current values range from 2.12x (OMW) to 2.81x (BCS), indicating significant rescheduling overhead.
- An A/B test with demographic data is recommended to identify which patient profiles benefit most from outreach.

## Repository Structure

```
├── README.md
├── LICENSE
├── notebook.ipynb                        # Full analysis and report
├── Data Analyst Presentation .pdf        # Non-technical presentation (PDF)
├── Data Analyst Presentation .key        # Non-technical presentation (Keynote)
├── outbound_call_nursing_team.csv
└── figures/
    ├── patients_by_call_status.png
    ├── Comparison_Frequency_Patient_Count.png
    ├── Compliance_rate_eligible_screenings.png
    ├── initial_compliance.png
    ├── mean_completion_rates.png
    ├── number_screening_scheduled.png
    ├── screening_completion_grouped.png
    └── screening_completion_proportions_call_screening.png
```

## Tools & Packages

- **Language:** R
- **Environment:** DataCamp DataLab
- **Packages:** tidyverse, stringr, lubridate, ggplot2, scales, glue, rstatix, ggsignif, ggtext

## Author

Jessene Aquino-Thomas

## License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.

---

*Completed as part of the [DataCamp Data Analyst Certification]([https://www.datacamp.com/certification/data-analyst-professional](https://www.datacamp.com/certificate/DA0021861645910)), December 2025.*

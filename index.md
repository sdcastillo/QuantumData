---
layout: default
title: QuantumData
description: Datasets for actuaries practicing predictive analytics.
samwiki: true
---

QuantumData holds tables for actuaries who are practicing predictive analytics in the form Exam PA expects. Each object is a rectangular data frame with a documented response, a mix of numeric and categorical predictors, and a row count that still fits in memory on a laptop. The files come from SOA exam sittings, SOA sample projects, and the practice exams written around that syllabus, plus a few public modeling sets used the same way.

The exam task is to explore a file, choose a GLM or a tree, hold out data, and say what the fit means for a decision. These tables are the raw material for that loop. Targets include claim amounts, retention, a high-value flag, hospital days, crash severity, and hourly counts. Predictors are the ones a pricing, underwriting, or health analyst would actually be handed: demographics, prior utilization, road and weather conditions, and a handful of scores built by someone else.

The level is intermediate. A first course in GLMs is enough to start. The practice is in the exam habits around the model: a split that respects time when the rows are ordered, a check that each predictor is known before the outcome, and a short recommendation a claims or pricing lead could use. The UCI bank file is the clearest case. Call duration dominates a model of whether the customer subscribed, and duration is known only after the call ends, so a score meant to be used before the call leaves that column out.

Column dictionaries live in this repository, one roxygen file per table under `R/` and the generated help under `man/`. Several source extracts are also stored as CSV under `raw-data/`. The packaged `.RData` objects are not in the git tree. The project notes record that those files were moved to [Hugging Face](https://huggingface.co/supersam7).

### Tables

- **Exam sittings.** `june_pa` is the June 2019 crash file: 23,137 crashes, a severity score, and road, weather, light, and time features. `customer_value` is the December 2019 file: 48,842 prospects and a high or low value flag, with an insurance score, capital gains, and hours worked. The June 2020 files are `patient_length_of_stay` (days in hospital, admission type, and medication indicators, 10,000 stays), `customer_phone_calls`, and `patient_num_labs`.
- **SOA sample projects.** `readmission` is the 2019 hospital readmission sample: 66,782 stays, a binary readmission flag, prior emergency visits, length of stay, and an HCC risk score. `student_success` is the 2019 student sample: 585 rows and a wide set of school, family, and study variables.
- **Practice-exam files.** `health_insurance` is 1,338 policies with age, BMI, smoking status, and annual charges. `apartment_apps` is 1,430 buildings with application counts and unit characteristics. `exam_pa_titanic` is 906 passengers with survival, ticket class, and age.
- **Related modeling tables.** `auto_claim` is 10,296 auto policies with claim frequency, claim amount, and whether the policy was retained. `bank_loans` is the UCI bank marketing extract: 41,188 contacts and 21 variables, including credit default, housing, and campaign history. `actuary_salaries` is a small DW Simpson table of salary bands by industry, exams, and years of experience. `travel_insurance` and `travel_spending` are trip-cost tables. `bike_sharing_demand` and `pedestrian_activity` are hourly counts with weather. `boston` is the 506-tract housing file.

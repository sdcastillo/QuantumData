## About

The R library for [PredictiveInsightsAI.com](PredictiveInsightsAI.com), **the comprehensive, all-in-one solution to help you pass PA**.  Includes practice exams and quizzes and video tutorials.  Don’t let PA stop you from earning your ASA!

5 years.  That’s the average time required to pass all the exams to get an ASA.
The pass rate of PA is only 50%. And this includes people who are taking PA for a second time.
Having to retake PA adds another 6 months to this journey.

## Download the data

For your convenience, all data in this book, including data from prior exams and sample solutions, has been put into a library called `ExamPAData` which is available on CRAN.

```{r eval = F}
install.packages("ExamPAData")
library(ExamPAData)
```

To get the data dictionary for a data set, use `?dataset_name` such as `?customer_phone_calls`.  For your convenience, you can use these data sets for your own practice.  They make great candidates for machine learning problems. 

| Dataset   |      Description      |
|----------|-------------|
|`customer_phone_calls`| Data used on June 18, 2020 Exam PA |
|`patient_length_of_stay`| Data used on June 16, 2020 Exam PA|
|`patient_num_labs`| Data used on June 19, 2020 Exam PA |
|`actuary_salaries`| DW Simpson actuarial salary data|
|`june_pa`|Auto crash data set from SOA June 2019 PA|
|`customer_value`| Customer value data set from December 2019 PA|
|`exam_pa_titanic`| Titanic passengers as used in PredictiveInsightsAI.com's practice exam |
|`apartment_apps`| Apartment applications as used in PredictiveInsightsAI.com's Practice Exam|
|`health_insurance`| Health insurance claims as used in PredictiveInsightsAI.com's Practice Exam|
|`student_success`| SOA Student Success PA Sample Project, 2019|
|`readmission`| SOA Hospital Readmissions Sample Exam, 2019 |
|`auto_claim`| Automotive claims |
|`boston`| Boston housing data set |
|`bank_loans`| Credit data from UCI Machine Learning Repository |


## Data Migration Notice

All data has been migrated over to https://huggingface.co/supersam7

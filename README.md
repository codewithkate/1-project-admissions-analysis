# Project 1: Standardized Test Analysis

## Overview
- [Background](#Background)
- [Data Import & Cleaning](#Data-Import-and-Cleaning)
- [Exploratory Data Analysis](#Exploratory-Data-Analysis)
- [Data Visualization](#Visualize-the-Data)
- [Conclusions and Recommendations](#Conclusions-and-Recommendations)

## Background
---
The pandemic influenced the adoption of test optional policies. In 2021, 51 states made the switch. This project evaluates the now 316 test-optional schools and their varying policy periods.

Note that there is substantial amount of critique of standardized testing. During the pandemic, student-run nonprofit groups campaigned for all colleges and universities to adopt test-optional policies.

Before these events, more critiques were based on the fact that standardized tests are being promoted with the narrative of standardization, yet competition was centered in the actual approach.

### Problem Statement
This project aims to evaluate the relationships amongst university admissions factors within the context of national participation rates and performance. The cleaned data, visualizations, and findings could be used to inform policy decisions around creating or expanding test-optional policies to maintain standards in the admissions process.

### Deliverables
- A Jupyter notebook that describes the data with visualizations & statistical analysis.
- A README markdown file that provides an introduction to and overview of the project.
- A presentation slideshow rendered as a .pdf file.

## Datas Import and Cleaning
---
#### Provided Data
* [`act_2017.csv`](./data/act_2017.csv): 2017 ACT Scores by State ([source](https://blog.prepscholar.com/act-scores-by-state-averages-highs-and-lows))
* [`act_2018.csv`](./data/act_2018.csv): 2018 ACT Scores by State ([source](https://blog.prepscholar.com/act-scores-by-state-averages-highs-and-lows))
* [`act_2019.csv`](./data/act_2019.csv): 2019 ACT Scores by State ([source](https://blog.prepscholar.com/act-scores-by-state-averages-highs-and-lows))
* [`sat_2017.csv`](./data/sat_2017.csv): 2017 SAT Scores by State ([source](https://blog.collegevine.com/here-are-the-average-sat-scores-by-state/))
* [`sat_2018.csv`](./data/sat_2018.csv): 2018 SAT Scores by State ([source](https://blog.collegevine.com/here-are-the-average-sat-scores-by-state/))
* [`sat_2019.csv`](./data/sat_2019.csv): 2019 SAT Scores by State ([source](https://blog.prepscholar.com/average-sat-scores-by-state-most-recent))
* [`sat_act_by_college.csv`](./data/sat_act_by_college.csv): Ranges of Accepted ACT & SAT Student Scores by Colleges ([source](https://www.compassprep.com/college-profiles/))

#### External Data
* [`2019-2020_alt_criteria`](https://nces.ed.gov/programs/digest/d21/tables/dt21_305.30.asp?current=yes): Number and percentage of degree-granting postsecondary institutions with first-year undergraduates using various selection criteria for admission, by control and level of institution

#### Data Dictionary
---
|Feature|Type|Dataset|Description|
|---|---|---|---|
|accept_rate|float|College Admissions|Average acceptance rate|
|act_q1|float|College Admissions|Admitted Students 
|act_q2|float|College Admissions|
|composite|float|ACT/SAT|
|ebrw|integer|SAT
|math|integer|SAT|
|number_of_applicants|College Admissions|
|participation|float|ACT/SAT|
|policy_details|object|College Admissions|
|policy_period|float|College Admissions|
|sat_q1|float|College Admissions|
|sat_q2|float|College Admissions|
|school|object|College Admissions|
|state|object|ACT/SAT|
|test_optional?|integer|College Admissions|
|total|integer|SAT|
|year|integer|ACT/SAT|

## Exploratory Data Analysis
---
The EDA was performed to address the following questions:
1. How do the scores of schools with high participation rates for both tests compare?
2.  What are the trends in national SAT/ACT participation rates over the last three years?
3. What are the trends in national SAT/ACT scores over the last three years?
4. How do national averages differ from admitted students performances at test-optional and test-required schools?
5. How do the scores of schools with high acceptance rates compare to those with low acceptance rates?
6. What is the correlation between scores of admitted students and university's acceptance rates?
7. For the schools that are test optional what is their acceptance rate?
8. What is the correlation between scores of admitted students and the university's test optional policies?
9. Based on acceptance rates, what SAT/ACT scores are being accepted into test_optional schools? 
10. Based on acceptance rates, what SAT/ACT scores are being accepted into test_required schools? 

## Conclusions and Recommendations
---
Correlation values clearly showed the very high positive relationships between admitted student scores on the ACT and SAT. This could be inferred, since each row is for an individual school that has it's own criteria. However, this result is useful to schools that want to compare themselves to a school with a similar scoring profile.

Additionally, strong correlations exist between acceptance rate and ACT/SAT quartile scores, so schools were compared based on these factors. 

Of the 9 high performing/highly competitive schools, UChicago was the only one that had a permanent test-optional policy. If the other 8 looked to standardize their testing policies to align with UChicago, it is hoped that this project could assist in that effort. Further this action would be recommended based on the disparities that could exist due to the negative trends in state participation and performance. Trends in admittance based on demographic data could be evaluated to further support these claims.

Further consideration was given to findings that showed the competitive nature of the admissions process where there were higher scores for schools with low acceptance rates. It is possible that there may be more barriers to admittance for students in states with high testing participation since it was found that the students are more likely to score lower on the test, decreasing their chance of admittance.

A counter-argument to this recommendation could be that some schools may benefit from exclusive and competitive acceptance rates and admitted scores. To that point, further research would have to be done on *how*, and if so, *when* low national scoring averages would impact these institutions' applicant pools. From here, the effect of these trends on revenue and costs could be addressed.

## Cited Sources
---
- [ACT.org](https://www.act.org/content/act/en/products-and-services/the-act/scores/understanding-your-scores.html)
- [College Vine](https://blog.collegevine.com/here-are-the-average-sat-scores-by-state/)
- [Dropping SAT and ACT requirements from CNN](Dropping SAT and ACT requirements)
- [Compass Prep](https://www.compassprep.com/college-profiles/)
- [A History of the SAT and ACT by Minot Daily News](https://www.minotdailynews.com/news/local-news/2017/04/a-brief-history-of-the-sat-and-act/)
- [National Center for Education Statistics](https://nces.ed.gov/programs/digest/current_tables.asp)
- [Princeton Review on SAT Section](https://www.princetonreview.com/college/sat-sections)

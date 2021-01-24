# School District Analysis
Using data analytics packages to gain unique insights on school performance

## Overview

### Purpose

The purpose of this analysis was to explore historic data from district and charter schools in the US, and to try and determine unique insights based off metrics like budget, population, and test scores. We use pandas DataFrames and some functions from the NumPy library to clean the initial dataset, and then omit certain values based off exclusion parameters (suspicion of academic dishonesty). We then conduct some summary statistics by arbitrarily grouping schools into different categories, like population or per-capita budget.

Technologies Used:

* Python 3.7.6 & Jupyter Notebook
* Modules: pandas, NumPy
* Data Source: schools_data_set, students_data_set (.csv)

## Results

The initial analysis contained data from Thomas High School's 9th grade class. However, it is later determined that this class was under suspicion for rampant academic dishonesty. So as not to corrupt the remaining analysis, the choice was made to exclude this class.

Once the exclusion was made, some key differences were apparent:

### District Summary

| Description              | DataFrame                                                  |
|--------------------------|------------------------------------------------------------|
| District Summary: Before | ![District_before](Resources/district_analysis_before.png) |
| District Summary: After  | ![District_before](Resources/district_analysis_after.png)  |

- **Conclusion:** No significant changes were seen when excluding Thomas High School's 9th grade class from the original analysis
--------------------------------------
### School Summary

| Description                                            | DataFrame                                              |
|--------------------------------------------------------|--------------------------------------------------------|
| School Summary: Before                                 | ![School_before](Resources/school_analysis_before.png) |
| School Summary: THS 9th Grade removed                  | ![School_9thNaN](Resources/school_analysis_9thNaN.png) |
| School Summary: After replacing with THS 10-12th Grade | ![School_after](Resources/school_analysis_after.png)   |

- **Conclusion:** As seen, there was no significant changes seen when excluding the 9th grade class of Thomas High School from the analysis. In the modified dataset, the 10-12th grade scores are similar to what was seen before when the 9th grade data was included
--------------------------------------

### Math Scores By Grade

| Description                  | DataFrame                                              |
|------------------------------|--------------------------------------------------------|
| Math Scores by Grade: Before | ![Math_before](Resources/math_scores_grade_before.png) |
| Math Scores by Grade: After  | ![Math_after](Resources/math_scores_grade_after.png)   |

### Reading Scores By Grade

| Description                     | DataFrame                                                    |
|---------------------------------|--------------------------------------------------------------|
| Reading Scores by Grade: Before | ![reading_before](Resources/reading_scores_grade_before.png) |
| Reading Scores by Grade: After  | ![reading_after](Resources/reading_scores_grade_after.png)   |

- **Conclusion:** No changes were expected to this report, except the exclusion of Thomas High School's 9th grade data. In both DataFrames, it now reads as `Nan`.
--------------------------------------

### Scores by Per-Student Capita

| Description                          | DataFrame                                                 |
|--------------------------------------|-----------------------------------------------------------|
| Scores by Per-Student Capita: Before | ![capita_before](Resources/scores_by_spending_before.png) |
| Scores by Per-Student Capita: After  | ![capita_after](Resources/scores_by_spending_after.png)   |

- Conclusion: No changes were seen in the before & after reports
--------------------------------------
### Scores by School Size

| Description            | DataFrame                                           |
|------------------------|-----------------------------------------------------|
| Scores by Size: Before | ![size_before](Resources/scores_by_size_before.png) |
| Scores by Size: After  | ![size_after](Resources/scores_by_size_after.png)   |

- Conclusion: No changes were seen in the before & after reports
--------------------------------------
### Scores by School Type (District vs Charter)

| Description            | DataFrame                                           |
|------------------------|-----------------------------------------------------|
| Scores by Type: Before | ![type_before](Resources/scores_by_type_before.png) |
| Scores by Type: After  | ![type_after](Resources/scores_by_type_after.png)   |

- Conclusion: No changes were seen in the before & after reports 
--------------------------------------

## Summary

**Four major changes between the original analysis and the updated analysis:**

- The updated analysis' 9th grade data in the Math and Reading Scores by Grade DataFrames are now removed and replaced with NaN
- The total number of students in the district decreased from 39,170 to 38,709 due to the exclusion of THS' 9th grade data
- Almost all scores in the district summary after slightly lower than the original analysis, but not enough to provide a significant signal
- The overall passing percentage of Thomas High School dropped from 90.95%  to 90.63%




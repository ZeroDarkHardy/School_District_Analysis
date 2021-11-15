# School_District_Analysis

## Project Overview

### Given a large amount of student and school related data, we've been tasked with analyzing student grade performace to find if there's any correlation to school funding, school size, or school type (district or charter).  Additionally, in light of potential academic dishonesty in the testing results of a specific group of students (9th graders from Thomas High School), we refactored the parameters of the analysis to make sure that per-student averages weren't unfairly weighted or erroneously skewed.
---
## Resources
**Source Files:** schools_complete.csv, students_complete.csv
**Python Code (via Jupyter Notebook):** PyCitySchools_Challenge.ipynb, PyCitySchools.ipynb
**Software:** Python 3.7.10, Anaconda, Jupyter Notebook, Visual Studio Code 1.62.1

## Results
Potential academic dishonesty was observed within our data sample, neccesitating the exclusion of all data pertaining to the 9th grade class at Thomas High School (all values for THS 9th grade test results replaced with NaN).  Below we will compare the previous and current outputs, before and after the data was re-averaged to consider the ineligible test results.

### District Summary
- (ORIGINAL OUTPUT)
![ORIGINAL DISTRICT SUMMARY](https://github.com/ZeroDarkHardy/School_District_Analysis/blob/main/Resources/district_summary_df_old1.png)
- (RECALCULATED OUTPUT)
![RECALCULATED DISTRICT SUMMARY](https://github.com/ZeroDarkHardy/School_District_Analysis/blob/main/Resources/district_summary_df_new.png)



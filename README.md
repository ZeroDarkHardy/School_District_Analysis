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
    - The impact of the recaculations to the district summary as a whole were minimal, though we do see a few small categoric value decreases.  This suggests that if there was, in fact, academic dishonesty among the scores that were ultimately ommitted, those scores had been skewed above the district averages.
    - The average student math score decreased from 79.0 to 78.9.
    - The percentage of students passing math fell from 75% to 74.8%.
    - While the average student reading score remained the same (81.9), the percentage of students passing reading fell from 86% to 85.7%.
    - The percentage of students passing all subjects fell from 65% to 64.9%

### School Summary (Thomas High School)
- (ORIGINAL OUTPUT)
![ORIGINAL THS SUMMARY](https://github.com/ZeroDarkHardy/School_District_Analysis/blob/main/Resources/ths_summary_old1.png)
- (OUTPUT AFTER 9TH GRADE RESULTS REPLACED WITH "NaN")
![NAN THS SUMMARY](https://github.com/ZeroDarkHardy/School_District_Analysis/blob/main/Resources/ths_summary_old.png)
- (OUTPUT AFTER RESULTS RE-AVERAGED FOR UPDATED STUDENT COUNT)
![NEW THS SUMMARY](https://github.com/ZeroDarkHardy/School_District_Analysis/blob/main/Resources/ths_summary_new.png)



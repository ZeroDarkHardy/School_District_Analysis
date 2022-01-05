# School_District_Analysis

[Project Overview](#project-overview)

[Resources](#resources)

[Results](#results)

- [District Summary](#district-summary)
- [School Summary](#school-summary-thomas-high-school)
- [THS vs. Other Schools](#How-does-the-recalculation-affect-Thomas-High-Schools-performance-relative-to-other-schools)
- [Math and Reading Scores by Grade](#math-and-reading-scores-by-grade)
- [Scores by School Spending](#scores-by-school-spending)
- [Scores by School Size](#scores-by-school-size)
- [Scores by School Type](#scores-by-school-type)

[Summary](#summary)

## Project Overview

Given a large amount of student and school related data, we've been tasked with analyzing student grade performace to find if there's any correlation to school funding, school size, or school type (district or charter).  Additionally, in light of potential academic dishonesty in the testing results of a specific group of students (9th graders from Thomas High School), we refactored the parameters of the analysis to make sure that per-student averages weren't unfairly weighted or erroneously skewed.

---

## Resources
**Source Files:** [schools_complete.csv](https://github.com/ZeroDarkHardy/School_District_Analysis/blob/main/Resources/schools_complete.csv), [students_complete.csv](https://github.com/ZeroDarkHardy/School_District_Analysis/blob/main/Resources/students_complete.csv)

**Python Code (via Jupyter Notebook):** [PyCitySchools_Challenge.ipynb](https://github.com/ZeroDarkHardy/School_District_Analysis/blob/main/PyCitySchools_Challenge.ipynb), [PyCitySchools.ipynb](https://github.com/ZeroDarkHardy/School_District_Analysis/blob/main/PyCitySchools.ipynb)

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
Here we see the following:  The original analysis results for Thomas High School, the ouput of the same code with the 9th graded results replaced with "NaN", and finally the output once those results had been refactored to consider an eligible student count...
- (ORIGINAL OUTPUT)
![ORIGINAL THS SUMMARY](https://github.com/ZeroDarkHardy/School_District_Analysis/blob/main/Resources/ths_summary_old1.png)
- (OUTPUT AFTER 9TH GRADE RESULTS REPLACED WITH "NaN")
![NAN THS SUMMARY](https://github.com/ZeroDarkHardy/School_District_Analysis/blob/main/Resources/ths_summary_old.png)
- (OUTPUT AFTER RESULTS RE-AVERAGED FOR UPDATED STUDENT COUNT)
![NEW THS SUMMARY](https://github.com/ZeroDarkHardy/School_District_Analysis/blob/main/Resources/ths_summary_new.png)
    - While we see a dramatic (though predictable) swing in average values once the 9th grade test results are initially disqualified, we only see a marginal difference from the original results once the remaining THS grades have been re-averaged.
    - The average THS math score fell by less than a tenth of a percent, from 83.41 to 83.35
    - The average THS reading score **increased** from 83.84 to 83.89, though the percentage of students passing reading fell from 97.30% to 97.01%.
    - The percentage of students passing math fell very slightly, from 93.27% to 93.18%.
    - In the end, the overall percentage of students passing both subjects at Thomas High School fell from 90.95% to 90.63%.

### How does the recalculation affect Thomas High School's performance, relative to other schools?
- (TOP 5 SCHOOLS, ORIGINAL OUTPUT)
![TOP SCHOOLS OLD OUTPUT](https://github.com/ZeroDarkHardy/School_District_Analysis/blob/main/Resources/top_schools_old.png)
- (TOP 5 SCHOOLS, RECALCULATED OUTPUT)
![TOP SCHOOLS NEW OUTPUT](https://github.com/ZeroDarkHardy/School_District_Analysis/blob/main/Resources/top_schools_new.png)
    - While we do see the above mentioned value changes for Thomas High School's grading averages, the changes aren't great enough to unseat THS from second place on the list of the district's top 5 schools.

### Math and Reading Scores By Grade
![SCORES BY GRADE OLD OUTPUT](https://github.com/ZeroDarkHardy/School_District_Analysis/blob/main/Resources/per_grade_scores_gallery_old.png)
![SCORES BY GRADE NEW OUTPUT](https://github.com/ZeroDarkHardy/School_District_Analysis/blob/main/Resources/per_grade_scores_gallery_new.png)
- As we can see by comparing the original and new ouputs for the average subject scores by grade, removing the 9th grade THS scores had absolutely no numeric impact on the DataFrames other than to replace the scores with "nan".

### Scores by School Spending
- (ORIGINAL OUTPUT)
![SPENDING SCORES ORIGINAL OUTPUT](https://github.com/ZeroDarkHardy/School_District_Analysis/blob/main/Resources/spending_summary_df_old.png)
- (RECALCULATED OUTPUT)
![SPENDING SCORES NEW OUTPUT](https://github.com/ZeroDarkHardy/School_District_Analysis/blob/main/Resources/spending_summary_df_new.png)
    - The recalculated data shows that the impact of removing the 9th grade THS students wasn't enough to impact the district averages, when the schools are broken down by per-student-capita.

### Scores by School Size
- (ORIGINAL OUTPUT)
![ORIGINAL SCHOOL SIZE OUTPUT](https://github.com/ZeroDarkHardy/School_District_Analysis/blob/main/Resources/size_summary_df_old.png)
- (RECALCULATED OUTPUT)
![UPDATED SCHOOL SIZE OUTPUT](https://github.com/ZeroDarkHardy/School_District_Analysis/blob/main/Resources/size_summary_df_new.png)
    - As with the scores by school spending, the impact of recalculating the student score averages weren't large enough to alter our output, at least to the degree of precision required.

### Scores by School Type
- (ORIGINAL OUTPUT)
![ORIGINAL SCHOOL TYPE OUTPUT](https://github.com/ZeroDarkHardy/School_District_Analysis/blob/main/Resources/type_summary_df_old.png)
- (RECALCULATED OUTPUT)
![UPDATED SCHOOL TYPE OUTPUT](https://github.com/ZeroDarkHardy/School_District_Analysis/blob/main/Resources/type_summary_df_new.png)
    - Once more, the dataframes before and after the ommision of 9th grade THS students weren't enough to impact overall district metrics when grouped with other schools of matching type.
---
## Summary
If we had not updated the total student counts for both THS and the district to reflect the disqualified student class, it would have unfairly skewed every metric and brought down averages across the board. After refactoring the code to exclude those students from the total counts, we found that the impact was only really visible at higher degrees of precision.  We saw minor impacts to the math scores, reading scores, and passing percentages within Thomas High School's metrics, but usually usually less than a single unit of measurement, which wasn't enough to impact the district averages on the whole.


# Overview of the school district analysis:
  The School Board would like to understand various performance metrics of the different school districts and schools. We will first work with Maria (our contact) provide the initial analysis based on data collected from many students and schools across the school district.
While the School Board is pleased with the insight that we have provided in our work with Maria, it has been identified that there appears to be some anomalies in the data, in particular in the math and reading scores of the grade nine students at Thomas High School. In order to ensure these results do not skew the analysis, the Boad has asked us to again work with Maria to remove the impact of these results by changing all the grade 9 Thomas High School math and reading scores to Nan (which is a null value).
The School Board will like to understand the impact of changing all the grade 9 math and reading scores at Thomas High School to Nan - we will now review how this change impacted various parts of the analysis relative to when it was ran including the Thomas High School grade 9th scores.
Although the school board does not know the full extent of the academic dishonesty, they want to uphold state-testing standards and have turned to Maria for help.

# Purpose :
  In this analysis,  we used pandas and numpy libraries to find various metrics school board asked for.
1. Open Jupyter Notebook files from local directories using a development environment.
2. Read an external CSV file into a DataFrame.
3. Format a DataFrame column.
4. Determine data types of row values in a DataFrame.
5. Retrieve data from specific columns of a DataFrame.
6. Merge, filter, slice, and sort a DataFrame.
7. Apply the groupby() function to a DataFrame.
8. Use multiple methods to perform a function on a DataFrame.
9. Perform mathematical calculations on columns of a DataFrame or Series.


# Results :

## How does district summary affected?
![School_district_summary)](/Resources/School_district_summary.png)
  The change of adding Nan to all grade 9 and Thomas High School math and reading scores did not have a large impact on the district analysis, with each metric decresing by less that 0.5 percentage point each (meaning scores changed by less than 0.5%). It's important to consider there are only 461 students in grade 9 at Thomas High School, and given the total student count is 39,170, the grade 9 students only make up 1.2% of the total student count, so removing their math and reading scores can only impact the averages so much.

## How does the school summary  affected ?
![per_school_summary](/Resources/per_school_summary.png)

![per_school_summary_updated)](/Resources/per_school_summary_updated.png)

1. The ranking of the top schools including Thomas High School was not affected by the update.
While the average math, reading and overall scores at Thomas High School were impacted with the update, the changes were not enough to change its relative ranking versus other schools. The changes only had a small impact of less than a change of 1 percentage point on each metric.


2. The ranking of the bottom schools was not affected by the update as the only metrics impacted where at Thomas High School as we are looking at each school's scores.


## Math and reading scores by grade :
1. Math scores by grade:

![math_scores_by_grade](/Resources/math_scores_by_grade.png)

2. Reading scores by grade:

![reading_scores_by_grade](/Resources/reading_scores_by_grade.png)

The only score that is impacted on this DataFrame is that the grade 9 students at Thomas High School have Nan instead of a grade for both math and reading. If we ran a sum or mean of the DataFrame, we would see a difference between the orignal and updated.


##  Scores by school spending :
![spending_summary_per_student](/Resources/spending_summary_per_student.png)
 There was a slight change in the scores by school spending groups scores for the $630-644 per student grouping as this is where Thomas High School is grouped, however the change is small with each metric changing less than 0.1 percentage points (or change of less than 0.1%).
 

##  Scores by school size:

![size_summary](/Resources/size_summary.png)

The scores for the Medium (1000-2000) size schools changed slightly (less than 1 percentage point as we have seen with other calculations above). They were impacted as Thomas High School included in this group as it has 1,635 students who attend (including the grade 9 students).
 Thomas High School is a Charter type school, so this is why we see changes to the scores for Charter (again less than change of 0.1% each metric), but no changes to District type school scores as Thomas High School not part of that group and no other school scores were affected.


## Scores by school type:
![type_summary](/Resources/type_summary.png)
Thomas High School is a Charter type school, so this is why we see changes to the scores for Charter (again less than change of 0.1% each metric), but no changes to District type school scores as Thomas High School not part of that group and no other school scores were affected.


# Summary :

District Analysis - changes to all scores by less than 0.5 percentage points (or change by less than 0.5%) - no impact to school or student count.
Top School Ranking - no change to ranking, however Thomas High School scores did change, but by less than 1 percentage point (or changed by less than 1%) for each metric.
Scores by School Size - changes to Medium (1000-2000) grouping for all scores by less than 0.1 percentage points (or change by less than 0.1%).
Scores by School Type - chages to Charter type grouping for all scores by less than 0.1 percentage points (or change by less than 0.1%).

# School_District_Analysis

## Project and Challenge Overview:
The project consisted of assisting the School District's Superintendent in replacing some students' grades that had been altered, from the Thomas High School's 9th grade, without affecting the rest of the data from that school, and reanalyzing the overall metrics for the School District.

1. How is the District Summary affected?
2. How is the School Summary affected?
3. How does replacing the ninth graders’ math and reading scores affect Thomas High School’s performance, relative to the other schools?
4. How does replacing the ninth-grade scores affect the following?
* Math and Reading Scores by Grade
* Scores by School Spending
* Scores by School Size
* Scores by School Type

## Resources
- Data source: schools_complete.csv, students_complete.csv, clean_students_complete.csv
- Software: Python 3.7.6, Jupyter Notebook

## Summary
The analysis has shown:

__1. How is the District Summary affected?__\
The District Summary was marginally affected, since all metrics shown are averages throughout all schools in the district. This minimizes the effect that changing the scores from a single grade, from a single school might've had in the district's overall metrics.

__2. How is the School Summary affected?__\
The passing percentages for both Math and Reading, as well as the Overall Passing Percentage were considerably affected by the alteration, while the average scores for Math and Reading were very minimally affected.

_The scores from the 9th grade having been replaced for "NaN" means that those scores are no longer accounted for in the count of students who have passed Math or Reading, since the calculation uses the "Score" columns. However, the students that those scores belonged to are still accounted for in the total student count, which counts the names in the "Student Names" column. With the denominator staying the same and the numerator being much reduced, the passing percentages end up very reduced as well._

_As for the averages, they were not very affected because the mean() method was applied to the "Score" columns and defaults to excluding "NaN" values when computing the result, thus returning virtually the same average Math and Reading scores._

__3. How does replacing the ninth graders’ math and reading scores affect Thomas High School’s performance, relative to the other schools?__\
Thomas High School has dropped in the ranking of Overall Passing Percentage from being the school with the 2nd highest passing percentage to 8th place.

__4. How does replacing the ninth-grade scores affect the following?__
* __Math and Reading Scores by Grade__\
The only scores that were affected by the alteration were those of Thomas High School's 9th grade specifically, for both Math and Reading. None of the other grades were affected.

* __Scores by School Spending__\
Like for "Scores by School Size", the only scores that were affected were those of the $630-644 range of spending per student, since that is the category of Thomas High School. The percentages of passing students were much more affected than the averages.

* __Scores by School Size__\
Like for "Scores by School Spending", the only scores that were affected were those of Medium schools (1000-2000), since that is the category of Thomas High School. The percentages of passing students were much more affected than the averages.

* __Scores by School Type__\
The removed scores for the 9th grade have reduced the percentage of students who passed Math, Reading and Overall Passing percentage for Charter schools only, since that is the Thomas High School's type of school. The average Math and Reading scores, however, have not been affected.

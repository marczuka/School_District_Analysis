# School_District_Analysis
Performing school data analysis using Anaconda, Jupiter Notebook and Pandas library. 
The analysis contains the following reports.

## District Summary Report
This reposrt presents the following information for the district:
- Total Number of Schools
- Total Number of Students
- Total Budget
- Average Math Score
- Average Reading Score
- % of Students Passing Math
- % of Students Passing Reading
- % Overal Passing (% of Students who passed both Math and Reading)

## School Summary Report
This report presents the following information for each school in the district:
- Type of school in the "School Type" column
- Total number of students per school in the "Total Students" column
- Total budget per school in the "Total School Budget" column
- Total budget per student for each school in the "Per Student Budget" column
- Average math score for each school in the "Average Math Score" column
- Average reading score for each school in the "Average Reading Score" column
- Percentage of students passing math for each school in the "% Passing Math" column
- Percentage of students passing reading for each school in the "% Passing Reading" column
- Overall passing percentage for each school in the "% Overall Passing" column

## High and Low Performing Schools
...

## Average Math and Reading Scores by grade
...

## Group Scores by School Spending per Student
This report segregates all the schools in the district into 4 spending bins depending on the budget per student:
- 1st bin: <$584 budget per student,
- 2nd bin: $585-629 budget per student, 
- 3rd bin: $630-644 budget per student, 
- 4th bin: $645-675 budget per student.

For each bin the following information is presented:
- Average math score in the "Average Math Score" column
- Average reading score in the "Average Reading Score" column
- Percentage of students passing math in the "% Passing Math" column
- Percentage of students passing reading in the "% Passing Reading" column
- Overall passing percentage in the "% Overall Passing" column

## Group Scores by School Size
This report segregates all the schools in the district into 3 bins depending on the size of the school:
- Small bin: less than 1000 students, 
- Medium bin: 1000-2000 students, 
- Large bin: 2000-5000 students.

For each bin the following information is presented:
- Average math score in the "Average Math Score" column
- Average reading score in the "Average Reading Score" column
- Percentage of students passing math in the "% Passing Math" column
- Percentage of students passing reading in the "% Passing Reading" column
- Overall passing percentage in the "% Overall Passing" column

## Group Scores by School Type
This report separates all the schools into two groups: Charter schools and District schools.

For each group the following information is presented:
- Average math score in the "Average Math Score" column
- Average reading score in the "Average Reading Score" column
- Percentage of students passing math in the "% Passing Math" column
- Percentage of students passing reading in the "% Passing Reading" column
- Overall passing percentage in the "% Overall Passing" column


## Challenge Analysis
Since the grades for the ninth graders at Thomas High School have been changed our task was to recalculate the reports for all the schools in the district without the data for the ninth graders of the Thomas High School.

To acomplish the calculations we first replaced the math and reading scores for the ninth graders at Thomas High School with "NaN" which means that value is unknown. That is about 1% of the total number of students in the district. We have kept all the personal information about the students (as name, gender, school and grade) for the above students.

### District Summary Report
This report was affected by the loss of data for the ninth graders at Thomas High School very slightly: only percentage values have changed by 1%. 

The following values were affected:
- % of Students Passing Math
- % of Students Passing Reading
- % Overal Passing

Even though the values were affected - 1% difference does not seem significant so the district information seems to remain informative and trustworthy dispite the data loss.

### School Summary Report
The loss of data for the ninth graders at Thomas High School only affected the values for the Thomas High School in this report (all the values for other schools remained intact).

The following values were affected:
- Avarage Math Score became 0,1% higher
- % Passing Math decreased significantly (more than 25%)
- % Passing Reading decreased signigicantly (more than 25%)
- % Overall Passing decreased significantly (more than 25%)

Average scores for the Thomas High school remained almost intact. However passing percentages have decreased significantly: % of students passing math now is significantly lower than for other Charter schools, and the % of sudents passing reading is the lowest among all the schools (District and Charter) which does seem very unusual. The overall % of students passing both math and reading for Thomas High is also significantly lower than for other Charter schools in the district. The information for about 1/3 of the students for Thomas High School is unknown.
All of the above makes the school summary report for this school not informative. 
We need to get the changed values and recalculate the data.

### High and Low Performing Schools
The Thomas High school lost its second place in the top five schools and moved to the eighth place. Bottom five schools remain the same. This report needs to be recalculated when the changed values for the Thomas High become availbale.

### Average Math and Reading Scores by grade
These two reports don't have data for the 9th grade of Thomas High School. All other values in the reports remained intact.

### Group Scores by School Spending per Student
The percentages of students passing math, reading and both subjects have changed for the third spending bin ($630-$644 per student) since the Thomas High School has $638 budget per student.

The foloowing values have changed:
- % Passing Math decreased less than 10%
- % Passing Reading decreased less than 10%
- % Overall Passing decreased less than 10%

Even though the percentage values for the third spending bin decreased the overall picture presented by the report remained the same: it seems that the bigger is budget per student - the lower average scores and passing percentages the school gets. 
My conclusion is that budget per student is not the key factor deciding about academic indicators.

### Group Scores by School Size
Since the Thomas school have 1635 students the values have only changed for the Medium size bin (1000-2000 students).

The following values have changed:
- % Passing Math decreased less than 10%
- % Passing Reading decreased less than 10%
- % Overall Passing decreased less than 10%

Even though the percentage values for the Medium bin have changed the overall picture presented by the report remains intact. It looks even more proportional now: the bigger is the school - the lower are the passing percentages. This can be explained logically: students in the small schools receive more attention per student than in the big schools.

### Group Scores by School Type
Since the Thomas school is a Charter school the values have only changed for the Charter schools group.

The following values have changed:
- % Passing Math decreased less than 5%
- % Passing Reading decreased less than 5%
- % Overall Passing decreased less than 5%

Even though the percentage values for one group have changed the overall picture presented by the report remains intact: Charter schools present better academic indicators than the District schools.

### Conclusion
Most of the reports for the school district were not affected by the change of data for one grade in one single school.
However taking into account the above analysis we do have a reason to suspect that presented values of the ninth graders in Thomas High School might have been significantly higher than the real ones (some kind of cheating might have taken place). 
The analysis for the Thomas High School needs to be remade when the changed values are available.

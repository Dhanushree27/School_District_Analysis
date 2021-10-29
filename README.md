# School Data Analysis Project

## Overview of the project
This project was undertaken to assist Maria with the analysis of student data. The dataset consisted of two files: 
- 'students_complete.csv' with 39,170 student data from 14 schools in the district
- 'school_complete.csv' with details of the 14 schools, such as type, size and budget

The purpose of the analysis was to determine:
- A high-level snapshot of the district's key metrics
- An overview of the key metrics for each school
- Top 5 and bottom 5 performing schools, based on the overall passing rate
- The average math score received by students in each grade level at each school
- The average reading score received by students in each grade level at each school
- School performance based on the budget per student
- School performance based on the school size 
- School performance based on the type of school

The analysis was carried out using the Python, specifically the 'Pandas' library. It was later notified that the math and reading scores for ninth grade students of Thomas High school were modified. Taking this into consideration, the analysis was repeated by replacing the altered scores with 'NaN'. The results from the analysis and the differences observed have been explained in detail in this report.

## Results
The scores for ninth grade Thomas High School students were altered, requiring a second analysis of the dataset. Replacing the values with 'NaN' resulted in the following changes in the results:

### Effect on district summary
To reduce the impact of 'NaN' values on percentage passing, the total count was recalculated by ignoring the count of students in ninth grade in Thomas High School. The resultant values showed that there was not much of an impact on the overall district's performance. 
**Result:** Minimal impact

![District_Summary]'Resources/Images/District_Summary.png') 

![District_Summary_Updated]Resources/Images/District_Summary_Challenge.png)

### Effect on school summary
For the school summary, the summary of all the schools were calculated normally first. This calculation resulted in skewed data, since the values for ninth grade students were 'NaN'. This was not a proper reflection of the performance of the other grade students.

![School_Summary_WithNaN]Resources/Images/School_Summary_WithNaN.png)

To correct the skew, the count of Thomas High School students who had passed math, reading, both math and reading was recalculated. The percentage was then determined using the recalculated values. This revealed that there was not much of an impact on the school's overall performance due to the altered values. The altered ninth grade values did not impact the school's performance. 
**Result:** Minimal impact

![School_Summary]'Resources/Images/School_Summary.png') 

![School_Summary_Updated]Resources/Images/School_Summary_Challenge.png)

### Relative ranking of Thomas High School
Though there was not a considerable difference in '% Overall Passing' of Thomas High School after the removal of ninth grade scores, there was a slight reduction of 
**0.31**. Despite this reduction, Thomas High School remained in the second position in the list of top 5 schools
**Result:** No impact

![Top_Schools]'Resources/Images/Top_Schools.png')

### Math and Reading scores by grade
Since the scores of 9th grade students of Thomas High School were replaced with NaN, it was not possible to compute the grade average for math and reading for the same. Also, there was no impact on the other values as there was no relationship between each grade, or school
**Result:** Incomputable. No impact on other values

### Scores by School Spending
The schools were categorized into 5 bins based on the budget. Thomas High School fell into the '$620-644' bin. There was no observed difference in the values since the alteration had not impacted the summary statistics greatly.
**Result:** No impact

### Scores by School Size
The schools were categorized into 3 bins based on the size. Thomas High School fell into the 'Medium (1000-2000)' bin. Again, there was no observed difference in the values since the alteration had not impacted the summary statistics greatly.
**Result:** No impact

### Scores by School Type
The dataset already had information on school type. Schools were categorized into District or Charted school. Thomas High School was a 'Charter' school. Again, there was no observed difference in the values since the alteration had not impacted the summary statistics greatly.
**Result:** No impact

## Summary
Despite the alteration, it was observed that there was no major impact on the summary statistics, nor on the analysis carried out using the statistical data. Minor differences observed:
### District Summary
- Minor change on math average and percentage: Average math score by 0.1 and Percentage math score dropped by 0.2
- This was also reflected on the % Overall Passing where the value had dropped by 0.3
### School Summary
- Averages: Math average had dropped by 0.06 whereas reading average had increased by 0.05
- Percentage: Math average had dropped by 0.09 and reading average had dropped by 0.29
- The overall percentage also showed a drop by 0.31

Overall, the changes were negligible. Major differences would have been observed if the calculations had not accounted for the NaN values, as shown in the school summary calculated considering all values.

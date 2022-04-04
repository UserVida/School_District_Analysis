# School_District_Analysis

## Overview of School District Analysis

### Purpose

The purpose of this project was to analyze school district data to discover trends in student academic performances of high schools within a school district. The school district data was provided in two csv files; one with the student data and the other with the school data. These two files were merged together in the juptyer notebook environment using python code and the pandas library. The data was then aggregated to remove personal identifiable information and to perform calculations on. These calculations were used to create different metrics to examine the difference between standaridized test scores and other school variables such as budget and school size. 

Due the the discovery of altered and incorrect data, the values for the 9th grade standardized test results for Thomas High School were replaced with NaN (Not a Number) values using a function from the numpy library. All calculations and analyses were adjusted accordingly to factor in these NaN values. 


### Project Overview
Recreate the school district analysis and following metrics to adjust for the NaN values:
1. The district summary
2. The school summary
3. The top 5 and bottom 5 performing schools, based on the overall passing rate
4. The average math score for each grade level from each school
5. The average reading score for each grade level from each school
6. The scores by school spending per student, by school size, and by school type

### Resources
* Data Source: students_complete.csv, schools_complete.csv
* Software: Jupyter Notebook 6.4.5, Python 3.7.11
* Python Libraries: Pandas library, NumPy library 

<br>

##  Results

### School District Summary

![origdis_summary](https://user-images.githubusercontent.com/97644424/161448833-4b518907-e7ec-4b47-a879-7778f16266ad.png)
![adjdis_summary](https://user-images.githubusercontent.com/97644424/161448895-566c787f-a399-49f2-9f6b-fab25f5e9e78.png)<br>
<br>

* The removal of the 9th grade math and reading scores of Thomas High School affected the school district summary in the following four ways:
  * The average math score dropped by **0.9%**, from 79% to **78.9%**.
  * The percentage of students passing math dropped by **0.2%**, from 75% to **74.8%**.
  * The percentage of students passing reading dropped by **0.3%**, from 86% to **85.7%**.
  * The percentage of students passing overall dropped by **0.1%**, from 65% to **64.9%**.

<br>

### School Summary

![THSOrgAdjScores](https://user-images.githubusercontent.com/97644424/161460552-9750238f-7ba3-4b01-9ab4-5d6871635cb8.png)
> Code used: per_school_summary_df["Average Math Score"].sort_values(ascending=False)
>> per_school_summary_df["% Passing Reading"].sort_values(ascending=False)

* The school summary metrics for Thomas High School were affected in 2 significant ways: 
  * For the average math score in the per school summary, Thomas High School fell from the 4th position (83.413348) on the list to the 6th position (83.350937)
  * For the percentage of students passing reading in the per school summary, Thomas High School fell from the 1st position (97.308869%) to the 3rd position  (97.018739%) 
 
* For the rest of the metrics, the position of Thomas High School in comparision to the other schools remain unchanged but the scores changed very slightly.
   * Average reading score:  rose by **0.047145%** from 83.848930% to **83.896082%**
   * Percentage of students passing math: dropped by **0.086481%** from 93.272171% to **93.185690%**
   * Percentage of students passing overall: dropped by **0.317688%** from 90.948012 to **90.630324%**

<br>

### Math and Reading Scores by Grade
<img src="https://user-images.githubusercontent.com/97644424/161467182-de237a1d-d14c-45fa-8e4f-301e4a0e1983.PNG" width="500" height="500"/>
* The math and reading scores for the 9th grade students in Thomas High School have been replaced with NaN values. 
 
 <br>
 <br>
 
### Scores by School Spending

![Spending Range Summary](https://user-images.githubusercontent.com/97644424/161467976-16ad4f7e-3a0c-42fd-bbe6-a55038f14ab7.png)
* The scores for the spending range ($631 - $645) all dropped by < 1 except for the "Average Reading Score" which rose by 0.011788. The change in scores is not dectectable when looking at the rounded values between the original and adjusted metric. 

<br>

### Scores by School Size

![SchoolSizeSummary](https://user-images.githubusercontent.com/97644424/161468538-4caa2737-c667-4709-a8af-c79bc12a6900.png)
 * The scores for the medium sized schools (1000 - 1999 students) all dropped by < 1 for all categories except the "Average Reading Score" which rose by 0.009431. The change in scores is not dectectable when looking at the rounded values between the original and adjusted metric. 

<br>

### Scores by School Type 

![SchoolTypeSummary](https://user-images.githubusercontent.com/97644424/161469121-61b282fa-b89b-496b-aa0a-bf5dd4b53793.png)
* The scores for the charter type schools all dropped by < 1. The change in scores is not dectectable when looking at the rounded values between the original and adjusted metric. 
  
<br>
  
## Summary of Differences 

Overall, any categories and metrics that included the student test result data for Thomas High School was affected by a change in values. These differences in values were less than 1 unit or percent; and most would go unnoticed if the score values had been rounded up. Most of the differences were decreases in score and percentage values but there were some exceptions were the score or percentage value actually increased. The summary of the changes to the district analysis are discussed below.

The removal of Thomas High School's 9th grade scores affected the average math and reading score categories, as well as the percentage passing categories of the entire school district. The "Average Math Score" and the "% Passing Reading" increased in value but the rest of the categories saw a decrease. 

As for each school summary, almost all categories related to score and percentage passing for Thomas High School's saw a drop in value. The only category that saw an increase in value was the "Average Reading Score". Although these differences were less than 1 unit/percent, it did cause Thomas High School's position ranking amongst the schools in the district to drop in the "Average Math Scores" and "% Passing Reading" categories to 6th and 3rd place respectfully from 4th and 1st place.

The changes in scoring values and percentage passing values only occured in the spending bin, size bin and school type that Thomas High School was categorized in. In other words, only the spending bin "$631 - $645", size bin "medium (1000-1999)" and school type "Charter" saw a difference in values. All these differences in scoring and percentage values were decreases of less than 1, with the exception of the "Average Reading Score" in the spending bin "$631 - $645" and in the size bin "medium (1000-1999)", which saw an increase of less than 1.

    


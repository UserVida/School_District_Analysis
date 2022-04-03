# School_District_Analysis

## Overview of School District Analysis

### Purpose

The purpose of this project was to analyze school district data to discover trends in student academic performances of high schools within a school district. The school district data was provided in two csv files, one with the student data and one with the school data. These two files were merged together in the juptyer notebook environment using python code and the pandas library. The data was then aggregated to remove personal identifiable information and to perform calculations on. These calculations were used to create different metrics to examine the difference between scores and other school factors such as budget and school size. 

Due the the discovery of altered and incorrect data, the values for the 9th grade standardized test results for Thomas High School were replaced with NaN (Not a Number) values using a function from the numpy library. All calculations and analyses were adjusted accordingly to factor in these NaN values. 


### Project Overview
Create the school district analysis and following metrics to adjust for the NaN values:
1. The district summary
2. The school summary
3. The top 5 and bottom 5 performing schools, based on the overall passing rate
4. The average math score for each grade level from each school
5. The average reading score for each grade level from each school
6. The scores by school spending per student, by school size, and by school type

### Resources
Jupyter Notebook
Python 3.7
Pandas library
NumPy library 

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

![THSAvgMathScores](https://user-images.githubusercontent.com/97644424/161452027-2f2fc2fe-3a4a-485f-906c-4e8a8d51674c.png)
> Code used: per_school_summary_df["Average Math Score"].sort_values(ascending=False)

* The school summary metrics for Thomas High School were affected in 2 significant ways: 
  * For the average math score in the per school summary, Thomas High School fell from the 4th position (83.413348) on the list to the 6th position (83.350937)
  * For the percentage of students passing reading in the per school summary, Thomas High School fell from the 1st position (97.308869%) to the 3rd position  (97.018739%) 
 
* For the rest of the metrics, the position of Thomas High School in comparision to the other schools remain unchanged but the scores changed very slightly.
   * Average reading score:  rose by **0.047145%** from 83.848930% to **83.896082%**
   * Percentage of students passing math: dropped by **0.086481%** from 93.272171% to **93.185690%**
   * Percentage of students passing overall: dropped by **0.317688%** from 90.948012 to **90.630324%**

### Math and Reading Scores by Grade


* The math and reading scores for the 9th grade students in Thomas High School have been replaced with NaN values. 
 
### Scores by School Spending
* The scores for the medium sized schools (1000 - 1999 students) all dropped by < 1. The change in scores is not dectectable when looking at the rounded values between the original and adjusted metric. 

### Scores by School Size
 * The scores for the medium sized schools (1000 - 1999 students) all dropped by < 1. The change in scores is not dectectable when looking at the rounded values between the original and adjusted metric. 

### Scores by School Type 
* The scores for the charter type schools all dropped by < 1. The change in scores is not dectectable when looking at the rounded values between the original and adjusted metric. 
  
## Summary of Differences 

The election audit script presented in this project can be utilized in other forms of elections with slight modifications. For the script to execute successfully, the tabulated data of votes must be in csv format. The code grabs the vote count, candidate name and county name from row indexes 0, 1 and 2 of the csv data. The codes assumes that all csv voting data will be organized in this order. To prevent misread row information, a code can be added to print the row headers in the terminal. If any of the rows in the csv file are not in the order assumed by the code, the index number used to retrieve the vote count, candidate name and county name can be changed to match the correct row. 


    


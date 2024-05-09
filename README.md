# Project1--Global-Data-Professionals-Benchmarking-Dashboard

##About Data:

This is the real world data taken by the 600-700 professionals like Data Analyst, Data Scientist, Data Engineers and more around the world.

##Problem Statement:

In today's data-driven business environment, organizations rely heavily on the expertise and performance of their data professionals to drive strategic decision-making and maintain a competitive edge. However, many organizations struggle with effectively benchmarking the performance of their data professionals across different regions globally. This lack of visibility into the capabilities, efficiency, and effectiveness of data professionals hinders organizations' ability to optimize talent management, resource allocation, and skill development initiatives

Also, Addressing these challenges requires the development of a comprehensive Global Data Professionals Benchmarking Dashboard that enables organizations to:

Gain visibility into the performance of data professionals across different regions.
Standardize metrics and KPIs for accurate benchmarking analysis.
Identify trends, patterns, and disparities to inform strategic decision-making.
Optimize talent management, resource allocation, and skill development initiatives based on data-driven insights.

### Steps followed 

- Step 1 : Load data into Power BI Desktop, dataset is a (.xlsx) file.
- Step 2 : Open power query editor & in view tab under Data preview section, check "column distribution", "column quality" & "column profile" options.
- Step 3 : Also since by default, profile will be opened only for 1000 rows so you need to select "column profiling based on entire dataset".
- Step 4 : It was observed that in some of the columns have errors & empty values were present.
- Step 5 : It was observed that Current Yearly Salary was in text datatype and it have salary in a range format like(105k-250k). For calculating average salary, first we have to split column by choosing digit to non-digit and then again Replace the 'k' value by blank values in the Current Yearly salary(2) and again by replacing the '-' value by blank value and again replace '+' by blank value. Then Replace the blank value in Current Yearly Salary (2) by 225 and change both the Current Yearly Salary(1) and Current Yearly Salary(2) datatype from text to whole number to calculate the average salary. 
- Step 6 :We calculate the average salary by adding custom column using DAX query-([#"Q3 - Current Yearly Salary (in USD).1"]+[#"Q3 - Current Yearly Salary (in USD).2"])/2
- Step 7 :Then we delete/remove some blank column present in the data named 'Browser', 'OS', 'City', 'Country'.
- Step 8 : In the data, there are several column like 'Q1 - Which Title Best Fits your Current Role?', 'Q4 - What Industry do you work in?', 'Q5 - Favorite Programming Language' there is row where professionals have specify the "Other" option so we have to split that by using left most delimiter "(" .

In the report view, under the view tab, theme was selected.

- Step 9 : Two Card Visuals were added to canvas to represent "Average Salary of Survey Taker" and "Average age of Survey Taker".

<img width="215" alt="Card" src="https://github.com/anchal765/Project1--Global-Data-Professionals-Benchmarking-Dashboard/assets/105012057/c90038ed-53a5-47a7-9da2-467fd4b09f95">

- Step 10 : To Represent " Happiness of Survey Takers with Salary and Work/Life Balance", a new visual was added using the two "Gauge" in the visualizations pane in report view.
<img width="215" alt="Guage" src="https://github.com/anchal765/Project1--Global-Data-Professionals-Benchmarking-Dashboard/assets/105012057/ee7dc0e6-a461-4d7c-b18d-452a4d9e169d">

 Step 11 : Use "Treemap" visual to represent the "Number of Data professionals in Different countries" who took the survey.
 
![Screenshot 2024-05-09 202429](https://github.com/anchal765/Project1--Global-Data-Professionals-Benchmarking-Dashboard/assets/105012057/aba123d5-7767-4816-a875-8f724063cbae)

- Step 12 : A stacked bar chart was also added to the report design area representing the Average salary of survey takers by their Job title.

<img width="224" alt="stacked bar chart" src="https://github.com/anchal765/Project1--Global-Data-Professionals-Benchmarking-Dashboard/assets/105012057/f845982f-aece-4155-940e-7c7d9303435f">

- Step 10 : A Stacked Column chart is added to represent the Favourite Programming language of the Survey takers according to their Job role.
<img width="221" alt="stacked column chart" src="https://github.com/anchal765/Project1--Global-Data-Professionals-Benchmarking-Dashboard/assets/105012057/39a0697b-13fe-4735-9755-a3ad00ae7cc9">

- Step 11 : A Donut chart is added to represent the difficulty in breaking into the data industry and a pie chart were added to visualise the number of male and female survey takers.

- <img width="172" alt="Donut chart" src="https://github.com/anchal765/Project1--Global-Data-Professionals-Benchmarking-Dashboard/assets/105012057/33b0dcef-f315-4881-9183-9ad585aeb66e">
<img width="176" alt="pie chart" src="https://github.com/anchal765/Project1--Global-Data-Professionals-Benchmarking-Dashboard/assets/105012057/c977342c-6d2a-4768-8138-82464658fcfe">

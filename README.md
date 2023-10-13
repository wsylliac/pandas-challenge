# pandas-challenge
## Module 4 Challenge

In this assignment, you’ll create and manipulate Pandas DataFrames to analyze school and standardized test data.

### Background
You are the new Chief Data Scientist for your city's school district. In this capacity, you'll be helping the school board and mayor make strategic decisions regarding future school budgets and priorities.

As a first task, you've been asked to analyze the district-wide standardized test results. You'll be given access to every student's math and reading scores, as well as various information on the schools they attend. Your task is to aggregate the data to showcase obvious trends in school performance.

### Before You Begin
1. Create a new repository for this project called ![Screenshot 2023-10-13 at 5 58 29 PM](https://github.com/wsylliac/pandas-challenge/assets/140991773/666cdac5-58e8-4090-8cc5-dff3f8ad88dd)
**Do not add this homework to an existing repository.**
2. Clone the new repository to your computer.
3. Inside your local Git repository, create a folder for this homework assignment and name it ![Screenshot 2023-10-13 at 6 00 39 PM](https://github.com/wsylliac/pandas-challenge/assets/140991773/016f4e62-7a05-48d9-8d9d-1a1a2666c514).
4. Add your Jupyter notebook to this folder. This will be the main script to run for analysis.
5. Push these changes to GitHub or GitLab.

### Files
Download the following files to help you get started:

[Module 4 Challenges files](https://static.bc-edx.com/data/dl-1-2/m4/lms/starter/Starter_Code.zip) 📁

### Instructions
Using Pandas and Jupyter Notebook, create a report that includes the following data. Your report must include a written description of at least two observable trends based on the data.

**Hint:** Check out the sample solution called ![Screenshot 2023-10-13 at 6 11 45 PM](https://github.com/wsylliac/pandas-challenge/assets/140991773/74809522-d3e7-41a4-825c-03c11cfdb093) located in the .zip file to review the desired format for this assignment.

### District Summary 
Perform the necessary calculations and then create a high-level snapshot of the district's key metrics in a DataFrame.

Include the following:
* Total number of unique schools
* Total students
* Total budget
* Average math score
* Average reading score
* % passing math (the percentage of students who passed math)
* % passing reading (the percentage of students who passed reading)
* % overall passing (the percentage of students who passed math AND reading)

### School Summary
Perform the necessary calculations and then create a DataFrame that summarizes key metrics about each school.
Include the following:
* School name
* School type
* Total students
* Total school budget
* Per student budget
* Average math score
* Average reading score
* % passing math (the percentage of students who passed math)
* % passing reading (the percentage of students who passed reading)
* % overall passing (the percentage of students who passed math AND reading)

### Highest-Performing Schools (by % Overall Passing)
Sort the schools by ![Screenshot 2023-10-13 at 6 22 35 PM](https://github.com/wsylliac/pandas-challenge/assets/140991773/d1a87bc4-03df-4607-8dcb-683c6a7bcf35) in descending order and display the top 5 rows.

Save the results in a DataFrame called "top_schools".

### Lowest-Performing Schools (by % Overall Passing)

Sort the schools by % ![Screenshot 2023-10-13 at 6 22 35 PM](https://github.com/wsylliac/pandas-challenge/assets/140991773/d1a87bc4-03df-4607-8dcb-683c6a7bcf35) in ascending order and display the top 5 rows.

Save the results in a DataFrame called "bottom_schools".

### Math Scores by Grade

Perform the necessary calculations to create a DataFrame that lists the average math score for students of each grade level (9th, 10th, 11th, 12th) at each school.

### Reading Scores by Grade

Create a DataFrame that lists the average reading score for students of each grade level (9th, 10th, 11th, 12th) at each school.

### Scores by School Spending

Create a table that breaks down school performance based on average spending ranges (per student).

Use the code provided below to create four bins with reasonable cutoff values to group school spending.

![Screenshot 2023-10-13 at 6 48 27 PM](https://github.com/wsylliac/pandas-challenge/assets/140991773/e6059526-4849-4622-96c7-93ac44c5f5bd)

Use ![Screenshot 2023-10-13 at 6 50 01 PM](https://github.com/wsylliac/pandas-challenge/assets/140991773/1a310fb4-efd3-4b76-9ef0-112cc0e65bc4) to categorize spending based on the bins.

Use the following code to then calculate mean scores per spending range.

spending_math_scores = school_spending_df.groupby(["Spending Ranges (Per Student)"])["Average Math Score"].mean()
spending_reading_scores = school_spending_df.groupby(["Spending Ranges (Per Student)"])["Average Reading Score"].mean()
spending_passing_math = school_spending_df.groupby(["Spending Ranges (Per Student)"])["% Passing Math"].mean()
spending_passing_reading = school_spending_df.groupby(["Spending Ranges (Per Student)"])["% Passing Reading"].mean()
overall_passing_spending = school_spending_df.groupby(["Spending Ranges (Per Student)"])["% Overall Passing"].mean()

Use the scores above to create a DataFrame called![Screenshot 2023-10-13 at 6 52 16 PM](https://github.com/wsylliac/pandas-challenge/assets/140991773/6fee9897-5df1-41d3-a3cb-c4c9dda8c133).

Include the following metrics in the table:
* Average math score
* Average reading score
* % passing math (the percentage of students who passed math)
* % passing reading (the percentage of students who passed reading)
* % overall passing (the percentage of students who passed math AND reading)

#### Scores by School Size
Use the following code to bin the ![Screenshot 2023-10-13 at 6 54 07 PM](https://github.com/wsylliac/pandas-challenge/assets/140991773/ceae66ab-f9e0-4a1d-bfa3-10e1fb86f23d). 

![Screenshot 2023-10-13 at 6 54 45 PM](https://github.com/wsylliac/pandas-challenge/assets/140991773/e367ac0e-291a-4d10-a385-1f9a89d7de78)

Use![Screenshot 2023-10-13 at 6 56 54 PM](https://github.com/wsylliac/pandas-challenge/assets/140991773/009d28d9-78e8-4c22-b30e-4251b8c60ae0) on the "Total Students" column of the![Screenshot 2023-10-13 at 6 57 42 PM](https://github.com/wsylliac/pandas-challenge/assets/140991773/90cc1f63-67e1-4219-9466-ca1a4fb30a58).

Create a DataFrame called ![Screenshot 2023-10-13 at 6 59 51 PM](https://github.com/wsylliac/pandas-challenge/assets/140991773/519bc0a2-3962-43bc-87b0-e9670ed022bf) that breaks down school performance based on school size (small, medium, or large).

### Scores by School Type

Use the ![Screenshot 2023-10-13 at 7 01 11 PM](https://github.com/wsylliac/pandas-challenge/assets/140991773/76a908c1-7b9f-498a-beb5-5134d54c9331) DataFrame from the previous step to create a new DataFrame called ![Screenshot 2023-10-13 at 7 02 42 PM](https://github.com/wsylliac/pandas-challenge/assets/140991773/f50d9c56-46a2-4dfe-950d-83396f128885).

This new DataFrame should show school performance based on the "School Type".







# pandas-challenge

Background: 

In this assignment, I am tasked with conducting an in-depth analysis of district-wide standardized test results. I have been provided with two datasets schools_complete.csv and students_complete.csv which have been merged seamlessly. These datasets contain comprehensive information, including the math and reading scores of each student, along with various details regarding the schools they are enrolled in. 

<img width="839" alt="Screenshot 2024-03-27 at 9 05 34 PM" src="https://github.com/Kimbonilla96/pandas-challenge/assets/156154742/32af30ff-dd11-4a25-a617-e73b1fb1870b">

District Summary:

In this section, my task is to compute various key metrics, including the total number of unique schools, total number of students, total budget for each school, the average math score, average reading score, percentage passing math, percentage passing reading, and the overall percentage passing. Upon completing these calculations I generated a comprehensive overview of the districts key metrics in a DataFrame.

<img width="623" alt="Screenshot 2024-03-27 at 9 11 37 PM" src="https://github.com/Kimbonilla96/pandas-challenge/assets/156154742/83288e16-1c9f-44fb-93ad-114abd5d9ba0">

School Summary: 

For each school, I computed essential metrics, encompassing the school names, the school type, total student count, the total school budget, per-student budget, average math and reading scores, percentage passing math, reading, and the overall passing rates. 

<img width="1008" alt="Screenshot 2024-03-27 at 9 16 58 PM" src="https://github.com/Kimbonilla96/pandas-challenge/assets/156154742/9db2da47-6747-4fea-a581-4733e5071907">

Highest-Performing Schools (by % Overall Passing):

Sort the schools by % Overall Passing in descending order and display the top 5 rows. Save the results in a DataFrame called "top_schools".

<img width="994" alt="Screenshot 2024-03-27 at 9 18 07 PM" src="https://github.com/Kimbonilla96/pandas-challenge/assets/156154742/d6c69992-6406-45e9-b6cd-c45d4be53416">

Lowest-Performing Schools (by % Overall Passing)

Sort the schools by % Overall Passing in ascending order and display the top 5 rows. Save the results in a DataFrame called "bottom_schools".

<img width="984" alt="Screenshot 2024-03-27 at 9 18 46 PM" src="https://github.com/Kimbonilla96/pandas-challenge/assets/156154742/cbcda89f-0138-4275-8472-5934dda51236">

Math Scores by Grade:

Perform the necessary calculations to create a DataFrame that lists the average math score for students of each grade level (9th, 10th, 11th, 12th) at each school.

<img width="492" alt="Screenshot 2024-03-27 at 9 19 39 PM" src="https://github.com/Kimbonilla96/pandas-challenge/assets/156154742/a82d4cec-c9f8-4132-9826-7458c4103d43">

Reading Scores by Grade:

Create a DataFrame that lists the average reading score for students of each grade level (9th, 10th, 11th, 12th) at each school.

<img width="502" alt="Screenshot 2024-03-27 at 9 20 04 PM" src="https://github.com/Kimbonilla96/pandas-challenge/assets/156154742/edcb0769-4bda-4aae-9201-1fbe566cc143">

Scores by School Spending:

Create a table that breaks down school performance based on average spending ranges (per student).

Use the code provided below to create four bins with reasonable cutoff values to group school spending.

<img width="535" alt="Screenshot 2024-03-27 at 9 22 39 PM" src="https://github.com/Kimbonilla96/pandas-challenge/assets/156154742/8f09b4b2-08f4-492d-8a09-17f68386c5d8">

Use pd.cut to categorize spending based on the bins.

Use the following code to then calculate mean scores per spending range.

spending_math_scores = school_spending_df.groupby(["Spending Ranges (Per Student)"])["Average Math Score"].mean()
spending_reading_scores = school_spending_df.groupby(["Spending Ranges (Per Student)"])["Average Reading Score"].mean()
spending_passing_math = school_spending_df.groupby(["Spending Ranges (Per Student)"])["% Passing Math"].mean()
spending_passing_reading = school_spending_df.groupby(["Spending Ranges (Per Student)"])["% Passing Reading"].mean()
overall_passing_spending = school_spending_df.groupby(["Spending Ranges (Per Student)"])["% Overall Passing"].mean()

Use the scores above to create a DataFrame called spending_summary.
Include the following metrics in the table:

Average math score

Average reading score

% passing math (the percentage of students who passed math)

% passing reading (the percentage of students who passed reading)

% overall passing (the percentage of students who passed math AND reading)


<img width="587" alt="Screenshot 2024-03-27 at 9 21 00 PM" src="https://github.com/Kimbonilla96/pandas-challenge/assets/156154742/66b664c3-e4f6-4b05-b162-9801f5fb4f19">



Scores by School Size:

Use the following code to bin the per_school_summary.


Use pd.cut on the "Total Students" column of the per_school_summary DataFrame.

Create a DataFrame called size_summary that breaks down school performance based on school size (small, medium, or large).

<img width="989" alt="Screenshot 2024-03-27 at 9 25 57 PM" src="https://github.com/Kimbonilla96/pandas-challenge/assets/156154742/6043c911-fdb0-4b94-bcc8-53d7c0901091">


<img width="985" alt="Screenshot 2024-03-27 at 9 24 17 PM" src="https://github.com/Kimbonilla96/pandas-challenge/assets/156154742/b98d76cd-7605-48a3-a0e4-df90043e46ab">







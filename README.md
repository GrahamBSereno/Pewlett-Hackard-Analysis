# Pewlett-Hackard-Analysis

## Overview of Analysis
The purpose of this analysis is to assist Pewlett Hackard with valuable insights on staff members nearing retirement age. The aging distribution of the organization is skewed toward the higher age range, so Pewlett Hackard needs to begin contingency planning for titles that will need to be replaced in the future to avoid business disruption. To do this, I created a database to hold relevant employee data and queried information regarding aging individuals by using Structured Query Language (SQL).

To create the database, I began with an Entity Relationship Diagram (ERD) by following the Conceptual, Logical, and Physical modeling process (see below).

![alt text](https://github.com/GrahamBSereno/Pewlett-Hackard-Analysis/blob/main/EmployeeDB.png)

## Results
- The main titles that Pewlett Hackard will have to complete contingency planning for are Senior Engineer (25,916 positions), Senior Staff (24,926 positions), and Engineer (9,285 positions). See below for the full retiring titles distribution:

![alt text](https://github.com/GrahamBSereno/Pewlett-Hackard-Analysis/blob/main/retiringtitles.png)

- I noticed that there were some duplicate titles, so I used the 'Destinct On' statement to retreive the first occurence of the employee number for each set of rows. The above bullet also doesnt take into account those employees that have left the company, so I had to filter for employees with no end of employment date. 
- I then wrote a querty to create a memtorship elegiblity to assist with the broader Mentorship Program. To do this, retrieve the employee information from my Employees table, retrieve the tenure information from the Department Employee table, and filter on employees with birthdays between 1/1/1965 and 12/1/1965. This is important as Pewlitt Hackard need senior employees to train. See SQL query below:

![alt text](https://github.com/GrahamBSereno/Pewlett-Hackard-Analysis/blob/main/MentorshipEligibility.png)

- There are not too many employees available for the Mentorship Program. I used the Count statement to reach a total of 1,549 employees. Pewlitt Hackard needs more employees to assist with training for contingency planning purposes.

## Summary
1. There are 72,359 positions that Pewlitt Hackard will need to account for as the retirement wave hits. 
2. There are 1549 employees eligible for the Mentorship Program.

I also completed two additonal queires as part of this analysis.
1. I used a count to get those employees that are eligible for the mentorship program. See below:
![alt text](https://github.com/GrahamBSereno/Pewlett-Hackard-Analysis/blob/main/MentorshipEligibleCount.png)

2. I used a sum of salary to get Pewlitt Hackard's salary overhead cost. See below:
![alt text](https://github.com/GrahamBSereno/Pewlett-Hackard-Analysis/blob/main/TotalSalary.png)


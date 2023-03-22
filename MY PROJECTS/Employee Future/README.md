# Employee future in company: Project Overview 
* Create a tool that predicts whether an employee will want to lay off within 2 years.
* Analyze which aspects influence and which do not influence the decision.
* Optimized GridsearchCV to reach the best model.  

## Code and Resources Used 
**Python Version:** 3.7  
**Packages:** pandas, numpy, sklearn, matplotlib, seaborn, plotly.express

## About Data

1.Education - Education of the employee - {Bachelors,Masters,Phd}.

2.JoiningYear - Joining Year of the employee - {2012,2013,2014,2015,2016,2017,2018}.

3.City - Working location of the employee - {Bangalore,Pune,New Delhi}.

4.PaymentTier - Type of payments - {1,2,3}.

5.Age - Age of the employee - {20-45}.

6.Gender - Gender of the employee - {Male,Female}.

7.EverBenched - Whether the employee has ever been on bench-means he/she wasnt working on any project - {'Yes','No'}.

8.ExperienceInCurrentDomain - How much experience an employee has in current domain?

9.LeaveOrNot - Which employee will leave the organizaion? - {0,1}

10.HiredYears - How long someone is hired in this company.

## EDA
### Data Preparinh
PaymentTier is now: High Pay, Mid Pay, Low Pay
Age is now: Young, MiddleAged, Adulthood
LeaveOrNot is now: No, Yes

I looked at the distributions of the data and the value counts for the various categorical variables. Below are a few highlights from the pivot tables. 

![alt text](https://github.com/PlayingNumbers/ds_salary_proj/blob/master/salary_by_job_title.PNG "Salary by Position")
![alt text](https://github.com/PlayingNumbers/ds_salary_proj/blob/master/positions_by_state.png "Job Opportunities by State")
![alt text](https://github.com/PlayingNumbers/ds_salary_proj/blob/master/correlation_visual.png "Correlations")

## Model Building 
First, I transformed the categorical variables into dummy variables. I also split the data into train and tests sets with a test size of 20%.

# Employee future in company: Project Overview 
* Create a tool that predicts whether an employee will want to lay off within 2 years.
* Analyze which aspects influence and which do not influence the decision.
* Optimized GridsearchCV to reach the best model.  

## Code and Resources Used 
**Python Version:** 3.9  
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
* PaymentTier is now: High Pay, Mid Pay, Low Pay
* Age is now: Young, MiddleAged, Adulthood
* LeaveOrNot is now: No, Yes

Interestingly, the least correlation with the dismissal decision is the payout so it cannot be the main reason for the decision.

The chart shows that as a percentage, women are far more likely to decide to quit than men. 

When it comes to education, on average every second person with a master's degree quits. 

![alt text](https://user-images.githubusercontent.com/117313800/226877671-3437779c-74e0-471b-9040-d547880723fc.png "Correlations")
![alt text](https://user-images.githubusercontent.com/117313800/226877632-c590732f-e329-4bff-8e47-5d8a33e70f63.png "Experience")
![alt text](https://user-images.githubusercontent.com/117313800/226877741-65ff1d07-47eb-4f60-a876-fc6361770857.png "Correlations")
![alt text](https://user-images.githubusercontent.com/117313800/226877745-c8794d81-fbfa-4833-b302-412f59471976.png "Gender count")

## Model Building 
First, I transformed the categorical variables into dummy variables. I also split the data into train and tests sets with a test size of 20%.

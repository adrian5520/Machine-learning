# Used phone price prediction
* Create a tool that predicts prices of used phone
* Analyze which aspects have the bigest impact in price
* Optimized GridsearchCV to reach the best model.  

## Code and Resources Used 
**Python Version:** 3.9  
**Packages:** pandas, numpy, sklearn, matplotlib, seaborn

## About Data



## EDA

### Models specyfication

1.Screen size - most have from 10 to 15 cls

2.day_ued - most have form 550d to 1000+

3.weight - most have form 100g to 200g

4.RAM = most have 4GB

5.battery most have from 2000mph to 4000mph

* Correlation 
The most correlated parameters of the phone are: 
* screen size
* RAM 
* cameras
* battery

We can also read from the data that the number of days of use of the phone does not significantly affect the price.

![alt text](https://user-images.githubusercontent.com/117313800/226948623-5737a7c3-107c-4bd1-b4ff-2abfbdc19c92.png "Correlations")
![alt text](https://user-images.githubusercontent.com/117313800/226948630-de26438a-edfb-47e8-970e-173173807bac.png "Correlations")


## Model Building 


## Training Model
For this scinario i use three models: **SVC, DecisionTreeClassifier and RandomForestClassifier** and these are the results.

**The best model i can train is SVC!**

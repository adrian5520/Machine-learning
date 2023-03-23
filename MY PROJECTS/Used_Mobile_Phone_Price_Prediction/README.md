# Used phone price prediction
* Create a tool that predicts prices of used phone
* Analyze which aspects have the bigest impact in price
* Optimized GridsearchCV to reach the best model.  

## Code and Resources Used 
**Python Version:** 3.9  
**Packages:** pandas, numpy, sklearn, matplotlib, seaborn

## About Data

1.device_brand = Phone brand 

2.os = Software

3.screen_size = Screen size in cal

4.4g = Does the phone have 4G

5.5g = Does the phone have 5G

6.rear_camera_mp = Rear camera quality

7.front_camera_mp = Front camera quality

8.internal_memory = How much internal memory the phone has

9.ram = How much RAM the phone has

10.battery = How much mAh the battery has

11.weight = Weight

12.release_year = Relised phone year

13.days_used = How many day phone wos used

14.normalized_used_price = Used phone price 

15.normalized_new_price = New phone price

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
Before training the models, I prepared the data using get_dummies() and then normalized the data using the MinMaxScaler() method.

## Training Model
For this problem I use three models: **LinearRegression, DecisionTreeClassifier and RandomForestClassifier** and these are the results.

MSE:
* LinearRegression: 0.05537407019586381 
* DecisionTreeRegressor 0.11645956435285287 
* RandomForestRegressor 0.05550902497362688 

R2:
* LinearRegression: 0.8570216595071964 
* DecisionTreeRegressor 0.6992961653931385 
* RandomForestRegressor 0.8566732001994756 

Explained Variance:
* LinearRegression: 0.8732622797087883 
* DecisionTreeRegressor 0.709610152863769 
* RandomForestRegressor 0.8631342698473614 

**Best model: Linear Regression**

![alt text](https://user-images.githubusercontent.com/117313800/227266183-f90c424d-571c-4f57-b12d-d540a72acae1.png "Correlations")

I then wanted to improve the model with the Lasso and GridSearchCV methods, but unfortunately the model did not improve. 

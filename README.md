# Bike Sharing Demand Prediction
![bike sss](https://user-images.githubusercontent.com/103363862/189334857-47a5588e-d0c4-4268-bff3-5e849def84ef.jpg)

# Inrtoduction
Currently Rental bikes are introduced in many urban cities for the enhancement of mobility comfort. It is important to make the rental bike available and accessible to the public at the right time as it lessens the waiting time. Eventually, providing the city with a stable supply of rental bikes becomes a major concern. The crucial part is the prediction of bike count required at each hour for the stable supply of rental bikes.

# Problem statement
We are tasked with predicting the number of bikes rented each hour so as to make an approximate estimation of the number of bikes to be made available to the public given a particular hour of the day.

# Overview of the data
We are given the following columns in our data:

Date : year-month-day
Rented Bike count - Count of bikes rented at each hour
Hour - Hour of the day
Temperature-Temperature in Celsius
Humidity - %
Wind Speed - m/s
Visibility - 10m
Dew point temperature - Celsius
Solar radiation - MJ/m2
Rainfall - mm
Snowfall - cm
Seasons - Winter, Spring, Summer, Autumn
Holiday - Holiday/No holiday
Functional Day - No(Non Functional Hours), Yes(Functional hours)

# Steps involved
Installing libraies and getting the dataset.
Performing EDA (exploratory data analysis).
Drawing conclusions from the data.
Preprocessing the data.
Training different models.
Evaluating metrics of all the models.

# Algorithms used
Linear Regression
Lasso And Ridge Regression
Decision Tree Regressor
Gradient Boosting

We used R2-score to understand which model fit our data better, and the scores are as follows:

![model](https://user-images.githubusercontent.com/103363862/189334454-77b6f5a6-4cb8-41c0-927a-a0157730e9f7.png)

# Conclusion
Demand for bikes got higher when the temperature and hour values were more.

Demand was high for low values of Humidity and solar radiation.

Demand was high during springs and summer and autumn and very low during winters.

Maximum bikes were reneted in the year 2018

Count of rented bikes is high during no holiday and functioning day especially during office time.

# Model Fitting Conclusion
XG Boost regressor performs best in that dataset it gives the accuracy of 88 % also when we hypertune that model the accuracy incresses by aroud 5 % finally it giver the accuracy of 93 % on the testing dataset.

The most important features who had a major impact on the model predictions were; hour, temperature, Humidity, solar-radiation, and Winter.

The model performed well in this case but as the data is time dependent, values of temperature, wind-speed, solar radiation etc. will not always be consistent. Therefore, there will be scenarios where the model might not perform well. As Machine learning is an exponentially evolving field, we will have to be prepared for all contingencies and also keep checking our model from time to time



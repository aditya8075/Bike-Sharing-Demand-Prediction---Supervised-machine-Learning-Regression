#Bike Sharing Demand Prediction
![scooty 2](https://user-images.githubusercontent.com/103363862/189123122-cbe11a88-48d1-4187-8d41-d87c5763a24e.jpg)
                                                     
                                                     
                                                     
                      

PROBLEM STATEMENT:
Maximize: The availability of bikes to the customer.
Minimize: Minimise the time of waiting to get a bike on rent.
The main goal of the project is to:
Finding factors and cause those influence shortage of bike and time delay of availing bike on rent. Using the data provided, this paper aims to analyse the data to determine what variables are correlated with customer churn, if any. Hourly count of bike for rent will also be predicted. 
Introduction :
Bike sharing systems are a means of renting bicycles where the process of obtaining membership, rental, and bike return is automated via a network of kiosk locations throughout a city. Using these systems, people are able rent a bike from a one location and return it to a different place on an as-needed basis.
The goal of this project is to combine the historical bike usage patterns with the weather data to forecast bike rental demand. The data set consists of hourly rental data spanning two years. 

![problem](https://user-images.githubusercontent.com/103363862/189124448-3b29ff5e-1fae-4f73-a5e0-2271cb02f71a.png)



Factors Affecting :
Following are the factors affecting to the number of bike rentals:

Weather : We observe higher bike rentals when the weather (ie humidity, windspeed solar radiations) is more clear and sunny. We also notice that there is a single instance where there were rentals under heavy rain/snow condition this maybe happen because of outliers in the dataset.

Seasons : Bike rental counts across the 4 seasons ie. Fall spring summer and winter. Bike reservations are highest during the Summer season and least during the Spring season.

Working Day : Bike rental counts on working and non-working days and we observed that the outliers are present in working day.

Holiday : Bike rental counts on holidays and non-holidays. Holidays correspond to non-working days. Also outliers are present in non holidays.

Temperature : We observed that there is increase in the bikes rented counts with temperature with a small decrease at the highest temperature. Temperature between 32 and 36 degrees Celsius seems to be the ideal temperature.

Hours : We observed that there is a peak in the bike rentals counts at around 8am morning and at around 5pm evening. 

Data-set description
Feature Name
Date : year-month-day 
Rented Bike Count
Hour
Temperature(°C)
Humidity (%)
Wind speed (m/s)
Visibility (10m)
Dew Point temperature (°C)
Solar Radiation (MJ/m2)
Rainfall (mm)
Snowfall(cm)
Seasons
Holiday
Functioning day


Steps involved :
The following steps are involved in the project
Exploratory Data Analysis : 
After loading and reading the dataset in notebook, we performed EDA. Comparing target variable which is bike rentals counts with other independent variables. This process helped us figuring out various aspects and relationships among the target and the independent variables and also we observed the distribution of variables. It gave us a better idea that how feature behaves with the target variable.
Null values Treatment and Outliers :
Dataset contains a no null values to disturb the accuracy but outliers are present which can disturb the accuracy. So Again,  we use z-score to remove outliers.

Numerical and categorical Features : With the help of exploratory data analysis we analyzed the categorical as well as numerical features in the dataset.

One hot encoding :
In this dataset some categorical variables like seasons, holiday and function day, we change it with numerical database.

Correlation Analysis :
We plot the heatmap to find  the correlation between both dependent variable and independent variables.

Train test Split :
In train test split we take x as dependent variables and y take as independent variable then train the model.

![eda steps](https://user-images.githubusercontent.com/103363862/189124038-381c7dea-6daa-45ac-a0f8-e633ce206d05.jpg)

# Algorithms used
Linear Regression
Decision Tree Regressor
Random Forest Regressor
Extra Trees Regressor


# Conclussion
We used R2-score to understand which model fit our data better, and the scores are as follows:

Linear Regression - 0.515109
Decision Tree Regressor - 0.795209
Random Forest Regressor - 0.844341
Extra Trees Regressor - 0.852685
Its evident from above that the Extra trees regressor model performed well in fitting the data with R2-score of 0.852685. The model which performed poorly was elastic net regularization with R2-score of 0.42.










 









 




Conclusion:
EDA:


Demand for bikes got higher when the temperature and hour values were more.


Demand was high for low values of Humidity and solar radiation.


Demand was high during springs and summer and autumn and very low during winters.

Maximum bikes were rented in the year 2018

Count of rented bikes is high during no holiday and functioning day especially during office time.

Model Fitting Conclusion


The model performed well in this case but as the data is time dependent, values of temperature, wind-speed, solar radiation etc. will not always be consistent. Therefore, there will be scenarios where the model might not perform well. As Machine learning is an exponentially evolving field, we will have to be prepared for all contingencies and also keep checking our model from time to time

Bike Sharing Demand Prediction
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




ALGORITHMS: 
LINEAR REGRESSION: 
Linear regression is a supervised machine learning model majorly used in forecasting. Supervised machine learning models are those where we use the training data to build the model and then test the accuracy of the model using the loss function.
Linear regression is one of the most widely known time series forecasting techniques which is used for predictive modelling. As the name suggests, it assumes a linear relationship between a set of independent variables to that of the dependent variable (the variable of interest).

We’re going to fit a line
 y = β0 + β1x 
to our data. Here, x is called the independent variable or predictor variable, and y is called the dependent variable or response variable. Before we talk about how to do the fit, let’s take a closer look at the important quantities from the fit:
• β1 is the slope of the line: this is one of the most important quantities in any linear regression analysis
• β0 is the intercept of the line.

![linear regression](https://user-images.githubusercontent.com/103363862/189124667-0bbf37e6-e3f4-42c4-9558-7593ef359c29.png)





 

RIDGE REGRESSION:

Ridge regression is a model tuning method that is used to analyse any data that suffers from multicollinearity. This method performs L2 regularization. When the issue of multicollinearity occurs, least-squares are unbiased, and variances are large, this results in predicted values to be far away from the actual values.
we have concluded that we would like to decrease the model complexity, that is the number of predictors. We could use the forward or backward selection for this, but that way we would not be able to tell anything about the removed variables' effect on the response. Removing predictors from the model can be seen as settings their coefficients to zero. Instead of forcing them to be exactly zero, let's penalize them if they are too far from zero, thus enforcing them to be small in a continuous way. This way, we decrease model complexity while keeping all variables in the model. This, basically, is what Ridge Regression does.



LASSO REGRESSION: 
 
Lasso, or Least Absolute Shrinkage and Selection Operator, is quite similar conceptually to ridge regression. It also adds a penalty for non-zero coefficients, but unlike ridge regression which penalizes sum of squared coefficients (the so-called L2 penalty), lasso penalizes the sum of their absolute values (L1 penalty). As a result, for high values of λ, many coefficients are exactly zeroed under lasso, which is never the case in ridge regression.
The only difference in ridge and lasso loss functions is in the penalty terms. Under lasso, the loss is defined as:








DECISION TREE:
Decision tree is the most powerful and popular tool for classification and prediction. A Decision tree is a flowchart like tree structure, where each internal node denotes a test on an attribute, each branch represents an outcome of the test, and each leaf node (terminal node) holds a class label. A tree can be “learned” by splitting the source set into subsets based on an attribute value test. This process is repeated on each derived subset in a recursive manner called recursive partitioning. Decision trees classify instances by sorting them down the tree from the root to some leaf node, which provides the classification of the instance. An instance is classified by starting at the root node of the tree, testing the attribute specified by this node, and then moving down the tree branch corresponding to the value of the attribute as shown in the above figure. This process is then repeated for the subtree rooted at the new node. 

![dt](https://user-images.githubusercontent.com/103363862/189124884-50d9a99e-ddee-472a-9f5e-a16ea0720746.png)



GRADIENT BOOSTING:
The term gradient boosting consists of two sub-terms, gradient and boosting. We already know that gradient boosting is a boosting technique. Let us see how the term ‘gradient’ is related here.

Gradient boosting re-defines boosting as a numerical optimisation problem where the objective is to minimise the loss function of the model by adding weak learners using gradient descent. Gradient descent is a first-order iterative optimisation algorithm for finding a local minimum of a differentiable function. As gradient boosting is based on minimising a loss function, different types of loss functions can be used resulting in a flexible technique that can be applied to regression, multi-class classification, etc

![gb](https://user-images.githubusercontent.com/103363862/189125097-7a88cdeb-04fa-4ee8-8195-71ed9fb09327.png)




Conclusion:
EDA:
Demand for bikes got higher when the temperature and hour values were more.
Demand was high for low values of Humidity and solar radiation.
Demand was high during springs and summer and autumn and very low during winters.
Maximum bikes were rented in the year 2018
Count of rented bikes is high during no holiday and functioning day especially during office time.
Model Fitting Conclusion

The model performed well in this case but as the data is time dependent, values of temperature, wind-speed, solar radiation etc. will not always be consistent. Therefore, there will be scenarios where the model might not perform well. As Machine learning is an exponentially evolving field, we will have to be prepared for all contingencies and also keep checking our model from time to time

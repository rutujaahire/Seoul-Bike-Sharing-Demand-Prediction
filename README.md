# Seoul-Bike-Sharing-Demand-Prediction
Analysis the data of seoul bike from 2017-2018 yr


Currently rental bikes are introduced in many urban cities for the enhancement of
mobility comfort. The purpose of this movement is to modernize cities and encourage
people to head to a green world.

Let's take the examples of Paris in 2007, where "velibs"
were introduced and Amsterdam, where there are more bikes than cars. The goal is
to facilitate the commute in the Seoul and reduce the amount of cars and the pollution.
Indeed, the development of the way to commute reduced the use of cars to go to work
and visit the city.It is important to make the rental bike available and accessible to the
public, as it provides many alternatives to commuters in metropolises.


The studied dataset contains weather information which are the features (Temperature,
Humidity, Wind speed, Visibility, Dew point, Solar radiation, Snowfall, Rainfall),
the target is the number of bikes rented per hour and date information.


In this report, we train a model to predict the number of bike rentals at any hour of the
year given the weather conditions. The data set was obtained from the Capital Bikeshare
program in Seoul. which contained the historical bike usage pattern with weather data
spanning two years.


First, we do Exploratory Data Analysis on the data set. We look for missing data values
(none were found) and outliers and appropriately modify them. We also perform
correlation analysis to extract out the important and relevant feature set and later
perform feature engineering to modify few existing columns and drop out irrelevant
ones.


We then look at several popular individual models from simple ones like Linear
Regressor and Regularization Models (Ridge and Lasso) to more complicated ensemble
ones like Random Forest, Gradient Boost and Adaboost. 

Additionally, few options for model formulation were tried - 1. A single unified model for working and non-working
days, 2. Two separate models for working and non-working days, 3. Using
OneHotEncoding to get Binary Vector representation of Categorical Features and 4.
Using Categorical Features as provided. Finally, we also tried stacking algorithms where
the predictions from the level 1 individual models were used as meta-features into a
second level model (Linear Regressor, Random Forest and Gradient Boost) to further
enhance the predicting capabilities. 

Acoording to Observation,In the Model Evaluation
Matrices table, Linear Regression, KNN is not giving great results. Random forest & GBR
have performed equally good in terms of adjusted r2. We are getting the best results
from lightGBM and CatBoost.

We started with loading the data, then we did Exploratory Data Analysis (EDA), null
values treatment, feature selection, encoding of categorical columns, and then model
building. In all of these models, our accuracy ranges from 56% to 91%, which can be said
to be good for such a large dataset. This performance could be due to various reasons
like the proper pattern of data, large data, or because of the relevant features. After
performing variable importance analysis to find the most significant variables for all the
models developed with the given data sets. We are getting the best results from
CatBoost and LightGBM.

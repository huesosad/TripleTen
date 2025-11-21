# Used Car Market Value Prediction | Project 14 - Tripleten
This project was part of my Data Scientist bootcamp at Tripleten

## Introduction
Rusty Bargain, a used car sales service, is developing an application to quickly find out the market value of a car. To aid this process, I have to create a Machine Learning model to determine the car's value based on historical data, including technical specifications, trim versions, and prices. I was specifically asked for RMSE (Root Mean Square Error) and the speed of the prediction, along with the time it takes to train the model. 

## Tasks
### 1. Data Preparation
The dataset contained information on a car's technical specifications, trim versions, and prices. The features included date profile was downloaded, vehicle body type, vehicle registration year, gearbox type, power, vehicle model, mileage, vehicle registration month, fuel type, vehicle brand, whether the vehicle was previously repaired or not, date of profile creation, number of vehicle pictures, postal code of profile owner, and date of the last activity of the user. The target variable was the car's price.

The dataset was preprocessed, which involved handling missing values, dealing with outliers, and encoding categorical features.

### 2. Model Training and Evaluation

4 different models were trained:
- Linear Regression as a sanity check (RMSE: 4274.0319 | CPU time: 15s)
- Random Forest Regression (RMSE: 1705.64 | CPU time: 11min 38s)
- LightGBM (RMSE: 1703.99 | CPU time: 5.52 s)
- CatBoost (RMSE 1687.95 | CPU time: 2min 41s)

### 3. Conclusions
After training the models with the best hyperparameters found, I can recommend that Rusty Bargain use LightGBM, as it provides very strong results in the shortest amount of time. Alternatively, if investing a bit more processing time is acceptable, CatBoost can deliver even better performance.

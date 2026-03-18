# Implementation of Random Forest Algorithm for Weather Prediction
## AIM:
To write a program to predict daily temperature , PM2.5 pollution level and Energy based on environmental sensor data using Random Forest Algorithm.

## Problem Statement and Dataset



## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. 
2. 
3. 
4. 

## Program:
```
/*
Program to implement the Random Forest Algorithm to predict daily temperature , PM2.5 pollution level and Energy based on environmental sensor data.
Developed by: THARUN DP
RegisterNumber:25018717

import pandas as pd
from sklearn.model_selection import train_test_split
from sklearn.ensemble import RandomForestRegressor
from sklearn.metrics import mean_absolute_error

data = pd.read_csv("weather-station-eee-block_2024_07_13.csv")

print(data.head())

X = data[['humidity', 'pressure', 'wind_speed', 'light_intensity']]
y = data[['temperature', 'pm2_5', 'energy']]

data = data.dropna()

X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, random_state=42
)

model = RandomForestRegressor(n_estimators=100, random_state=42)
model.fit(X_train, y_train)

y_pred = model.predict(X_test)

error = mean_absolute_error(y_test, y_pred)
print("Mean Absolute Error:", error)

new_data = [[65, 1012, 3.5, 400]]

prediction = model.predict(new_data)

print("Temperature:", prediction[0][0])
print("PM2.5:", prediction[0][1])
print("Energy:", prediction[0][2])
*/
```

## Output:
<img width="853" height="432" alt="image" src="https://github.com/user-attachments/assets/38264e70-8b07-4373-bfd3-e3f272684716" />


## Result:

# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

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
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: vijay k
RegisterNumber: 24901153
 import pandas as pd
from sklearn.tree import DecisionTreeClassifier, plot_tree
from sklearn.preprocessing import LabelEncoder
from sklearn.model_selection import train_test_split
from sklearn import metrics
import matplotlib.pyplot as plt

# Load the dataset
data = pd.read_csv("/content/Employee.csv")

# Display the first few rows
print(data.head())

# Dataset information
data.info()

# Check for missing values
print(data.isnull().sum())

# Value counts for the "left" column
print(data["left"].value_counts())

# Encode categorical variables (salary)
le = LabelEncoder()
data["salary"] = le.fit_transform(data["salary"])

# Display the updated data
print(data.head())

# Define features and target
x = data[["satisfaction_level", "last_evaluation", "number_project", "average_montly_hours",
          "time_spend_company", "Work_accident", "promotion_last_5years", "salary"]]
y = data["left"]

# Display features
print(x.head())

# Split the data into training and test sets
x_train, x_test, y_train, y_test = train_test_split(x, y, test_size=0.2, random_state=100)

# Initialize and fit the Decision Tree classifier
dt = DecisionTreeClassifier(criterion="entropy")
dt.fit(x_train, y_train)

# Make predictions
y_pred = dt.predict(x_test)

# Evaluate the model
accuracy = metrics.accuracy_score(y_test, y_pred)
print("Accuracy:", accuracy)

# Predict for a new sample
new_sample = [[0.5, 0.8, 9, 260, 6, 0, 1, 2]]
prediction = dt.predict(new_sample)
print("Prediction for new sample:", prediction)

# Plot the Decision Tree
plt.figure(figsize=(12, 8))
plot_tree(dt, feature_names=x.columns, class_names=['Not Left', 'Left'], filled=True)
plt.show() 
*/
```

## Output:
![ex8](https://github.com/user-attachments/assets/10ebfff5-7071-43c1-b761-0bbec0490d55)



## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.

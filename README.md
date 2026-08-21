# Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student

## AIM:
To write a program to implement the the Logistic Regression Model to Predict the Placement Status of Student.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm

 Step 1: Import Required Libraries

Step 2: Load the Dataset

Step 3: Copy Data & Drop Unwanted Columns

Step 4: Check Data Quality

Step 5: Encode Categorical Variables

Step 6: Define Features (X) and Target (y)

Step 7: Split into Training and Testing Sets

Step 8: Build and Train Logistic Regression Model

Step 9: Make Predictions

Step 10: Evaluate the Model

Step 11: Predict for a New Student

## Program:
```
/*
Program to implement the the Logistic Regression Model to Predict the Placement Status of Student.
Developed by :Supriya S J 
RegisterNumber: 212224110051

import pandas as pd

from sklearn.model_selection import train_test_split
from sklearn.preprocessing import StandardScaler, LabelEncoder
from sklearn.linear_model import LogisticRegression
from sklearn.metrics import accuracy_score, confusion_matrix, classification_report

# Load the dataset
data = pd.read_csv(r"C:\Users\admin\Downloads\Placement_Data.csv")
# Display the first five rows
print(data.head())

# Encode categorical columns
le = LabelEncoder()

data['gender'] = le.fit_transform(data['gender'])
data['ssc_b'] = le.fit_transform(data['ssc_b'])
data['hsc_b'] = le.fit_transform(data['hsc_b'])
data['hsc_s'] = le.fit_transform(data['hsc_s'])
data['degree_t'] = le.fit_transform(data['degree_t'])
data['workex'] = le.fit_transform(data['workex'])
data['specialisation'] = le.fit_transform(data['specialisation'])
data['status'] = le.fit_transform(data['status'])

# Select input features
X = data[['ssc_p', 'hsc_p', 'degree_p', 'workex', 'etest_p', 'mba_p']]

# Target variable
y = data['status']

# Split the dataset
X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, random_state=42
)

# Feature scaling
scaler = StandardScaler()

X_train = scaler.fit_transform(X_train)
X_test = scaler.transform(X_test)

# Create Logistic Regression model
model = LogisticRegression()

# Train the model
model.fit(X_train, y_train)

# Predict placement status
y_pred = model.predict(X_test)

# Accuracy
print("Accuracy:", accuracy_score(y_test, y_pred))

# Confusion Matrix
print("\nConfusion Matrix:")
print(confusion_matrix(y_test, y_pred))

# Classification Report
print("\nClassification Report:")
print(classification_report(y_test, y_pred))
*/
```

## Output:
<img width="957" height="627" alt="image" src="https://github.com/user-attachments/assets/86b2a881-3959-4809-89de-6654f94a8cc1" />


## Result:
Thus the program to implement the the Logistic Regression Model to Predict the Placement Status of Student is written and verified using python programming.

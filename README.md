# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm:
1. Import the standard libraries.

2. Upload the dataset and check for any null values using .isnull() function.

3. Import LabelEncoder and encode the dataset.

4. Import DecisionTreeRegressor from sklearn and apply the model on the dataset.

5. Predict the values of arrays.

6. Import metrics from sklearn and calculate the MSE and R2 of the model on the dataset.

7. Predict the values of array.

8. Apply to new unknown values.

## Program:
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

Developed by: Shyam Kumar.S

RegisterNumber: 212224040315

```python
import pandas as pd


data = pd.read_csv("Salary.csv")

data.head()

data.info()

data.isnull().sum()

from sklearn.preprocessing import LabelEncoder
le = LabelEncoder()
data["Position"] = le.fit_transform(data["Position"])
data.head()

x = data[["Position", "Level"]]
y = data["Salary"]

from sklearn.model_selection import train_test_split
x_train, x_test, y_train, y_test = train_test_split(x, y, test_size=0.2)

from sklearn.tree import DecisionTreeRegressor
dt = DecisionTreeRegressor()
dt.fit(x_train, y_train)
y_pred = df.predict(x_test)

from sklearn import metrics
mse = metrics.mean_squared_error(y_test, y_pred)
mse

r2 = metrics.r2_score(y_test, y_pred)
r2

dt.predict([[5,6]])
```

## Output:

![image](https://github.com/user-attachments/assets/69844bce-aa35-4b80-b5c1-d98b9a82bd9a)

![image](https://github.com/user-attachments/assets/a76c9c93-15ef-464f-a8de-5ef4462ed039)

![image](https://github.com/user-attachments/assets/83b48d72-0e8e-4ac0-a845-540ea8c5721f)

![image](https://github.com/user-attachments/assets/25620c03-ae78-4e61-b378-9ede969f12ca)

![image](https://github.com/user-attachments/assets/0d96c91c-fe49-43f2-b3dc-b8844e314686)

![image](https://github.com/user-attachments/assets/f37f62c7-653e-411b-9ec6-36985a5951a8)

![image](https://github.com/user-attachments/assets/a2b0940e-a8c3-4f2d-a709-0ca34791ea34)


## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.

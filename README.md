# 🏡 **House Price Predictor using Machine Learning**  

📌 A **Machine Learning** project that predicts **house prices** based on various features like **location**, **area**, and **number of rooms**.  
It uses **Random Forest Regression** to provide **accurate price estimations**, and the trained model is saved in **`Dragon.joblib`** for reuse.  

---

## 📂 **Project Structure**  

```plaintext
House-Price-Predictor-ML/
│── data.csv                    # Dataset used for training
│── housing.data                 # Raw data file
│── housing.names                # Description of dataset features
│── Dragon Real Estates.ipynb     # Jupyter Notebook for training the model
│── Model Usage.ipynb            # Jupyter Notebook for testing the trained model
│── Dragon.joblib                 # Trained ML model (RandomForestRegressor)
│── README.md                    # Project documentation
│── .gitignore                    # Ignores unnecessary files
└── requirements.txt             # Required dependencies
```
_____________________________________________________________________________________________________________________________________________________________________________________________
 ## 🔍 **Key Features**

✅ **Data Preprocessing – Handling missing values, feature scaling, and categorical encoding.**

✅ **Exploratory Data Analysis (EDA) – Insights into the dataset using visualization tools.**

✅ **Machine Learning Model – Implemented Random Forest Regression for price prediction.**

✅ **Model Persistence – The trained model is saved as Dragon.joblib for future use.**

✅ **Jupyter Notebook Execution – Well-structured code for step-by-step execution.**

______________________________________________________________________________________________________________________________________________________________________________________________
## 🛠️ **Technologies & Tools Used**

**Programming Language: Python 🐍**

## **Libraries & Frameworks:**
 
**Pandas, NumPy – Data manipulation**

**Scikit-Learn – Machine learning model**

**Matplotlib, Seaborn – Data visualization**

**Joblib – Model saving & loading**

## **Tools:** Jupyter Notebook, GitHub


## 🚀 **How to Train the Model**

**1️⃣ Open Jupyter Notebook**

**2️⃣ Run Dragon Real Estates.ipynb**

**The trained model will be saved as Dragon.joblib**

## **Loading the Model**

```plaintext
import joblib

# Load the trained model
model = joblib.load("Dragon.joblib")
print(model)  # Output: RandomForestRegressor()
```

**The output RandomForestRegressor() indicates that the Dragon.joblib file contains a trained Random Forest Regressor model.**

## **Predicting House Prices**

**You can use the trained model to predict house prices by providing input features.**

**Below are examples of how to use the model:**

**Example 1: Predicting Using a Sample from the Dataset**

```plaintext
import pandas as pd

# Load dataset
df = pd.read_csv("data.csv")

# Drop the target column (MEDV) to get only input features
X = df.drop(columns=["MEDV"])

# Select the first row for testing
sample_data = [X.iloc[0].values]  

# Predict the house price
predicted_price = model.predict(sample_data)
print("Predicted House Price:", predicted_price[0])
```

**Output:**
```plaintext
Predicted House Price: 23.051999999999992
```

**Example 2: Predicting with Custom Input**
```plaintext
import numpy as np

# Example input features
features = np.array([[-5.439, 4.126, -1.616, -0.672, -1.422,-11.444, -49.312, 7.611, -26.001, -0.577,-0.974, 0.411, -66.860]])  

# Predict the house price
predicted_price = model.predict(features)
print("Predicted House Price:", predicted_price[0])
```

**Output:**
```plaintext
Predicted House Price: 24.571999999999992
```

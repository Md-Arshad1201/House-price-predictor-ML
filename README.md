# 🏡 House Price Predictor using Machine Learning  

📌 A Machine Learning project that predicts house prices based on various features like **location, area, and number of rooms**.  
It uses **Random Forest Regression** to provide accurate price estimations, and the trained model is saved in `Dragon.joblib` for reuse.  

---

## 📂 Project Structure  


---

## 🔍 Key Features  

✅ **Data Preprocessing** – Handling missing values, feature scaling, and categorical encoding.  
✅ **Exploratory Data Analysis (EDA)** – Insights into the dataset using visualization tools.  
✅ **Machine Learning Model** – Implemented **Random Forest Regression** for price prediction.  
✅ **Model Persistence** – The trained model is saved as `Dragon.joblib` for future use.  
✅ **Jupyter Notebook Execution** – Well-structured code for step-by-step execution.  

---

## 🛠️ Technologies & Tools Used  

- **Programming Language:** Python 🐍  
- **Libraries & Frameworks:**  
  - Pandas, NumPy – Data manipulation  
  - Scikit-Learn – Machine learning model  
  - Matplotlib, Seaborn – Data visualization  
  - Joblib – Model saving & loading  
- **Tools:** Jupyter Notebook, GitHub  

---

## 🚀 How to Train the Model  

1️⃣ **Open Jupyter Notebook**  
2️⃣ **Run `Dragon Real Estates.ipynb`**  
   - The trained model will be saved as **`Dragon.joblib`**  

---

## 🎯 How to Use the Trained Model  

Once the model is trained, you can **load and use it** in **`Model Usage.ipynb`** or a Python script.  

```python
import joblib
import numpy as np

# Load the trained model
model = joblib.load("Dragon.joblib")

# Sample input (ensure it has 13 features)
features = np.array([[-5.439, 4.126, -1.616, -0.672, -1.422,
                      -11.444, -49.312, 7.611, -26.001, -0.577,
                      -0.974, 0.411, -66.860]])

# Make prediction
predicted_price = model.predict(features)
print("Predicted House Price:", predicted_price[0])

# 💳 Credit Card Approval Prediction  

This project predicts whether a **credit card application** will be **approved or rejected** based on various financial factors. The model is trained using **Random Forest Classifier** and supports real-time user input for predictions.  

---

## ✨ Features  
✅ Simulated **credit card application dataset**  
✅ Handles missing values and encodes categorical data  
✅ Applies **StandardScaler** for feature scaling  
✅ Uses **Random Forest Classifier** for predictions  
✅ Saves and loads the model using **joblib**  
✅ Supports **real-time user input** for approval prediction  

---

## 📦 Prerequisites  
Ensure you have the following installed:  
🔹 **Python 3.x**  
🔹 **Pandas**  
🔹 **Numpy**  
🔹 **Scikit-learn**  
🔹 **Joblib**  

Install dependencies using:  
```sh
pip install pandas numpy scikit-learn joblib
```

---

## ⚡ Running the Project  

### 📊 1️⃣ Generating & Preprocessing Data  
The dataset is **synthetically generated** and stored as `credit_card_approval.csv`.  
```python
df.to_csv("credit_card_approval.csv", index=False)
```
Missing values are handled using **median imputation**, and categorical data is encoded.

### 🏋️ 2️⃣ Training the Model  
A **Random Forest Classifier** is trained to classify applications as **Approved (1) or Rejected (0)**.  
```python
model = RandomForestClassifier(random_state=42)
model.fit(X_train, y_train)
```
The model is saved for future use:  
```python
joblib.dump(model, "credit_card_approval_model.pkl")
joblib.dump(scaler, "scaler.pkl")
```

### 🔥 3️⃣ Making Predictions  
Users can enter financial details to check their **credit card approval status**:  
```python
age = int(input("Enter Age: "))
income = float(input("Enter Monthly Income ($): "))
credit_score = float(input("Enter Credit Score (300-850): "))
employment_status = int(input("Employment Status (0 = Unemployed, 1 = Employed, 2 = Self-Employed): "))
loan_amount = float(input("Enter Loan Amount ($): "))
debt = float(input("Enter Current Debt ($): "))
```
The model processes the input and gives the final **approval decision**.

---

## 📂 Project Structure  
```
credit-card-approval/
│── dataset/
│   ├── credit_card_approval.csv  # 💳 Simulated dataset
│── cc_approval().ipynb       # 🚀 Main script
│── credit_card_approval_model.pkl # 🔥 Trained model
│── scaler.pkl                    # 📏 StandardScaler object
│── README.md                      # 📖 Project documentation
```

---

## 🎯 Results & Conclusion  
📌 The **accuracy score** and **classification report** help evaluate model performance.  
📌 The model predicts whether a user is **eligible** for credit card approval.  

---

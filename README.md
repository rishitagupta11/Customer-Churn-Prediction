# 📊 Customer Churn Prediction App

This project predicts whether a customer will **churn or not** using a trained machine learning model. It includes:

- ✅ A **Flask web app** (`app.py`) with a form-based UI  
- 🚀 A **FastAPI app** (`fastapi_app.py`) for API predictions  
- 📁 Pre-trained model, encoders, and scaler (`.pkl` files)

---

## ⚙️ How to Run

### 1. Install Requirements
Create a file named `requirements.txt` and paste the following:

```
flask
fastapi
uvicorn
pydantic
pandas
scikit-learn
```

Then install with:
```bash
pip install -r requirements.txt
```

### 2. Run Flask App (Web Form)
```bash
python app.py
```
Open in browser: [http://localhost:5000](http://localhost:5000)

### 3. Run FastAPI App (API)
```bash
uvicorn fastapi_app:app --reload
```
Check Swagger UI: [http://localhost:8000/docs](http://localhost:8000/docs)

---

## 📤 FastAPI Request Format

POST `/predict`

```json
{
  "gender": "Female",
  "SeniorCitizen": 0,
  "Partner": "Yes",
  "Dependents": "No",
  "tenure": 12,
  "PhoneService": "Yes",
  "MultipleLines": "No",
  "InternetService": "DSL",
  "OnlineSecurity": "Yes",
  "OnlineBackup": "Yes",
  "DeviceProtection": "No",
  "TechSupport": "Yes",
  "StreamingTV": "No",
  "StreamingMovies": "Yes",
  "Contract": "One year",
  "PaperlessBilling": "No",
  "PaymentMethod": "Bank transfer (automatic)",
  "MonthlyCharges": 65.4,
  "TotalCharges": 850.0
}
```

Sample Response:
```json
{
  "prediction": "No Churn",
  "probability": 0.23
}
```

---

## 📁 Files Included

- `app.py` – Flask web app  
- `fastapi_app.py` – FastAPI backend  
- `Customer Churn Prediction.ipynb` – Model training notebook  
- `best_model.pkl`, `encoder.pkl`, `scaler.pkl` – Trained model & preprocessors

---

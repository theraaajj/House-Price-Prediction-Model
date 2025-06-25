# 🏡 House Price Prediction System

A full-stack ML application that predicts house prices in Bangalore using a dataset from Kaggle. It features end-to-end data preprocessing, model training, and a responsive web UI powered by a Flask backend.

---

## 🎯 Project Objective

To build an intuitive system that estimates housing prices based on key features such as location, square footage, number of bedrooms, and bathrooms — using real-world data and regression models.

---

## 🗂️ Project Structure

├── client/
│ ├── app.html # Web form UI
│ ├── app.css # Styling
│ └── app.js # Frontend JS logic
│
├── server/
│ ├── server.py # Flask app with API routes
│ ├── util.py # Model loading and prediction logic
│ └── artifacts/
│ ├── columns.json # Feature list (location encoding)
│ └── *.pickle # Trained model
│
├── model/
│ ├── Untitled1.ipynb # Jupyter Notebook (EDA, training)
│
├── House Price Data.txt # Original dataset


---

## 🔍 Features

- ✅ Regression model trained on 1000s of real housing records
- ✅ Feature Engineering (BHK per sqft, outlier removal)
- ✅ Location-based one-hot encoding
- ✅ Cross-validated Linear Regression model with 80%+ R²
- ✅ JSON + Pickle-based model serving
- ✅ Clean web UI for input & prediction
- ✅ REST API endpoints for integration

---

## ⚙️ Model Overview

- **Algorithm:** Linear Regression (Scikit-learn)
- **Features Used:**  
  `total_sqft`, `bath`, `bhk`, `location` (one-hot encoded)
- **Data Cleaning Includes:**
  - Removal of rare area types
  - Conversion of non-numeric sqft ranges (like `'2100 - 2850'`)
  - Outlier removal using BHK/sqft thresholds
- **Evaluation:**
  - Train/Test Split + Cross Validation
  - Final R² score ~0.80 on test set

---

## 🛠️ How It Works

1. User inputs: `location`, `area (sqft)`, `BHK`, `bathrooms`
2. Flask backend calls `util.get_estimated_price(...)`
3. Input vector is built using one-hot encoding + numerical values
4. Pickled model makes prediction, result returned via API

---

##  🧪 Local Setup Instructions
1. Clone and Set Up Environment
git clone https://github.com/yourusername/house-price-prediction.git
cd house-price-prediction
python -m venv venv
source venv/bin/activate  # or venv\Scripts\activate

2. Install Requirements
pip install -r requirements.txt

3. Run Flask Server
cd server
python server.py
✅ The API will run at: http://127.0.0.1:5000/

4. Open the UI
Open client/app.html in your browser.

---

## 📬 Contact
Raj Aryan
📧 theraaajj@gmail.com

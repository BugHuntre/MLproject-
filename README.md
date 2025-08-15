# 🎓 Student Performance Prediction – End-to-End Machine Learning Project

## 📌 Overview
This project is an **industry-level, end-to-end Machine Learning application** that predicts student performance based on demographic, academic, and social factors.  
It follows a **modular coding approach** for maintainability, scalability, and clarity.

The workflow covers:
1. **Data ingestion and preprocessing**
2. **Feature engineering** using `ColumnTransformer`
3. **Model training** (without hyperparameter tuning for baseline results)
4. **Prediction pipeline** for real-time inference
5. **Flask-based web application** for deployment

---

## 🛠 Features
- **Modular Code Structure** – each component is separated into Python modules for better maintainability.
- **Feature Engineering** – handled with `ColumnTransformer` for clean, reproducible preprocessing.
- **Industry-Level Deployment** – Flask web app with proper request handling and user interface.
- **Error Handling & Logging** – added to make the pipeline production-ready.
- **No Hyperparameter Tuning** – baseline model for faster prototyping.

---

## 📂 Project Structure
│
├── data/ # Raw datasets
├── artifacts/ # Saved model & preprocessing objects
├── src/
│ ├── components/ # Modular components for each ML stage
│ │ ├── data_ingestion.py
│ │ ├── data_transformation.py
│ │ ├── model_trainer.py
│ │ ├── prediction_pipeline.py
│ │ └── utils.py
│ ├── exception.py # Custom exception handling
│ ├── logger.py # Logging setup
│ └── config.py # Path and constant configurations
│
├── templates/ # HTML templates for Flask app
├── pipeline / # Prediction pipeline
├── app.py # Flask application entry point
├── requirements.txt # Project dependencies
└── README.md # Project documentation


---

## 📊 Dataset
- **Source:** inside in the data folder
- **Target Variable:** Student final exam performance (numeric or categorical)
- **Example Features:**
  - Gender
  - Parental education level
  - Study time
  - Test preparation course
  - Absences
  - Past grades

---

## 🔍 Approach
### 1️⃣ Data Ingestion
- Load dataset from CSV into Pandas DataFrame.
- Save a copy of the raw dataset for reference.

### 2️⃣ Data Transformation & Feature Engineering
- Handle missing values using `SimpleImputer`.
- Encode categorical variables using `OneHotEncoder`.
- Scale numerical features with `StandardScaler`.
- Apply transformations using `ColumnTransformer`.

### 3️⃣ Model Training
- Used a baseline ML model (e.g., Linear Regression, Random Forest, LightGBM).
- No hyperparameter tuning — focus on end-to-end integration.

### 4️⃣ Prediction Pipeline
- Load preprocessor and trained model from `artifacts/`.
- Accept raw input, transform features, and output predictions.

### 5️⃣ Web Application (Flask)
- User-friendly HTML form for input.
- Backend processes input, predicts score, and returns results instantly.

---

## 🚀 Getting Started
### Prerequisites
- Python 3.8+
- pip

### Installation
```bash
# Clone the repository
git clone https://github.com/BugHuntre/Mlproject.git
cd MLproject

# Create virtual environment
python -m venv venv
source venv/bin/activate   # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt





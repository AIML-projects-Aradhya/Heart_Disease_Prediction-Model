# ❤️ Heart Disease Prediction using Logistic Regression

This project implements a machine learning model using **Logistic Regression** to predict whether a person has heart disease, based on clinical features from a medical dataset.

---

## Dataset

The dataset used is a CSV file (`data.csv`) consisting of patient attributes relevant to heart disease diagnosis:

| Feature               | Description                           |
|-----------------------|---------------------------------------|
| age                  | Age in years                          |
| sex                  | 1 = male, 0 = female                  |
| cp                   | Chest pain type (0–3)                 |
| trestbps             | Resting blood pressure                |
| chol                 | Serum cholesterol (mg/dl)             |
| fbs                  | Fasting blood sugar (>120 mg/dl)      |
| restecg              | Resting electrocardiographic results  |
| thalach              | Maximum heart rate achieved           |
| exang                | Exercise-induced angina               |
| oldpeak              | ST depression induced by exercise     |
| slope                | Slope of peak exercise ST segment     |
| ca                   | Number of major vessels (0–3)         |
| thal                 | Thalassemia (1 = normal; 2 = fixed defect; 3 = reversible defect) |
| target               | 0 = healthy, 1 = heart disease         |

---

## Libraries Used

- `pandas` – data manipulation  
- `numpy` – numerical operations  
- `scikit-learn` – ML model training, evaluation

---

## Workflow

### 1. Data Loading & Exploration

- Load CSV
- View shape, types, and check missing values
- Analyze class distribution

### 2. Preprocessing

- Split into features (`X`) and target (`y`)
- Stratified `train_test_split` (80/20)

### 3. Model Training

- `LogisticRegression` from scikit-learn
- Fit on training data

### 4. Evaluation

- Predict on training and test sets
- Use `accuracy_score` for metrics

### 5. Predictive System

- Input raw patient data as a tuple
- Model returns prediction (0 or 1)

---

## Example Prediction

input_data = (57, 1, 2, 150, 168, 0, 1, 174, 0, 1.6, 2, 0, 2)
output:
[1]
The person has a heart disease

### Improvements
Add data normalization

Try other models (e.g. Random Forest, XGBoost)

Build Streamlit/Flask interface for real-time prediction

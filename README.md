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

## How to Run

Follow these steps to set up and run the Heart Disease Prediction model on your local machine:

1. **Clone the Repository**

    ```bash
    git clone https://github.com/ara2105/Heart_Disease_Prediction-Model.git
    cd Heart_Disease_Prediction-Model
    ```

2. **Install Dependencies**

    Make sure you have Python 3.8+ installed. Then install the required packages:

    ```bash
    pip install -r requirements.txt
    ```

3. **Add the Dataset**

    Place the `data.csv` file in the root directory of the project.  
    If your dataset is elsewhere or has a different name, update this line in the script:

    ```python
    heart_data = pd.read_csv('data.csv')
    ```

4. **Run the Notebook**

      ```bash
      jupyter notebook heart_disease_prediction.ipynb
      ```

### Improvements
1. Add data normalization
2. Try other models (e.g. Random Forest, XGBoost)
3. Build Streamlit/Flask interface for real-time prediction

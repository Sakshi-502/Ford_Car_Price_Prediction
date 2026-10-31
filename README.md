<img width="413" height="172" alt="image" src="https://github.com/user-attachments/assets/e5cd7a37-fa98-4ba1-a483-8305160871f1" />
# 🚗 Ford Car Price Prediction

## 📌 Project Overview

This project focuses on predicting the **price of Ford cars** using machine learning techniques.

The project uses a Ford car dataset containing **17,966 records and 9 original features**. Exploratory Data Analysis (EDA) is performed to understand the dataset and relationships between numerical variables. Categorical variables are then encoded, numerical features are standardized, and a **Linear Regression** model is trained to predict car prices.

---

## 🎯 Objective

The main objective of this project is to:

- Analyze Ford car pricing data.
- Understand the factors associated with car prices.
- Perform exploratory data analysis.
- Preprocess categorical and numerical features.
- Build a machine learning model for car price prediction.
- Evaluate the model using the **R² score** and **Adjusted R² score**.

---

## 📊 Dataset

The dataset contains **17,966 Ford car records** with the following 9 columns:

| Column | Description |
|---|---|
| `model` | Ford car model |
| `year` | Manufacturing year |
| `price` | Car price — target variable |
| `transmission` | Type of transmission |
| `mileage` | Mileage of the car |
| `fuelType` | Type of fuel used |
| `tax` | Vehicle tax |
| `mpg` | Miles per gallon |
| `engineSize` | Engine size |

There are **no missing values** in the dataset.

---

## 🔍 Exploratory Data Analysis

The project performs EDA to understand the distribution and relationships within the data.

### Analysis performed:

- Dataset inspection
- Shape and information analysis
- Descriptive statistics
- Missing-value analysis
- Price distribution analysis using a histogram
- Correlation analysis using a heatmap

The numerical variables analyzed include:

- Year
- Price
- Mileage
- Tax
- MPG
- Engine Size

The average car price in the dataset is approximately **12,279.53**, while the median price is **11,291**.

---

## 🛠️ Data Preprocessing

### 1. Categorical Encoding

The categorical variables:

- `model`
- `transmission`
- `fuelType`

are converted into numerical representations.

Two encoding approaches are explored:

### One-Hot Encoding

One-hot encoding creates binary columns for the categorical variables, resulting in a dataset with **34 features**.

### Label Encoding

Label Encoding is also applied to:

```text
model
transmission
fuelType
```

The encoded dataset retains the original 8 predictor columns after removing the target variable.

---

## 📏 Feature Scaling

`StandardScaler` is used to standardize the numerical variables:

```text
year
mileage
tax
mpg
engineSize
```

This transforms the numerical features to a standardized scale before model training.

---

## 🤖 Machine Learning Model

### Linear Regression

The project uses **Linear Regression** for predicting car prices.

The dataset is divided into training and testing sets using:

```python
train_test_split(
    X_one_encode,
    y,
    test_size=0.33,
    random_state=42
)
```

A **33% test split** is used, with `random_state=42` for reproducibility.

The Linear Regression model is then trained using the training data.

---

## 📈 Model Evaluation

The model is evaluated using the **R² score**.

### R² Score

The Linear Regression model achieved:

```text
R² Score: 0.7310
```

This means the model explains approximately **73.1% of the variation in Ford car prices** in the test data.

### Adjusted R² Score

The project also calculates the Adjusted R² score:

```text
Adjusted R² Score: 0.7307
```

The same R² score was obtained when the model was trained using the label-encoded features. 

---

## 📌 Model Performance

| Metric | Score |
|---|---:|
| R² Score | **0.7310** |
| Adjusted R² Score | **0.7307** |

The model therefore provides a reasonable baseline for predicting Ford car prices.

---

## 🧰 Technologies Used

- **Python**
- **Pandas**
- **NumPy**
- **Seaborn**
- **Matplotlib**
- **Scikit-learn**
- **Google Colab / Jupyter Notebook**

---

## 📚 Machine Learning Concepts Used

This project demonstrates:

- Exploratory Data Analysis
- Data preprocessing
- Missing-value analysis
- One-Hot Encoding
- Label Encoding
- Feature Scaling
- Train-Test Split
- Linear Regression
- R² Score
- Adjusted R² Score

---

## 📂 Project Structure

```text
Ford-Car-Price-Prediction/
│
├── Ford_Car_Price_Prediction.ipynb
├── ford.csv
└── README.md
```

---

## 🚀 How to Run the Project

### 1. Clone the repository

```bash
git clone <your-repository-link>
```

### 2. Open the notebook

Open:

```text
Ford_Car_Price_Prediction.ipynb
```

using Jupyter Notebook or Google Colab.

### 3. Install required libraries

```bash
pip install numpy pandas seaborn matplotlib scikit-learn
```

### 4. Load the dataset

Make sure `ford.csv` is available in the appropriate working directory.

The notebook loads the dataset using:

```python
df = pd.read_csv('ford.csv')
```

### 5. Run the notebook

Execute the cells sequentially to perform:

```text
Data Loading
     ↓
Data Exploration
     ↓
EDA
     ↓
Categorical Encoding
     ↓
Feature Scaling
     ↓
Train-Test Split
     ↓
Linear Regression
     ↓
Price Prediction
     ↓
Model Evaluation
```

---

## 💡 Key Takeaway

This project demonstrates how machine learning can be used to estimate Ford car prices based on characteristics such as **model, year, mileage, transmission, fuel type, tax, MPG, and engine size**.

The Linear Regression model achieved an **R² score of approximately 73.1%**, making it a useful baseline model for the car price prediction problem.

---

## 👩‍💻 Project Type

**Machine Learning | Regression | Predictive Analytics | Automotive Price Prediction**

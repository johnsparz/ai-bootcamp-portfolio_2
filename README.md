# 🚗 Used Car Price Prediction

## 📌 Project Overview

This project builds a Machine Learning model that predicts the selling price of used cars based on vehicle characteristics such as age, fuel type, mileage, transmission type, and current market price.

The objective is to help an online car marketplace estimate fair and competitive prices for used vehicles.

---

## 🎯 Business Problem

Determining the correct selling price of a used car can be challenging due to factors such as vehicle age, mileage, fuel type, and market demand. This project uses Linear Regression to predict a car's selling price based on these features.

---

## 📊 Dataset Information

The dataset contains the following features:

| Feature       | Description               |
| ------------- | ------------------------- |
| Car_Name      | Name of the car           |
| Year          | Manufacturing year        |
| Present_Price | Current ex-showroom price |
| Kms_Driven    | Total kilometers driven   |
| Fuel_Type     | Petrol, Diesel, or CNG    |
| Seller_Type   | Dealer or Individual      |
| Transmission  | Manual or Automatic       |
| Owner         | Number of previous owners |
| Selling_Price | Target variable           |

---

## 🔍 Exploratory Data Analysis (EDA)

The following analyses were performed:

* Checked dataset shape and structure
* Examined data types
* Checked for missing values
* Generated summary statistics
* Visualized feature relationships
* Analyzed feature correlations using a heatmap

### Key Findings

* No missing values were found in the dataset.
* Present Price has a strong positive relationship with Selling Price.
* Older cars generally have lower selling prices.
* Cars with higher mileage tend to sell for less.

---

## 🛠️ Data Cleaning

The dataset was cleaned by:

* Checking for missing values
* Verifying data types
* Removing duplicate records (if any)
* Preparing features for machine learning

---

## ⚙️ Feature Engineering

A new feature called **Car_Age** was created from the Year column:

```python
df["Car_Age"] = 2025 - df["Year"]
```

This feature better represents how old a vehicle is, which is an important factor in determining resale value.

After creating Car_Age, the original Year column was removed to avoid redundancy.

---

## 🔄 Data Preprocessing

The following preprocessing steps were applied:

### Numerical Features

* Missing value imputation using median values
* Feature scaling using StandardScaler

### Categorical Features

* Missing value imputation using most frequent values
* One-Hot Encoding using Scikit-Learn

A preprocessing pipeline was built using ColumnTransformer and Pipeline.

---

## 🤖 Model Building

### Algorithm Used

* Linear Regression

### Train-Test Split

* Training Data: 80%
* Testing Data: 20%

---

## 📈 Model Evaluation

The model was evaluated using:

* Mean Absolute Error (MAE)
* Root Mean Squared Error (RMSE)
* R² Score

### Results

| Metric   | Score |
| -------- | ----- |
| MAE      | 1.10  |
| RMSE     | 1.51  |
| R² Score | 0.90  |

### Interpretation

The model explains approximately **90% of the variance** in used car prices, indicating strong predictive performance.

---

## 🔮 Sample Predictions

The trained model was used to predict prices for five unseen vehicles from the test dataset.

Predicted prices closely matched actual selling prices, demonstrating the model's effectiveness.

---

## 💡 Insights

### Factors That Influence Car Price

1. Present Price

   * Strongest predictor of selling price.

2. Car Age

   * Newer vehicles generally have higher resale values.

3. Kilometers Driven

   * Cars with lower mileage tend to sell for more.

4. Transmission Type

   * Automatic vehicles often command higher prices.

5. Fuel Type

   * Fuel preferences affect resale value.

### Interesting Findings

* The dataset required minimal cleaning.
* Present Price showed a very strong correlation with Selling Price.
* Linear Regression occasionally produced negative predictions, highlighting one of its limitations.

---

## 🧰 Technologies Used

- Google Colab
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-Learn

---

## 📂 Repository Structure

```text
used-car-price-prediction/
│
├── data/
│   ├── Car_data.csv
│   └── car_data_cleaned.csv
│
├── notebook/
│   └── Used_Car_Price_Prediction.ipynb
│
├── README.md
├── requirements.txt
└── images/
```

---

## 🚀 How to Run the Project

### Option 1: Google Colab (Recommended)

1. Download the notebook (`Used_Car_Price_Prediction.ipynb`).
2. Open Google Colab.
3. Upload the notebook.
4. Upload the dataset (`Car_data.csv`) when prompted.
5. Run all cells from top to bottom.

### Option 2: Run Locally

Clone the repository:

```bash
git clone https://github.com/yourusername/used-car-price-prediction.git
```

Navigate to the project folder:

```bash
cd used-car-price-prediction
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Launch Jupyter Notebook:

```bash
jupyter notebook
```

Open the notebook and run all cells.
## 👨‍💻 Author

**John Arije**

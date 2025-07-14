# 🚗 Audi A1 Price Prediction

This project is a simple **Linear Regression model** trained on the [Kaggle Audi A1 Listings dataset](https://www.kaggle.com/datasets/jacklacey/audi-a1-listings). The goal is to predict the price of Audi A1 cars based on various features.

## 🔗 Dataset

- Source: [Kaggle - Audi A1 Listings](https://www.kaggle.com/datasets/jacklacey/audi-a1-listings)

## 📂 Project Files

- `2-audi_kaggle.ipynb` – Jupyter notebook containing data preprocessing, model training, evaluation, and predictions.

## 📊 Features Used

Some of the features used for prediction:

- `year` (model year)
- `transmission` (type of gearbox)
- `mileage` (distance driven)
- `fuelType` (fuel type)
- Technical specs like `tax`, `mpg`, `engineSize`

## 🧠 Model Info

- Model: `LinearRegression` from `sklearn.linear_model`
- `model.score(x, y)`: **0.9595** (R² score)
- Custom error metric: Mean absolute percentage error-like function

```python
def meanScore(y, y_pred):
    return np.mean(np.abs((y - y_pred) / y)) * 100
```

- Output: `meanScore(y, y_pred)` = **5.66%** error rate

## ⚙️ Installation

```bash
git clone https://github.com/yourusername/audi-price-prediction.git
cd audi-price-prediction
pip install -r requirements.txt  # if exists
jupyter notebook
```

## 🧪 How to Use

Run the notebook to:

1. Load and clean the dataset
2. Perform encoding and preprocessing
3. Train the Linear Regression model
4. Evaluate with R² and custom error score
5. Make predictions on new data

---

**Note:** This project is provided _without any license_. You are free to explore, learn, and build upon it, but redistribution or reuse is not formally permitted without author permission.

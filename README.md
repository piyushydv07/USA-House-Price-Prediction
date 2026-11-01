# USA House Price Prediction

A machine learning project that predicts house prices using the USA Housing dataset and regression techniques.

## Project Overview

This project analyzes housing data and builds a regression model to predict house prices based on:

- Average Area Income
- Average Area House Age
- Average Area Number of Rooms
- Average Area Number of Bedrooms
- Area Population

The notebook performs exploratory data analysis, data cleaning, visualization, model training, evaluation, hyperparameter tuning, and model saving.

## Dataset

The dataset contains **5,000 records and 7 columns**.

| Feature | Description |
|---|---|
| Avg. Area Income | Average income of the area |
| Avg. Area House Age | Average age of houses in the area |
| Avg. Area Number of Rooms | Average number of rooms |
| Avg. Area Number of Bedrooms | Average number of bedrooms |
| Area Population | Population of the area |
| Price | House price / target variable |
| Address | Property address |

The notebook checks for missing values and duplicate records before modeling.

## Machine Learning

The project uses:

- Linear Regression
- Ridge Regression
- GridSearchCV for Ridge hyperparameter tuning

The train-test split uses **80% training data and 20% testing data**, with `random_state=42`.

For Ridge Regression, GridSearchCV tests alpha values:

`[1, 5, 10, 20, 50, 100]`

The final model selected by the notebook is Ridge Regression with the best alpha found during tuning.

## Model Performance

The final model achieved an **R² score of approximately 0.918** on the test set.

> Results can vary if the notebook, dataset, or preprocessing is changed.

## Model File

The trained model is saved as:

`usa_house_price_model.pkl`

It can be loaded later with Python's `pickle` module for prediction.

## Project Structure

```text
USA-House-Price-Prediction/
│
├── housing_price prediction.ipynb
├── USA_Housing.xls
├── usa_house_price_model.pkl
├── README.md
├── requirements.txt
└── .gitignore
```

## Technologies Used

- Python
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook
- Pickle

## How to Run

1. Clone the repository.
2. Install the required packages:

```bash
pip install -r requirements.txt
```

3. Open the notebook:

```bash
jupyter notebook
```

4. Run `housing_price prediction.ipynb`.

### Dataset Note

The notebook currently loads the dataset using:

```python
pd.read_csv('USA_Housing.csv')
```

Therefore, if you keep the uploaded `.xls` dataset as `USA_Housing.xls`, update the notebook to use `pd.read_excel()` (and install `xlrd`) or use a CSV version named `USA_Housing.csv`.

## Disclaimer

This project is created for learning and portfolio purposes and should not be treated as a production-grade house valuation system.

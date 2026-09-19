# California Housing Price Prediction & Classification

A machine learning project using the California Housing dataset to perform both house-value prediction and house-price classification.

## Project Overview

This project implements two supervised machine learning approaches:

1. **Multiple Linear Regression** to predict the median house value.
2. **Logistic Regression** to classify houses into above-median and below-median price categories.

The project uses the California Housing dataset provided by Scikit-learn.

## Dataset

The dataset is loaded using `fetch_california_housing()` from Scikit-learn.

### Features

- MedInc — Median income
- HouseAge — Median house age
- AveRooms — Average number of rooms
- AveBedrms — Average number of bedrooms
- Population — Population
- AveOccup — Average occupancy
- Latitude — Latitude
- Longitude — Longitude

### Target

For the regression task:

- `MedHouseVal` — Median house value

For the classification task, a new binary variable called `PriceCategory` is created based on the median house value:

- `0` — Below or equal to median house value
- `1` — Above median house value

## Methodology

### 1. Data Preparation

The California Housing dataset is loaded using Scikit-learn and converted into a Pandas DataFrame.

The data is divided into:

- 70% training data
- 30% testing data

A `random_state` of 42 is used for reproducibility.

### 2. Multiple Linear Regression

Multiple Linear Regression is used to predict the continuous `MedHouseVal` target.

The model is evaluated using:

- R² Score
- Root Mean Squared Error (RMSE)
- Mean Absolute Error (MAE)

### 3. Logistic Regression

For classification, the median of `MedHouseVal` is calculated and used to create the binary `PriceCategory` target.

The features are standardized using `StandardScaler`, followed by Logistic Regression.

The classification model is evaluated using:

- Accuracy
- Precision
- Recall
- F1 Score

## Results

### Linear Regression

| Metric | Result |
|---|---:|
| R² Score | 0.5958 |
| RMSE | 0.7284 |
| MAE | 0.5272 |

### Logistic Regression

| Metric | Result |
|---|---:|
| Accuracy | 82.72% |
| Precision | 83.12% |
| Recall | 82.48% |
| F1 Score | 82.80% |

## Major Findings

The Linear Regression model achieved an R² score of approximately 0.596, indicating that the model explains a portion of the variation in median house values using the available features.

The Logistic Regression model achieved an accuracy of approximately 82.72% when classifying properties into above-median and below-median price categories.

## Limitations

- Housing prices can be influenced by factors that are not included in the dataset.
- Linear Regression assumes a linear relationship between the input features and the target.
- Logistic Regression converts the continuous house-value target into two categories and therefore does not predict the exact house price.

## Technologies Used

- Python
- NumPy
- Pandas
- Scikit-learn
- Google Colab
- Jupyter Notebook

## How to Run

### Clone the repository

```bash
Install dependencies
pip install -r requirements.txt
Run the notebook

Open:

California_Housing_Price_Prediction.ipynb

The dataset is downloaded automatically through Scikit-learn when the notebook is executed.

Project Structure
California-Housing-Price-Prediction/
│
├── California_Housing_Price_Prediction.ipynb
├── README.md
├── requirements.txt
└── .gitignore
Author

Aliya Khan

git clone https://github.com/YOUR-USERNAME/California-Housing-Price-Prediction.git
cd California-Housing-Price-Prediction

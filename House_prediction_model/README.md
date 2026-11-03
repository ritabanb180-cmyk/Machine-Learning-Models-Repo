# House Price Prediction Model
[![Ask DeepWiki](https://devin.ai/assets/askdeepwiki.png)](https://deepwiki.com/ritabanb180-cmyk/Machine-Learning-Models-Repo)

This repository contains a machine learning project to predict house prices using a Linear Regression model. The model is trained on the `Housing.csv` dataset, which includes various features of houses.

## 📋 Table of Contents
- [Dataset](#-dataset)
- [Methodology](#-methodology)
- [Results](#-results)
- [Getting Started](#-getting-started)

## 📖 Dataset

The model is trained on the `Housing.csv` dataset, which contains 545 entries and 13 columns describing various attributes of houses.

**Features:**
- `price`: The sale price of the house.
- `area`: The total area of the property in square feet.
- `bedrooms`: Number of bedrooms.
- `bathrooms`: Number of bathrooms.
- `stories`: Number of stories (floors).
- `mainroad`: Whether the house is connected to the main road (yes/no).
- `guestroom`: Whether the house has a guest room (yes/no).
- `basement`: Whether the house has a basement (yes/no).
- `hotwaterheating`: Whether the house has hot water heating (yes/no).
- `airconditioning`: Whether the house has air conditioning (yes/no).
- `parking`: Number of parking spaces.
- `prefarea`: Whether the house is in a preferred area (yes/no).
- `furnishingstatus`: The furnishing status of the house (furnished, semi-furnished, unfurnished).

## ⚙️ Methodology

The project follows a standard machine learning workflow implemented in the `House_price_prediction_model.ipynb` Jupyter Notebook.

1.  **Data Loading and Exploration**: The dataset is loaded using pandas, and an initial analysis is performed to understand its structure and check for missing values.
2.  **Data Preprocessing**: Categorical features (like `mainroad`, `guestroom`, etc.) are converted into numerical format using one-hot encoding (`pd.get_dummies`).
3.  **Feature Engineering**: New features are created to potentially improve model performance:
    - `price_log`: Log transformation of the price.
    - `area_log`: Log transformation of the area.
    - `area_per_room`: Area divided by the total number of rooms (bedrooms + bathrooms).
    - `total_rooms`: Sum of bedrooms and bathrooms.
    - `space_per_story`: Area divided by the number of stories.
4.  **Model Training**: The data is split into training (80%) and testing (20%) sets. A Linear Regression model from `scikit-learn` is trained on the training data. The `price_log` is used as the target variable.
5.  **Model Evaluation**: The trained model is evaluated on the test set using the R-squared (R²) score and Mean Absolute Error (MAE).

## 📈 Results

The Linear Regression model achieves the following performance on the test set:

-   **R-squared (R²) Score**: **78.67%**
-   **Mean Absolute Error (MAE)**: 0.1409 (on the log-transformed price)

This indicates that the model can explain approximately 78.67% of the variance in the house prices.

## 🚀 Getting Started

To run this project on your local machine, follow these steps:

### Prerequisites

Make sure you have Python and Jupyter Notebook installed. You will also need the following libraries:
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn

You can install them using pip:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

### Installation & Usage

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/ritabanb180-cmyk/machine-learning-models-repo.git
    ```
2.  **Navigate to the project directory:**
    ```bash
    cd machine-learning-models-repo/House_prediction_model/
    ```
3.  **Start Jupyter Notebook:**
    ```bash
    jupyter notebook
    ```
4.  Open the `House_price_prediction_model.ipynb` file and run the cells to see the model training and evaluation process.
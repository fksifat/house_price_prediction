# House Price Prediction

This project implements a machine learning pipeline to predict house prices using the California Housing dataset. The notebook performs exploratory data analysis (EDA), data preprocessing, model training with multiple algorithms, hyperparameter tuning, and evaluation.

## Dataset

The dataset used is the **California Housing dataset** (`housing.csv`), which contains information about housing blocks in California. It includes the following features:

- `longitude`: Longitude of the housing block
- `latitude`: Latitude of the housing block
- `housing_median_age`: Median age of houses in the block
- `total_rooms`: Total number of rooms in the block
- `total_bedrooms`: Total number of bedrooms in the block
- `population`: Population of the block
- `households`: Number of households in the block
- `median_income`: Median income of households (in tens of thousands of USD)
- `median_house_value`: Median house value (target variable, in USD)
- `ocean_proximity`: Proximity to the ocean (categorical: NEAR BAY, <1H OCEAN, INLAND, NEAR OCEAN, ISLAND)

The dataset has 20,640 samples and 10 columns.

## Requirements

To run this notebook, you need the following Python libraries:

- numpy
- pandas
- matplotlib
- seaborn
- scikit-learn

You can install them using pip:

```bash
pip install numpy pandas matplotlib seaborn scikit-learn
```

## Usage

1. Clone or download the repository.
2. Ensure `housing.csv` is in the same directory as the notebook.
3. Open `house_price_prediction.ipynb` in Jupyter Notebook or JupyterLab.
4. Run the cells in order to execute the analysis and model training.

The notebook is self-contained and includes:

- Data loading and exploration
- Handling missing values
- Feature engineering
- Model training and evaluation
- Hyperparameter tuning
- Final model selection and prediction example

## Models Used

The project evaluates the following regression models:

- Linear Regression
- Ridge Regression
- Lasso Regression
- Random Forest Regressor
- HistGradientBoosting Regressor

Models are trained using pipelines with preprocessing (imputation, scaling, encoding) and evaluated using cross-validation. Hyperparameter tuning is performed using GridSearchCV.

## Results

The best performing model is **HistGradientBoosting Regressor** with optimized hyperparameters. Performance metrics on the test set include RMSE, MAE, and R² score.

An example prediction is provided at the end of the notebook.

## Improvements

Potential ways to enhance the model performance:

- Create ratio features (e.g., rooms_per_household, bedrooms_per_room, population_per_household)
- Apply log transformation on the target variable
- Tune additional hyperparameters for HistGradientBoosting
- Experiment with advanced boosting models like XGBoost or LightGBM
- Perform error analysis by location or price ranges
- Use spatial or grouped validation for location-based data

## License

This project is open-source and available under the MIT License.

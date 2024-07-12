# Flood Prediction in Lagos

## Objective
The objective of this project is to predict the likely date of the next flood in Lagos using historical weather data and time series analysis.

## Introduction
Flooding is a major concern in Lagos, with significant impacts on infrastructure, economy, and public health. Accurate prediction of flood events can help in early warning and preparedness, mitigating the adverse effects.

## Data Collection and Preparation

### Data Source
Historical weather data for Lagos, including precipitation, temperature, and humidity.

### Data Preparation Steps
1. **Loading Data:** Data was loaded from a CSV file.
2. **Datetime Conversion:** Converted the `datetime` column to datetime objects.
3. **Missing Value Handling:** Filled missing values with the mean of their respective columns.
4. **Data Cleaning:** Removed unnecessary columns to focus on relevant features.

## Exploratory Data Analysis (EDA)

### Visualizations
- **Precipitation Over Time:** Trends and patterns in precipitation data.
- **Temperature Over Time:** Trends in temperature data.
- **Humidity Over Time:** Trends in humidity data.

## Feature Engineering
Created lag and rolling average features for precipitation to capture temporal dependencies:
- **Lag Features:** 1-day, 3-day, and 7-day lags.
- **Rolling Average Features:** 3-day and 7-day rolling averages.

## Model Building

### Model Selection
Selected the ARIMA (AutoRegressive Integrated Moving Average) model for time series forecasting.

### Model Training
- **Training and Testing Split:** 80% of data for training, 20% for testing.
- **ARIMA Parameters:** Chosen based on historical data patterns (p=5, d=1, q=0).

### Evaluation Metrics
- **Root Mean Squared Error (RMSE):** Evaluates the model's prediction accuracy.
- **Mean Absolute Error (MAE):** Measures the average magnitude of errors in predictions.

## Forecasting and Results

### Future Forecasting
Forecasted precipitation for the next 30 days.

### Flood Threshold
Determined the potential flood dates based on the current year's precipitation threshold for Lagos (1936.2 mm).

### Results
Potential flood dates based on forecasted precipitation:
- 2024-07-27
- 2024-07-31
- 2024-08-05
- 2024-08-09
- 2024-08-14
- 2024-08-18
- 2024-08-23

## Conclusion
The prediction of flood dates in Lagos has been justified through detailed data analysis, feature engineering, and model evaluation. The identified potential flood dates are based on the current year's precipitation threshold, ensuring relevance and accuracy.

## Skills Demonstrated
- Data Cleaning and Preparation
- Time Series Analysis
- Feature Engineering
- Data Visualization
- Model Building and Evaluation
- Forecasting

## Tools and Technologies Used
- Python (Pandas, Matplotlib, Statsmodels)
- Jupyter Notebook

## How to Run the Project
1. **Clone the repository:**
    ```sh
    git clone https://github.com/yourusername/flood-prediction-lagos.git
    ```
2. **Navigate to the project directory:**
    ```sh
    cd flood-prediction-lagos
    ```
3. **Install the required dependencies:**
    ```sh
    pip install -r requirements.txt
    ```
4. **Run the Jupyter Notebook:**
    ```sh
    jupyter notebook
    ```


## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

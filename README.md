# Walmart Sales Forecasting

This project aims to forecast sales for Walmart using time series analysis and regression techniques, specifically utilizing Long Short-Term Memory (LSTM) networks. The project employs feature engineering to enhance the model's predictive power by incorporating lagged variables, rolling statistics, seasonal indicators, and holiday information.

## Table of Contents

- [Introduction](#introduction)
- [Dataset](#dataset)
- [Feature Engineering](#feature-engineering)
- [Model Training](#model-training)
- [Evaluation](#evaluation)
- [Results](#results)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Introduction

Sales forecasting is a critical task in business, helping companies manage inventory, plan marketing strategies, and make informed financial decisions. In this project, we build a sales forecasting model for Walmart using Python and TensorFlow.

## Dataset

The dataset used in this project is the Walmart Store Sales dataset, which includes information about weekly sales, stores, departments, dates, and whether the week included a holiday.

## Feature Engineering

To improve the model's accuracy, we performed several feature engineering steps:

1. **Date Components**: Extracted `Year`, `Month`, `Day`, and `DayOfWeek` from the `Date` column.
2. **Lagged Variables**: Created lagged versions of `Weekly_Sales` to capture the influence of past sales.
3. **Rolling Statistics**: Computed rolling means and standard deviations of `Weekly_Sales` to capture trends.
4. **Holiday Indicators**: Added a binary feature to indicate whether a given date is a holiday.

## Model Training

We used an LSTM network for time series forecasting. The training process involved:

1. Scaling the features using `MinMaxScaler`.
2. Generating sequences of past observations to predict the next time step.
3. Building and compiling the LSTM model.
4. Training the model with the training dataset.

## Evaluation

The model was evaluated using various metrics:

- **Mean Squared Error (MSE)**
- **Root Mean Squared Error (RMSE)**
- **Mean Absolute Error (MAE)**

We also visualized the predictions against actual values to inspect the model's performance visually.

## Results

The model was able to forecast sales with reasonable accuracy. Below are some key evaluation metrics:

- Mean Squared Error (Test): 3.585819766382823e-05
- Root Mean Squared Error (Test): 0.0059881714791602475
- Mean Absolute Error (Test):  0.0021745846499817336

## Usage

To use this project, follow these steps:

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/walmart-sales-forecasting.git
    ```
2. Navigate to the project directory:
    ```bash
    cd walmart-sales-forecasting
    ```
3. Install the required packages:
    ```bash
    pip install -r requirements.txt
    ```
4. Run the Jupyter notebook:
    ```bash
    jupyter notebook Walmart_sales_Forecast.ipynb
    ```

## Contributing

Contributions are welcome! Please open an issue to discuss what you would like to change or add. Feel free to fork the repository and submit a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

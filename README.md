# LSTM-DEEP-LEARNING

# Air Passengers Forecasting Using LSTM

This project demonstrates how to forecast the number of air passengers using a Long Short-Term Memory (LSTM) network. It covers data preparation, model building, training, prediction, and visualization.

## Table of Contents
- [Project Overview](#project-overview)
- [Technologies Used](#technologies-used)
- [Setup and Installation](#setup-and-installation)
- [Project Steps](#project-steps)
- [Results](#results)
- [Future Improvements](#future-improvements)

## Project Overview
The goal of this project is to predict the monthly number of air passengers based on previous months' data using a deep learning approach. The dataset used is the classic "AirPassengers" dataset, which contains monthly totals of international airline passengers from 1949 to 1960.

## Technologies Used
- Python 3.x
- pandas
- numpy
- matplotlib
- scikit-learn
- TensorFlow / Keras

## Setup and Installation

1. Clone the repository or download the project files.
2. Install required libraries:
   ```bash
   pip install pandas numpy matplotlib scikit-learn tensorflow
   ```
3. Make sure the dataset `AirPassengers.csv` is available in the correct path (or update the path in the code).
4. Run the Python script.

## Project Steps

### Step 1: Import Libraries
Necessary Python libraries for data manipulation, visualization, scaling, and building the LSTM model are imported.

### Step 2: Load the Dataset
The dataset is loaded using pandas. The 'Month' column is parsed as datetime and set as the index.

### Step 3: Normalize the Data
The passenger count is normalized between 0 and 1 using `MinMaxScaler` to make training more stable.

### Step 4: Create Sequences
Sequences of 12 months are created to predict the next month, turning the time series into a supervised learning problem.

### Step 5: Train-Test Split
80% of the data is used for training and 20% for testing.

### Step 6: Build the LSTM Model
A simple LSTM model with 64 units and a Dense output layer is created and compiled with the Adam optimizer and mean squared error (MSE) loss.

### Step 7: Train the Model
The model is trained for 100 epochs, with validation on the test set.

### Step 8: Make Predictions
The model predicts passenger numbers on the test data. Predictions and actual values are inverse-transformed to original scale.

### Step 9: Plot the Results
Actual and predicted values are plotted to visually evaluate model performance.

## Results
The model is able to capture the general trend of the time series but may not perfectly predict sudden variations due to the simplicity of the model.

## Future Improvements
- Try adding more LSTM layers or stacking them.
- Introduce dropout to prevent overfitting.
- Tune hyperparameters such as sequence length, number of LSTM units, learning rate, etc.
- Use more advanced architectures like Bidirectional LSTM or Attention Mechanisms.
- Forecast multiple steps ahead instead of just the next month.


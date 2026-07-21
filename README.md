# Tesla-Stock-Price-Forecasting-Using-LSTM
This model predicts Tesla stock closing prices using an LSTM (Long Short-Term Memory) neural network. Historical stock data is preprocessed through cleaning, feature selection, and MinMax scaling before training. The model forecasts future prices and is evaluated using MAE, MSE, and RMSE, with visual comparisons of actual and predicted values.
# Tesla Stock Price Prediction Using LSTM

## Project Overview

This project predicts Tesla's stock closing prices using a Long Short-Term Memory (LSTM) neural network, a type of Recurrent Neural Network (RNN) designed for time series forecasting. The model learns historical stock price patterns and predicts future closing prices based on previous observations.

---

## Dataset

- **Dataset Name:** Tesla Stock Updated V2
- **Format:** CSV
- **Features:**
  - Date
  - Open
  - High
  - Low
  - Close
  - Volume
- **Target Variable:** Close Price

---

## Data Preprocessing

The following preprocessing steps were performed before training the model:

1. Loaded the dataset using Pandas.
2. Removed the unnecessary index column (`Unnamed: 0`).
3. Converted the `Date` column to datetime format.
4. Sorted the dataset chronologically.
5. Checked and handled missing values.
6. Removed duplicate records.
7. Selected the **Close** price as the target feature.
8. Normalized the data using **MinMaxScaler**.
9. Created 60-day input sequences for LSTM training.
10. Split the dataset into training and testing sets.

---

## LSTM Model Architecture

The forecasting model consists of:

- Input Layer
- LSTM Layer (50 units, return_sequences=True)
- Dropout Layer (20%)
- LSTM Layer (50 units)
- Dropout Layer (20%)
- Dense Layer (25 neurons)
- Output Dense Layer (1 neuron)

### Model Configuration

- Optimizer: Adam
- Loss Function: Mean Squared Error (MSE)
- Epochs: 20
- Batch Size: 32

---

## Model Evaluation

The trained model is evaluated using:

- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)

The project also visualizes:

- Actual vs Predicted Stock Prices
- Training Loss Curve

---

## Technologies Used

- Python
- Jupyter Notebook
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- TensorFlow / Keras

---

## Project Structure

```
Tesla-Stock-Prediction/
│
├── Tasla_Stock_Updated_V2.csv
├── Tesla_Stock_Prediction.ipynb
├── README.md
└── requirements.txt
```

---

## Steps to Run the Project

### 1. Clone or Download the Project

```bash
git clone <repository_url>
```

or download the project folder manually.

### 2. Install Required Libraries

```bash
pip install pandas numpy matplotlib scikit-learn tensorflow
```

### 3. Open Jupyter Notebook

```bash
jupyter notebook
```

### 4. Open the Notebook

Open:

```
Tesla_Stock_Prediction.ipynb
```

### 5. Run All Cells

Execute each notebook cell in order:

- Import libraries
- Load dataset
- Preprocess data
- Train the LSTM model
- Evaluate performance
- Visualize predictions

---

## Results

The LSTM model successfully learns historical stock price trends and generates predictions for Tesla's closing prices. The predicted values closely follow the actual stock prices, demonstrating the effectiveness of LSTM for time series forecasting.

---

## Future Improvements

- Train using a larger historical dataset.
- Include additional features such as Open, High, Low, and Volume.
- Perform hyperparameter tuning.
- Implement Bidirectional LSTM or GRU models.
- Compare performance with Transformer-based forecasting models.

---

## Author

**Mohamed Wajith**

BCA (Artificial Intelligence)

B.S. Abdur Rahman Crescent Institute of Science and Technology

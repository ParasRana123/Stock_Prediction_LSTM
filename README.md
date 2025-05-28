# Stock Price Prediction using LSTM (Apple Inc.)

This project demonstrates how to predict future stock prices using **Long Short-Term Memory (LSTM)** neural networks. We used historical stock data from **Apple Inc. (AAPL)** and implemented a time series forecasting pipeline using deep learning with Python.

🔗 **Dataset Source:** [Tiingo](https://www.tiingo.com/) (via `pandas_datareader`)

## Features

- 📉 **Time Series Forecasting** using deep LSTM architecture
- 🔢 **Data Preprocessing** with `MinMaxScaler`
- 🧪 **Train/Test Split** for model evaluation
- 🔁 **Custom LSTM Training** (sample-by-sample)
- 🔮 **30-Day Future Prediction** after last known value
- 📊 **Visualization** of real vs predicted stock prices

## Tech Stack

- **Language**: Python
- **Libraries**:
  - `pandas`, `numpy`, `matplotlib`
  - `pandas_datareader`
  - `scikit-learn`
  - `tensorflow` (Keras)

## Project Structure

```bash
├── main.ipynb          # Core LSTM model prediction pipeline     
├── AAPL.csv            # Downloaded stock data
├── requirements.txt    # Python dependencies
└── README.md           # Project Documentation
```

## How It Works

### 1. **Data Collection**
- Used `pandas_datareader` to fetch historical AAPL data from Tiingo.
- Data saved to `AAPL.csv` for reproducibility.

### 2. **Data Preprocessing**
- Extracted the `close` price.
- Applied `MinMaxScaler` for normalization (0–1 range).
- Reshaped and split the data into training and testing sets.

### 3. **Dataset Preparation**
- Created a function to build datasets based on a 100-time-step window.

### 4. **Model Building**
- Stacked 3 LSTM layers and a Dense layer for output.
- Loss Function: `Mean Squared Error`
- Optimizer: `Adam`

### 5. **Training Strategy**
- Used a **sample-wise training loop** (1 epoch per sample × 100 epochs total).

### 6. **Evaluation**
- Used RMSE (Root Mean Squared Error) for performance on train and test sets.
- Compared predicted vs actual prices using plots.

### 7. **30-Day Forecast**
- Used a rolling input window to forecast the next 30 days beyond the test set.

## Installation

> **Note**: Python Version greater than 3.8 needed.

1. **Clone the Repository**

```bash
git clone [repository-url]
cd NOVA
```

2. **Create and activate python virtual environment**

```bash
conda create -p venv python==3.12.0 -y
activate venv/
```

3. **Install all the requirements necessary for this project**

```bash
pip install -r requirements.txt
```

4. **Make an empty `Data` folder in root directory for Chatlogs and then create a file `chatlog.json` inside it**

```bash
mkdir Data
cd Data
echo. > chalog.json
```

5. **Start the Python application**

```bash
python test.py
```

## Contributing

We welcome contributions from the community! Whether you're interested in improving features, fixing bugs, or adding new functionality, your input is valuable. Feel free to reach out to us with your ideas and suggestions.

## License
This project is licensed under the MIT License - see the LICENSE file for details.

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

- **Frontend**: Tkinter (Python GUI Library)
- **AI/ML Integration**: Google Gemini
- **API Integration**: Google Calendar API
- **Voice Recognition**: Python SpeechRecognition
- **OS-Level Integration**: Python (pyttsx3, pyautogui, os subprocess)
- **Storage & Sync**: LocalStorage, Session Management

## Project Structure

```bash
├── test.py             # Main file combining all the code
├── Data
│   └── chalog.json     # Contains all the previous Chatlog
├── image.py            # Image analysis AI-code
├── jarvis.py           # Contains all multi-media tasks
├── todo.py             # Contains all the calender code
├── location.py         # Utility file for calender events
├── requirements.txt    # Contains all the requirements
└── README.md
```

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

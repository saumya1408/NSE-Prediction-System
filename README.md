# 📈 NSE Luminary AI: Advanced Stock Price Prediction with CNN-LSTM

> **A next-generation deep learning platform for stock price prediction, blending CNN-LSTM architectures with a modern interactive web dashboard.**

![GitHub last commit](https://img.shields.io/github/last-commit/yourusername/Stock-Price-Prediction)
![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![PyTorch](https://img.shields.io/badge/PyTorch-1.9.0%2B-orange)
![License](https://img.shields.io/badge/License-MIT-green)
![Issues](https://img.shields.io/github/issues/yourusername/Stock-Price-Prediction)
![Stars](https://img.shields.io/github/stars/yourusername/Stock-Price-Prediction?style=social)

---

<div align="center">
  <img src="docs/assets/demo_dashboard.gif" alt="Demo GIF" width="80%"/>
  <br>
  <em>Modern dashboard for multi-stock prediction, evaluation, and visualization</em>
</div>

---

## ✨ Overview

NSE Luminary AI is a production-grade platform for stock price prediction using a hybrid CNN-LSTM deep learning model. It empowers investors and researchers with:
- Real-time stock data ingestion
- Multi-stock, multi-timeframe predictions
- Interactive web dashboard
- Model evaluation, visualization, and export

<details>
<summary>🌟 <b>Key Highlights</b></summary>

- 🚀 **Hybrid CNN-LSTM Model**: Combines convolutional and recurrent layers for robust time-series forecasting.
- 📊 **Modern Web App**: Responsive, animated dashboard built with Flask, TailwindCSS, and Chart.js.
- 🔒 **Secure, Scalable Backend**: Modular Python codebase, ready for extension and deployment.
- 🧠 **AI/ML Best Practices**: Early stopping, mixed precision, L2 regularization, and volatility-aware prediction.
- 📈 **Rich Visualizations**: Interactive charts, metrics, and comparison tools.

</details>

---


## 🧱 Tech Stack

### Core Technologies
- **Python 3.8+** - Primary programming language
- **PyTorch** - Deep learning framework
- **Flask** - Web application framework
- **Pandas & NumPy** - Data manipulation
- **scikit-learn** - Data preprocessing and evaluation
- **yfinance** - Financial data collection

### Development Tools
- Git - Version control
- Virtual Environment - Dependency management
- Jupyter Notebook - For experimentation and analysis

## 🏗️ Project Structure

```
Stock-Price-Prediction/
├── web_app/                     # Flask web application
│   ├── static/                  # Static files (CSS, JS, images)
│   ├── templates/               # HTML templates
│   ├── app.py                   # Main Flask application
│   └── logs/                    # Application logs
├── scripts/                     # Core Python scripts
│   ├── lstm_trainer.py          # CNN-LSTM model definition and training
│   ├── data_fetcher.py          # Data collection from yfinance
│   ├── data_preprocessor.py     # Data cleaning and preparation
│   ├── predictor.py             # Price prediction logic
│   ├── evaluate.py              # Model evaluation metrics
│   └── logs/                    # Training logs
├── data/                        # Data storage
│   ├── raw/                     # Raw data from APIs
│   └── processed/               # Processed data for training
├── models/                      # Trained model weights
├── requirements.txt             # Python dependencies
└── README.md                    # Project documentation
```

## 🚀 Features

- **Hybrid CNN-LSTM Architecture**: Combines CNN's feature extraction with LSTM's sequence learning
- **Multi-timeframe Analysis**: Supports different timeframes for prediction
- **Real-time Data Fetching**: Automatically pulls the latest stock data
- **Interactive Web Interface**: User-friendly dashboard for predictions
- **Model Evaluation**: Comprehensive metrics including MSE, RMSE, and MAE
- **Scalable Backend**: Built with performance and scalability in mind

## 🛠️ Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/Stock-Price-Prediction.git
   cd Stock-Price-Prediction
   ```

2. **Create and activate virtual environment**
   ```bash
   python -m venv lstm_venv
   source lstm_venv/bin/activate  # On Windows: .\lstm_venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Set up environment variables**
   Create a `.env` file in the root directory with your configuration:
   ```
   FLASK_APP=web_app/app.py
   FLASK_ENV=development
   ```

## 📊 Usage

### Training the Model
```bash
python scripts/lstm_trainer.py
```

### Running the Web Application
```bash
flask run
```
Then open `http://127.0.0.1:5000` in your browser.

### Making Predictions
1. Select a stock symbol from the dropdown
2. Choose the prediction timeframe
3. View the predicted price chart and metrics

## 🧠 Model Architecture

The model combines CNN and LSTM layers for enhanced time-series prediction:

1. **CNN Layers**:
   - Two 1D convolutional layers with ReLU activation
   - Batch normalization and max pooling
   - Feature extraction from time-series data

2. **LSTM Layers**:
   - Two LSTM layers with dropout for regularization
   - Sequence learning and temporal pattern recognition

3. **Dense Layers**:
   - Fully connected layers for final prediction
   - Single output node for price prediction

## 📈 Performance

The model is evaluated using:
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)
- Mean Absolute Error (MAE)
- R² Score

## 🤝 Contributing

Contributions are welcome! Please follow these steps:
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📜 License

Distributed under the MIT License. See `LICENSE` for more information.

## 📬 Contact

Your Name - [@yourtwitter](https://twitter.com/yourtwitter) - your.email@example.com

Project Link: [https://github.com/yourusername/Stock-Price-Prediction](https://github.com/yourusername/Stock-Price-Prediction)

## 🙏 Acknowledgments

- [PyTorch](https://pytorch.org/) for the amazing deep learning framework
- [yfinance](https://pypi.org/project/yfinance/) for financial data
- [Flask](https://flask.palletsprojects.com/) for the web framework
- [scikit-learn](https://scikit-learn.org/) for data preprocessing and metrics

## 📌 Future Improvements

- [ ] Add more technical indicators as features
- [ ] Implement sentiment analysis from news and social media
- [ ] Add support for multiple stocks comparison
- [ ] Implement automated model retraining
- [ ] Add user authentication and portfolio tracking

---

<div align="center">
  Made with ❤️ by Your Name
</div>

# 📈 NSE Luminary AI: Advanced Stock Price Prediction with CNN-LSTM

> **A next-generation deep learning platform for stock price prediction, blending CNN-LSTM architectures with a modern interactive web dashboard.**

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![PyTorch](https://img.shields.io/badge/PyTorch-1.9.0%2B-orange)
![License](https://img.shields.io/badge/License-MIT-green)

---

<div align="center">
  <a href="https://drive.google.com/file/d/1jpGSw7rb4c8WpTFN4pr4SrPXsk4gYlyt/view?usp=sharing" target="_blank" style="display: inline-block; padding: 12px 24px; background-color: #4CAF50; color: white; text-decoration: none; border-radius: 4px; font-weight: bold; margin: 20px 0;">
    🎥 View Demo Video
  </a>
  <br><br>
  <img src="https://drive.google.com/uc?export=view&id=1laGMYoLQMYgs0nOhHBPKt9OCrkO7ebVs" alt="Dashboard Screenshot" width="90%"/>
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
- **Python 3.8+** — Primary programming language
- **PyTorch** — Deep learning framework
- **Flask** — Web application framework
- **Pandas & NumPy** — Data manipulation
- **scikit-learn** — Data preprocessing and evaluation
- **yfinance** — Financial data collection
- **Chart.js** — Data visualization (web dashboard)
- **TailwindCSS** — Modern UI styling

### Development Tools
- Git — Version control
- Virtual Environment — Dependency management
- Jupyter Notebook — For experimentation and analysis

---

## 🗂️ Project Structure & Data Flow

```
LSTM/
├── web_app/                  # Flask web application
│   ├── static/               # Frontend assets (CSS/JS)
│   ├── templates/            # Dashboard UI (HTML)
│   └── app.py               # API endpoints & routing
├── scripts/                 # Core ML scripts
│   ├── lstm_trainer.py      # Model training
│   ├── predictor.py         # Price prediction
│   ├── data_fetcher.py      # Fetch stock data
│   ├── data_preprocessor.py # Clean & normalize
│   └── evaluate.py          # Model evaluation
├── data/                    # Stock data
│   ├── processed/           # Raw CSVs
│   └── preprocessed/        # Processed NPYs
└── models/                  # Trained models
```

### 🔄 How It Works

1. **Data Pipeline**
   - Fetches stock data using yfinance
   - Preprocesses and normalizes the data
   - Saves processed data for training

2. **Model Training**
   - Trains CNN-LSTM model on historical data
   - Implements early stopping and validation
   - Saves best performing model

3. **Prediction**
   - Loads pre-trained model
   - Makes future price predictions
   - Adds volatility-based noise

4. **Web Interface**
   - Interactive dashboard
   - Real-time predictions
   - Performance metrics
   - Data visualization

---

## 🚀 Features

- **Hybrid CNN-LSTM Model** for time-series forecasting
- **Multi-stock, multi-timeframe** prediction
- **Interactive dashboard** with metrics, charts, and export
- **Real-time data ingestion** from yfinance
- **Volatility-aware predictions** (noise injection)
- **Model evaluation:** MSE, RMSE, MAE, R²
- **Production-ready backend** (modular scripts, logging)
- **Modern, responsive UI** (dark/light mode)

---

## 🛠️ Installation

```bash
# 1. Clone repository
$ git clone https://github.com/yourusername/Stock-Price-Prediction.git
$ cd Stock-Price-Prediction

# 2. Create and activate virtual environment
$ python -m venv lstm_venv
$ .\lstm_venv\Scripts\activate  # Windows
# Or: source lstm_venv/bin/activate  # Linux/Mac

# 3. Install dependencies
$ pip install -r requirements.txt

# 4. (Optional) Set environment variables
$ echo FLASK_APP=web_app/app.py > .env
$ echo FLASK_ENV=development >> .env
```

---

## 📊 Usage

### Train the Model
```bash
python scripts/lstm_trainer.py
```

### Run the Web App
```bash
flask run
# Open http://127.0.0.1:5000
```

### Predict Stock Prices
- Select a stock symbol
- Choose prediction days
- View interactive charts and metrics

---

## 🎬 Demo

<div align="center">
  <img src="https://drive.google.com/uc?export=view&id=1laGMYoLQMYgs0nOhHBPKt9OCrkO7ebVs" alt="Dashboard Screenshot" width="90%"/>
  <br>
  <em>Interactive Dashboard for Stock Price Prediction</em>
</div>

## 🏗️ System Architecture

```
┌───────────────────────────────────────────────────────────────┐
│                      User Interface                          │
│  ┌───────────────────────────────────────────────────────┐  │
│  │                  Web Dashboard                        │  │
│  │  ┌─────────────┐  ┌─────────────────┐  ┌───────────┐  │  │
│  │  │ Stock       │  │ Prediction      │  │ Model     │  │  │
│  │  │ Selection   │  │ Visualization   │  │ Metrics   │  │  │
│  │  └─────────────┘  └─────────────────┘  └───────────┘  │  │
│  └───────────────────────────────────────────────────────┘  │
└───────────────────────────────┬──────────────────────────────┘
                                │
┌───────────────────────────────▼──────────────────────────────┐
│                      Backend Services                        │
│  ┌─────────────────┐  ┌─────────────────┐  ┌─────────────┐  │
│  │  Flask API      │◄─┤  Data Pipeline  │◄─┤ yFinance   │  │
│  │  (app.py)       │  │  (preprocessing)│  │  API       │  │
│  └───────┬─────────┘  └────────┬────────┘  └─────────────┘  │
│          │                     │                            │
│  ┌───────▼────────────────────▼────────┐  ┌─────────────┐  │
│  │  CNN-LSTM Model (PyTorch)           │  │  Models     │  │
│  │  • 2x Conv1D + BatchNorm            │  │  Storage    │  │
│  │  • 2x LSTM Layers                   │  │  (models/)  │  │
│  │  • Dropout for regularization       │  │             │  │
│  └─────────────────────────────────────┘  └─────────────┘  │
└────────────────────────────────────────────────────────────┘
```

### 🧠 Model Architecture

```
Input Layer (150 timesteps)
       │
       ▼
┌─────────────────┐
│ Conv1D (64 filters)  │
│ BatchNorm + ReLU     │
└─────────┬───────────┘
          │
          ▼
┌─────────────────┐
│ MaxPool1D (2)   │
└────────┬─────────┘
         │
         ▼
┌─────────────────┐
│ Conv1D (32 filters)  │
│ BatchNorm + ReLU     │
└────────┬───────────┘
         │
         ▼
┌─────────────────┐
│ MaxPool1D (2)   │
└────────┬─────────┘
         │
         ▼
┌─────────────────┐
│ LSTM (50 units)  │
│ Dropout (0.2)    │
└────────┬─────────┘
         │
         ▼
┌─────────────────┐
│ LSTM (50 units)  │
│ Dropout (0.2)    │
└────────┬─────────┘
         │
         ▼
┌─────────────────┐
│ Dense (25)      │
│ ReLU Activation │
└────────┬─────────┘
         │
         ▼
┌─────────────────┐
│ Dense (1)       │
│ Linear Output   │
└─────────────────┘
```

---
## 🔌 API Endpoints

| Endpoint                      | Method | Description                             |
|-------------------------------|--------|-----------------------------------------|
| `/`                           | GET    | Dashboard (list stocks)                 |
| `/predict/<stock>/<days>`     | GET    | Predict future prices for stock         |
| `/original/<stock>?days=N`    | GET    | Get original stock data (last N days)   |
| `/evaluate/<stock>`           | GET    | Get model evaluation metrics            |

**Example:**
```bash
curl http://127.0.0.1:5000/predict/RELIANCE/30
```

---

## 🔒 Security & Authentication

> **Note:** No authentication is implemented by default. For production, consider adding:
- User authentication (Flask-Login, OAuth)
- API key/token protection
- HTTPS deployment
- Input validation & rate limiting

---

## 🧪 Testing

- Unit tests can be added for model, data, and API scripts (pytest recommended)
- Manual testing via the dashboard and API endpoints
- (Optional) Add CI workflow for automated tests

---

## 📚 Dataset

- **Source:** [yfinance](https://pypi.org/project/yfinance/) (NSE/BSE stocks)
- **Processed:** CSVs in `data/processed/`
- **Preprocessed:** Numpy arrays, scalers in `data/preprocessed/`
- **Features:** Close price, technical indicators (extendable)

---

## 🤖 AI/ML Details

- **Model:** CNN-LSTM hybrid (see architecture above)
- **Training:** Early stopping, mixed precision, L2 regularization
- **Prediction:** Volatility noise injection for realism
- **Evaluation:** MSE, RMSE, MAE, R² metrics

---

## 🧩 Algorithms & Logic

- **CNN Layers:** Feature extraction from time-series
- **LSTM Layers:** Sequence learning for temporal dependencies
- **Dense Layers:** Regression output
- **Noise Injection:** Adds historical volatility to predictions

---

## ⚙️ Configuration

<details>
<summary>Click to expand</summary>

- Most paths and settings are hardcoded in scripts (see `scripts/` and `web_app/app.py`)
- For advanced config, refactor to use environment variables or a config file
- Example `.env`:
  ```env
  FLASK_APP=web_app/app.py
  FLASK_ENV=development
  DATA_DIR=data/
  MODEL_DIR=models/
  ```
</details>

---

## 🔄 CI/CD Workflow

- No CI/CD by default. Recommended:
  - GitHub Actions for linting, testing, and deployment
  - Dockerize the app for reproducible builds

---

## ❓ FAQ

<details>
<summary>Click to expand</summary>

**Q: Can I use this for live trading?**
- No, this is for research/education only. Real trading requires more robust systems.

**Q: Can I add more stocks or indicators?**
- Yes! Add CSVs to `data/processed/` and retrain. Extend `data_preprocessor.py` for more features.

**Q: Is GPU required?**
- Recommended for training, not strictly required for inference.

**Q: How do I contribute?**
- See the [Contributing](#-contributing) section below.

</details>

---

## 🌱 Future Improvements

- [ ] Add more technical indicators
- [ ] Sentiment analysis from news/social
- [ ] Multi-stock comparison
- [ ] Automated model retraining
- [ ] User authentication & portfolio tracking

---

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📜 License

Distributed under the MIT License. See `LICENSE` for details.

---

## 🙏 Credits

- [PyTorch](https://pytorch.org/)
- [yfinance](https://pypi.org/project/yfinance/)
- [Flask](https://flask.palletsprojects.com/)
- [scikit-learn](https://scikit-learn.org/)
- [Chart.js](https://www.chartjs.org/)
- [TailwindCSS](https://tailwindcss.com/)

---

## 📬 Contact

**Your Name**  
[LinkedIn](https://www.linkedin.com/in/yourprofile) • [Twitter](https://twitter.com/yourtwitter) • your.email@example.com

---

<div align="center">
  Made with ❤️ by Your Name  
  <br>
  <sub>Optimized for technical recruiters & open-source contributors</sub>
</div>

---

## 🏅 Badges

![GitHub last commit](https://img.shields.io/github/last-commit/yourusername/Stock-Price-Prediction)
![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![PyTorch](https://img.shields.io/badge/PyTorch-1.9.0%2B-orange)
![License](https://img.shields.io/badge/License-MIT-green)
![Issues](https://img.shields.io/github/issues/yourusername/Stock-Price-Prediction)
![Stars](https://img.shields.io/github/stars/yourusername/Stock-Price-Prediction?style=social)

---

## 🧩 Extras

- Add your own screenshots, GIFs, and diagrams in `docs/assets/`
- For advanced deployment, see [Flask deployment options](https://flask.palletsprojects.com/en/latest/deploying/)
- For questions, open an [issue](https://github.com/yourusername/Stock-Price-Prediction/issues)

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

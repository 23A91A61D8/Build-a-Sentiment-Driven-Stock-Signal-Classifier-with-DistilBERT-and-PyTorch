# Build-a-Sentiment-Driven-Stock-Signal-Classifier-with-DistilBERT-and-PyTorch

## 🚀 Project Overview

This project builds an end-to-end machine learning pipeline that combines Natural Language Processing (NLP) and financial time-series analysis to predict stock trading signals.

The system fine-tunes a **DistilBERT Transformer model** on financial news sentiment data and combines the generated sentiment scores with stock market indicators to classify future stock movement signals such as:

* 📈 UP
* 📉 DOWN
* ⏸ HOLD

The project demonstrates practical applications of:

* Sentiment Analysis
* Transformer Models
* Feature Engineering
* Time-Series Analysis
* Financial ML Pipelines
* Backtesting Strategies

---

# 🛠️ Technologies Used

* Python
* Pandas
* PyTorch
* HuggingFace Transformers
* Scikit-Learn
* yfinance
* Docker
* Jupyter Notebook

---

# 📂 Project Structure

```bash
├── data/
├── models/
│   ├── finetuned_distilbert/
│   └── signal_classifier.joblib
├── notebooks/
│   └── analysis.ipynb
├── results/
├── Dockerfile
├── docker-compose.yml
├── requirements.txt
├── .env.example
└── README.md
```

---

# 📊 Workflow Architecture

## Stage 1: Sentiment Analysis

* Financial news headlines are collected
* DistilBERT model is fine-tuned using FinPhraseBank dataset
* Sentiment scores are generated for each headline

## Stage 2: Feature Engineering

* Historical stock data is collected using yfinance
* Lagged financial indicators are generated
* Daily sentiment scores are aligned with stock market data

## Stage 3: Signal Classification

* A machine learning classifier predicts:

  * UP
  * DOWN
  * HOLD

## Stage 4: Backtesting

* Trading signals are simulated
* Portfolio performance metrics are evaluated

---

# 📥 Dataset Sources

## Financial Sentiment Dataset

* FinPhraseBank Dataset

## Stock Market Data

* Yahoo Finance API using yfinance

---

# 🧠 Model Details

## NLP Model

* DistilBERT (`distilbert-base-uncased`)
* Fine-tuned for financial sentiment classification

## Signal Classification Model

* Logistic Regression
* Trained using:

  * Sentiment features
  * Lagged price indicators
  * Volatility metrics

---

# ⚙️ Setup Instructions

## 1️⃣ Clone Repository

```bash
git clone <repository-url>
cd Build-a-Sentiment-Driven-Stock-Signal-Classifier-with-DistilBERT-and-PyTorch
```

---

## 2️⃣ Create Virtual Environment

```bash
python -m venv venv
```

### Activate Environment

### Windows

```bash
venv\Scripts\activate
```

### Git Bash

```bash
source venv/Scripts/activate
```

---

## 3️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

---

# 🐳 Docker Setup

## Build Docker Container

```bash
docker compose up --build
```

---

# ▶️ Run Notebook

Open Jupyter Notebook:

```bash
jupyter notebook
```

Run:

```bash
notebooks/analysis.ipynb
```

from top to bottom.

---

# 📈 Output Artifacts

## Generated Files

### Models

* `models/finetuned_distilbert/`
* `models/signal_classifier.joblib`

### Results

* `results/features.csv`
* `results/performance_metrics.json`
* `results/backtest_results.json`
* `results/feature_comparison.json`

---

# 📊 Performance Evaluation

The project evaluates:

* Precision
* Recall
* F1-Score
* Total Portfolio Return
* Sharpe Ratio

---

# 📉 Backtesting Metrics

The trading strategy performance includes:

* Final Portfolio Value
* Total Return Percentage
* Sharpe Ratio

---

# 🔍 Feature Comparison

Three models are compared:

1. Sentiment-Only Model
2. Price-Only Model
3. Combined Feature Model

The combined model achieved better predictive performance by integrating NLP sentiment signals with stock price indicators.

---

# 🎯 Key Learnings

* Fine-tuning Transformer models for domain-specific NLP
* Handling financial time-series data
* Avoiding lookahead bias
* Building reproducible ML pipelines
* Combining NLP with quantitative finance

---

# 📌 Conclusion

This project demonstrates how financial news sentiment can be integrated with historical stock market indicators to build intelligent trading signal classifiers using modern NLP and machine learning techniques.

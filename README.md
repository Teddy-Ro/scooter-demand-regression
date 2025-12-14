# scooter-demand-regression
Demand forecasting for scooter-sharing service using time series regression analysis. Includes hourly demand aggregation, feature engineering (weather, calendar, promotional), and model comparison (Linear, Ridge, Lasso, RandomForest).

## 📊 Project Overview

This project develops a demand forecasting model for a scooter-sharing service using time series regression analysis. The model predicts hourly demand based on weather conditions, temporal patterns (hour, day of week, weekends), and promotional events.

## 📁 Project Structure

```
scooter-demand-regression/
├── notebooks/              # Jupyter notebooks for analysis
├── data/                   # Data files (not in repo)
├── requirements.txt        # Python dependencies
├── .gitignore             # Git ignore rules
├── LICENSE                # MIT License
└── README.md              # This file
```

## 🚀 Quick Start

### Installation

```bash
# Clone the repository
git clone https://github.com/Teddy-Ro/scooter-demand-regression.git
cd scooter-demand-regression

# Create a virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt
```

## 📈 Model Performance

Linear Regression (best model):
- Validation RMSE: ~13.0 trips/hour
- Validation R²: ~0.84 (explains 84% of demand variance)
- Test RMSE: ~13.5 trips/hour
- Test R²: ~0.85

## 🔍 Key Features

### Temporal Features
- Hour of day (0-23)
- Day of week (Monday-Sunday)
- Weekend indicator
- Promotional events (Monday 6-10am)

### Weather Features
- Temperature
- Precipitation
- Wind speed
- Cloud cover
- Sunshine duration

### Lag Features
- 1-hour demand lag
- 24-hour demand lag (previous day at same hour)
- 24-hour rolling average

## 📝 License

MIT License - see LICENSE file for details

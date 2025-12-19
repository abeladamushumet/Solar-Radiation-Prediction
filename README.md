# BAACUMEN: Solar Radiation Prediction Project ☀️

[![Python Version](https://img.shields.io/badge/python-3.8%2B-blue)](https://www.python.org/)

## 📖 Project Overview
This project is part of the **Baacumen Data Science, Analytics and AI Bootcamp**. Acting as Analytics Engineers at **MoonLight Energy Solutions**, we aim to optimize solar farm investments by predicting **Global Horizontal Irradiance (GHI)**. 

While the data is sourced from Benin, Sierra Leone, and Togo, the insights and predictive models are specifically designed to support Ethiopia's **National Electrification Program**, identifying high-potential regions such as **Afar, Oromia, and Amhara** for solar installations.

## 🎯 Business Objective
MoonLight Energy Solutions seeks to enhance operational efficiency and sustainability by deploying solar farms in high-potential regions. Our task is to develop a robust regression model to predict GHI using environmental measurements, thereby informing a strategic roadmap for solar expansion in Ethiopia.

## 🛠️ Tech Stack
- **Languages**: Python
- **Data Engineering**: Pandas, NumPy
- **Machine Learning**: Scikit-Learn, XGBoost, LightGBM
- **Visualization**: Matplotlib, Seaborn
- **Version Control**: Git & GitHub

## 📂 Repository Structure
```text
Solar-Radiation-Prediction/
├── data/                       # Raw and processed datasets
│   ├── solar_data.csv          # Combined raw data
│   └── solar_processed.csv     # Cleaned and engineered features
├── notebooks/                  # Jupyter notebooks for interactive analysis
│   ├── eda.ipynb               # Exploratory Data Analysis & Quality Checks
│   └── modeling.ipynb          # Model training, tuning, and evaluation
├── models/                     # Saved machine learning models
│   └── best_model.pkl          # Trained XGBoost model (serialized)
├── scripts/                    # Modular Python scripts
│   ├── data_processing.py      # Cleaning and feature engineering logic
│   └── __init__.py
├── reports/                    # Final documentation and figures
│   ├── report.md               # Detailed blog-style project report
│   └── figures/                # Visualizations extracted from analysis
├── requirements.txt            # Project dependencies
└── README.md                   # Project documentation
```

## 🚀 Key Findings & Modeling Results
Through rigorous EDA and feature engineering, we identified that **Direct Normal Irradiance (DNI)** and **Module Temperature** are the primary drivers of GHI.

### Model Performance
| Model | R² Score | RMSE |
| :--- | :--- | :--- |
| **XGBoost** | **0.9998** | **0.0139** |
| Random Forest | 0.9997 | 0.0166 |
| LightGBM | 0.9996 | 0.0185 |
| KNN | 0.9957 | 0.0632 |
| Linear Regression | 0.9945 | 0.0719 |

**Winner**: **XGBoost** yielded the highest accuracy, making it the recommended choice for MoonLight Energy Solutions' forecasting needs.

## ⚙️ Installation & Usage

1. **Clone the repository**:
   ```bash
   git clone https://github.com/abeladamushumet/Solar-Radiation-Prediction.git
   cd Solar-Radiation-Prediction
   ```

2. **Setup virtual environment**:
   ```bash
   python -m venv .venv
   .venv\Scripts\activate
   ```

3. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Run Analysis**:
   - Explore `notebooks/eda.ipynb` for data insights.
   - Run `notebooks/modeling.ipynb` to reproduce the model results.
   - Execute `python scripts/data_processing.py` to re-generate the processed dataset.


---
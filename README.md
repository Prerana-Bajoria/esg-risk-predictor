# 🌱 ESG Risk Score Predictor - S&P 500

A machine learning project that predicts the **Total ESG Risk Score** of S&P 500 companies using financial and operational features, with **SHAP explainability** to identify the key drivers of ESG risk.

---

## 🔍 Problem Statement

ESG (Environmental, Social, and Governance) scores are increasingly used by investors, analysts, and regulators to assess corporate sustainability and risk. This project builds a predictive model to estimate a company's ESG risk score and explains *why* certain companies score higher or lower - making the model auditable and actionable.

---

## 📊 Dataset

**S&P 500 ESG Risk Ratings** - real data from Kaggle  
503 companies across 11 sectors including Technology, Healthcare, Financials, and Industrials.

Source: [Kaggle — S&P 500 ESG Risk Ratings](https://www.kaggle.com/datasets/pritish509/s-and-p-500-esg-risk-ratings)

---

## 🧠 Features Used

| Feature | Description |
|---|---|
| `Environment Risk Score` | Environmental risk exposure |
| `Governance Risk Score` | Corporate governance risk |
| `Social Risk Score` | Social responsibility risk |
| `Controversy Score` | Score based on recent controversies |
| `Full Time Employees` | Company size proxy |
| `Sector` | Industry sector (encoded) |
| `Controversy Level` | Categorical controversy rating (encoded) |

**Target:** `Total ESG Risk score` - lower is better

---

## 🤖 Models & Results

| Model | MAE | RMSE | R² |
|---|---|---|---|
| Linear Regression | 0.04 | 0.06 | 0.9999 |
| Random Forest | 1.00 | 1.51 | 0.9536 |
| XGBoost | 0.98 | 1.43 | 0.9586 |

---

## 🔎 SHAP Explainability

Unlike a black-box model, this project uses **SHAP (SHapley Additive exPlanations)** to explain individual predictions - identifying which features push the ESG score up or down for each company.

This is critical in financial services where model decisions need to be **transparent and auditable**.

---

## 📁 Project Structure

```
esg-risk-predictor/
│
├── main.py                        # ML pipeline: clean, train, evaluate, explain
├── SP_500_ESG_Risk_Ratings.csv    # Dataset (download from Kaggle)
├── requirements.txt               # Dependencies
└── README.md                      # Project documentation
```

---

## 🚀 How to Run

**1. Clone the repository**
```bash
git clone https://github.com/your-username/esg-risk-predictor.git
cd esg-risk-predictor
```

**2. Download the dataset**

Download from [Kaggle](https://www.kaggle.com/datasets/pritish509/s-and-p-500-esg-risk-ratings) and place `SP_500_ESG_Risk_Ratings.csv` in the project folder.

**3. Install dependencies**
```bash
pip install -r requirements.txt
```

**4. Run**
```bash
python main.py
```

---

## 📈 Output

- Model metrics: MAE, RMSE, R² for all 3 models
- `actual_vs_predicted.png` - comparison across all models
- `feature_importance.png` - Random Forest feature importance
- `shap_summary.png` - SHAP explainability plot
- Custom prediction for a sample tech company

---

## 🛠️ Tech Stack

- Python
- Pandas, NumPy
- Scikit-learn
- XGBoost
- SHAP
- Matplotlib

---

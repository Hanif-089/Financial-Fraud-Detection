# 💳 Financial Fraud Detection System

An end-to-end machine learning web application built with **Streamlit**, **scikit-learn**, and **Plotly** to analyze financial transactions and flag potentially fraudulent activity in real time.

---

## ✨ Key Features

- **📊 Batch Prediction (CSV Upload):** Score thousands of transactions at once with an interactive fraud probability threshold slider (`0.00` – `1.00`).
- **🔎 Single Transaction Scoring:** Manually input transaction features (`Time`, `V1`–`V28`, `Amount`) for instant prediction, risk gauge visualization, and SHAP-based feature explanations.
- **📈 Live Evaluation & Visual Analytics:** Interactive Plotly charts including distribution donuts, amount histograms, time-series scatter plots, confusion matrices, ROC curves, and Precision-Recall curves (when ground-truth labels are present).
- **🕒 Session Prediction History:** Tracks all batch runs performed during a session with trend charts and summary KPIs.
- **🌓 Adaptive Light & Dark Mode:** Seamless theme switching across the entire UI and Plotly visualizations.
- **⬇️ Flexible Data Export:** Download full predictions, filtered views, or fraud-only records as CSV files.

---

## 🧠 Model Overview

| Metric | Score |
| :--- | :--- |
| **Algorithm** | Random Forest Classifier |
| **Dataset** | Credit Card Fraud Detection Dataset (Kaggle) |
| **Accuracy** | `99.95%` |
| **Precision** | `97.18%` |
| **Recall** | `72.63%` |
| **F1-Score** | `83.13%` |

*(Note: The app automatically discovers any `.pkl` model files placed inside the `app/` directory.)*

---

## 📁 Project Structure

```text
financial-fraud-detection/
├── app/
│   ├── app.py              # Main Streamlit dashboard application
│   └── model.pkl           # Trained scikit-learn classification model
├── .streamlit/
│   └── config.toml         # Streamlit theme & UI configuration
├── requirements.txt        # Python dependencies
└── README.md               # Project documentation
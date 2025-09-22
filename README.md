# 📊 High Frequency Realized Volatility Decomposition: An Empirical Study

This repository contains all materials for the **EC638 – Financial Econometrics** term paper and project at **IIT Bombay**.  
The study focuses on **realized variance (RV)**, **bipower variation (BV)**, and **jump variation (JV)** using high-frequency intraday (per-minute) Apple stock data, alongside forecasting benchmarks with the **HAR-RV model** and **GARCH-X model**.  

---

## 📂 Repository Structure

EC638-Financial_Econometrics/
│── 📄 report.pdf # Final report (LaTeX compiled)
│── 📄 presentation.pdf # Project presentation (slides)
│── 📄 financial_vol_project.ipynb# Main Jupyter/Kaggle notebook
│── 📁 streamlit_app/ # Streamlit mini-app source code
│ └── app.py
│── 📄 data.csv # Sample data (AAPL per-minute data)
│── 📄 requirements.txt # Python dependencies
│── 📄 README.md # This file


---

## 🔗 Project Links

- 📘 **Final Report (PDF):** Included in this repo  
- 🎥 **Presentation (Slides):** Included in this repo  
- 📓 **Kaggle Notebook:** [Financial Vol Project](https://www.kaggle.com/code/bhaveshtanan/financial-vol-project)  
- 💻 **GitHub Repository:** [EC638-Financial_Econometrics](https://github.com/007bhavesh/EC638-Financial_Econometrics)  

---

## 📑 Abstract

This project investigates **high-frequency realized volatility decomposition** using Apple’s intraday stock data. We compute and analyze **RV, BV, and JV** as measures of volatility and jumps, then apply **HAR-RV** and **GARCH-X** models for volatility forecasting.  

To ensure reproducibility, we provide both the **Kaggle notebook** for running the analysis in the cloud and a **Streamlit app** that visually demonstrates RV, BV, and JV with an interactive chart.  

---

## ⚙️ Methodology Overview

1. **Data**  
   - Apple (AAPL) per-minute intraday stock data.  
   - Resampled into daily realized measures (RV, BV, JV).  

2. **Volatility Decomposition**  
   - **RV (Realized Variance):** Total volatility.  
   - **BV (Bipower Variation):** Continuous volatility component.  
   - **JV (Jump Variation):** Sudden jumps/shocks.  

3. **Models Used**  
   - **HAR-RV model** – baseline for realized volatility forecasting.  
   - **GARCH-X model** – conditional variance approach with exogenous inputs.  

4. **Evaluation Metrics**  
   - RMSE, QLIKE.  
   - Visual comparison of predicted vs. actual realized measures.  

---

## 📊 Key Results

- **RV vs BV vs JV:** Clear identification of jumps in intraday stock data.  
- **HAR-RV Forecasting:** Captures persistence in volatility with daily, weekly, and monthly components.  
- **GARCH-X Comparison:** Provides a conditional variance-based benchmark.  
- **Evaluation:** HAR performed better in stability, while GARCH captured clustering.  

---

## 🖥️ Streamlit Mini-App

We developed a **Streamlit app** (`app.py`) for interactive visualization of realized measures.  
Run locally with:  


cd streamlit_app
streamlit run app.py

Features:
Interactive line charts for RV, BV, and JV.
Hover tooltips showing exact volatility values.
Explanations of each measure for non-technical audiences.

## 📖 How to Reproduce
Option 1: Kaggle (Recommended)
Run everything online without setup:
👉 Kaggle Notebook Link - https://www.kaggle.com/code/bhaveshtanan/financial-vol-project

Option 2: Local Setup
Clone the repo and install dependencies:
git clone https://github.com/007bhavesh/EC638-Financial_Econometrics.git
cd EC638-Financial_Econometrics
pip install -r requirements.txt

Run the notebook or the Streamlit app.

## ⚡ Requirements

The main libraries used are:
pandas, numpy, matplotlib, seaborn – data processing & plots
statsmodels, arch, scikit-learn – econometric models (HAR, GARCH)
streamlit, plotly – interactive app and visualizations
See requirements.txt for full list.

## 👨‍🎓 Author
Bhavesh Tanan (22B3018) – Department of Economics, IIT Bombay

## 📜 License

This repository is licensed under the **Apache License 2.0**.  
You are free to use, modify, and distribute this project, provided that you comply with the terms of the license.  

See the full license here: [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0)

# Fraud Detection Machine Learning Project

## 📋 Project Overview
This project implements a machine learning–based fraud detection system for e-commerce transactions. The system analyzes behavioral patterns, time-based features, and transaction metadata to identify fraudulent activities while minimizing impact on legitimate customers.

**Business Context:**  
Adey Innovations Inc. is experiencing significant financial losses due to fraudulent transactions. This project aims to build a predictive fraud detection model that automatically flags suspicious activities while maintaining a positive customer experience.

---

## 🎯 Project Goals
- **Business Impact:** Reduce fraud losses by accurately detecting fraudulent transactions  
- **Model Performance:** Achieve high recall (catch fraud) while maintaining strong precision (avoid false alarms)  
- **Explainability:** Provide transparent model decisions using SHAP values and feature importance  
- **Production Ready:** Design a pipeline suitable for real-time deployment  

---

## 📊 Dataset Description

### Primary Dataset: `Fraud_Data.csv`
- **Size:** 151,112 transactions, 11 features  
- **Time Period:** 2015  

**Key Features**
- `user_id` – Unique user identifier  
- `signup_time`, `purchase_time` – Timestamps  
- `purchase_value` – Transaction amount ($9–$154)  
- `device_id`, `source`, `browser`, `sex`, `age` – User metadata  
- `ip_address` – IP address in scientific notation  
- `class` – Target variable (0 = legitimate, 1 = fraud)  

### Supporting Dataset: `IpAddress_to_Country.csv`
- **Size:** 138,846 IP ranges  
- **Purpose:** Map IP addresses to countries for geolocation analysis  

### Additional Dataset (Optional): `creditcard.csv`
- **Purpose:** Bank transaction dataset with PCA features for comparison or extension  

---

## 🏗️ Project Structure

fraud-detection/
├── .gitignore
├── README.md
├── requirements.txt
├── data/
│   ├── raw/
│   └── processed/
├── notebooks/
│   ├── 01_data_cleaning.ipynb
│   ├── 02_modeling.ipynb
│   ├── 03_shap_explainability.ipynb
│   └── README.md
├── src/
│   ├── data_preprocessing.py
│   ├── feature_engineering.py
│   └── model_training.py
├── models/
├── reports/
│   └── interim_report.md
└── tests/

---

## 🔧 Installation & Setup

### Clone the Repository
git clone https://github.com/Aperca/fraud-detection.git
cd fraud-detection

### Create Virtual Environment
python -m venv venv  
source venv/bin/activate  

### Install Dependencies
pip install -r requirements.txt

---

## 🚀 Quick Start
jupyter notebook notebooks/01_data_cleaning.ipynb

---

## 📈 Key Findings
- 53.7% of fraud occurs within 1 minute of account creation  
- Fraud rate: 9.36% (9.7:1 legitimate to fraud ratio)  
- Total fraud exposure: $523,488  

---

## 🧪 Testing
python -m pytest tests/ -v

---

## 📄 License
Educational use only. Dataset usage subject to original terms.

# 🧠 CampusCALM
**Student Stress Level Prediction Using Ensemble Machine Learning**

[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://campuscalm.streamlit.app/)
[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![Scikit-Learn](https://img.shields.io/badge/scikit--learn-F7931E?logo=scikit-learn&logoColor=white)](https://scikit-learn.org/)

> **Short Summary:** An AI/ML-based application that identifies stress patterns and predicts student stress levels from psychological, physiological, social, environmental, and academic indicators, using an ensemble of classification models trained on a 2,000-respondent survey dataset.

---

### 📌 Project Properties
- **Author:** David Christian Golden Mahaviro
- **Context:** Group Class Assignment – Final Project Machine Learning (2026)
- **Role:** Data Analyst & Machine Learning Engineer
- **Tech Stack:** Python, Pandas, Scikit-learn, Imbalanced-learn (SMOTE), Matplotlib, Seaborn, Streamlit
- **Live Deployment:** [View Web App](https://campuscalm.streamlit.app/)

---

### 📖 Project Context
University students frequently face academic pressure, heavy workloads, sleep deprivation, and anxiety, which can severely elevate stress levels and negatively impact mental health, focus, and academic performance. **CampusCALM** was built to address this real-world academic problem by turning self-reported survey data into a reliable predictor for student stress levels (Distress / Eustress / Other-Mixed).

As the **Data Analyst & ML Engineer** for this group project, I was responsible for the entire modeling pipeline:
1. Performing Exploratory Data Analysis (EDA) and data cleaning.
2. Building, training, and evaluating four base classification models.
3. Designing and training the final ensemble model using majority voting.

---

### 📊 Dataset
All datasets used in this project are stored in the `data` folder as `.csv` files.
- **Title:** Stress Indicator Dataset for Mental Health Classification
- **Source:** [https://doi.org/10.17632/2gsjv8m7ch.1](https://doi.org/10.17632/2gsjv8m7ch.1)
- **Description:** A dataset containing 2,000 student respondents with 25 features representing stress factors. The features span five main categories: psychological, physiological, social, environmental, and academic (e.g., anxiety levels, sleep quality, study load, social support).

---

### ⚙️️ Methodology & Problem Solving

Student stress data collected through surveys is naturally noisy. It contains outliers (e.g., ages outside the target 18–22 range), imbalanced class distributions, and correlated features. 

- **EDA & Data Handling:** Explored class distributions, feature histograms, and demographic spread. Filtered out age outliers outside the intended 18–22 range and handled data noise using boxplot inspections across 1–5 scale features.
- **Feature Extraction & Preprocessing:** Built a correlation matrix to identify highly correlated features (threshold > 0.7). Applied `StandardScaler` to normalize feature scales and utilized **SMOTE** (Synthetic Minority Over-sampling Technique) exclusively on the training set to address class imbalance without data leakage.
- **Evaluation & Impact:** The final data-driven system successfully predicts stress levels with high reliability, delivering a robust classification engine for the dashboard.

---

### 🤖 Models
The trained machine learning models are stored in the `model` folder as Jupyter Notebooks (`.ipynb`).

| Model | Description |
| :--- | :--- |
| **Logistic Regression** | Baseline Model |
| **Random Forest** | Estimators & Feature Importance Analysis |
| **Support Vector Machine** | Linear Kernel |
| **K-Nearest Neighbors** | Default Hyperparameters |
| **Ensemble (Majority Voting)** | **Final Production Model (Combined RF + SVM + KNN)** |

*By benchmarking five models side-by-side using classification reports, confusion matrices, and F1 metrics, the Ensemble Majority Voting classifier was selected for outperforming individual base classifiers and providing greater predictive robustness.*

---

### 🚀 How to Run Locally

**1. Install Dependencies**  
Ensure Python 3.8+ is installed, then run the following command in your terminal:
```bash
pip install -r requirements.txt
```

> ## **How to run**
link demo deplyoment apps "CampusCalm" : https://campuscalm.streamlit.app/
or you can run in a local:
### 1. Install Dependencies
make sure Python 3.8+ installed, and run:
```bash
pip install -r requirements.txt
```

### 2. Training Model
retrain all model use Ensemble (Majority Voting):
```bash
# run in Visual Studio Code or Google Colab for have  .pkl.
```

### 3. Deployment (Streamlit)
run dashboard apps use Streamlit:
```bash
python -m streamlit run app.py
```
local address: [http://localhost:8501](http://localhost:8501)

---

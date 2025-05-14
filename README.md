#  Water Potability Prediction

A machine learning project to predict whether water is **safe for drinking (potable)** based on its chemical properties. The model is trained using real-world data and includes preprocessing, feature analysis, model training, evaluation, and an optional deployment interface.

---

##  Problem Statement

The goal is to build a reliable model that can classify water samples as **potable (1)** or **non-potable (0)** based on features such as pH, hardness, solids, chloramines, sulfate, and others. This model can assist health departments or local communities in assessing water quality efficiently.

---

##  Dataset

- **Source**: [Kaggle - Water Quality Dataset](https://www.kaggle.com/adityakadiwal/water-potability)
- **Records**: 3,276
- **Features**: 9 (pH, Hardness, Solids, Chloramines, Sulfate, Conductivity, Organic Carbon, Trihalomethanes, Turbidity)
- **Target**: `Potability` (0 = Not potable, 1 = Potable)

---

##  Exploratory Data Analysis (EDA)

- Handled **missing values** in columns like `Sulfate`, `ph`, and `Trihalomethanes`.
- Analyzed distributions and correlations.
- Identified **class imbalance** in the target variable (more non-potable samples).

---

##  Technologies & Tools

- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn
- XGBoost / RandomForest
- Streamlit (for deployment)

---

##  Project Workflow

Water-Potability-Prediction/
├── data/ # Raw and cleaned datasets
├── notebooks/ # Jupyter notebooks for EDA and modeling
├── models/ # Saved ML models (Pickle)
├── streamlit_app/ # Streamlit web app files (optional)
├── requirements.txt
└── README.md


---

## Model Building

- Used **Random Forest**, **XGBoost**, and **Logistic Regression** models.
- Applied **Standard Scaling** to improve performance.
- Evaluated using:
  - Accuracy
  - Precision & Recall
  - F1-score
  - Confusion Matrix

---

##  Results

| Model              | Accuracy | F1-score |
|-------------------|----------|----------|
| Random Forest      | 80.2%    | 78.5%    |
| XGBoost            | 82.4%    | 80.3%    |
| Logistic Regression| 74.5%    | 72.1%    |

 **XGBoost performed best overall.**

---

##  Challenges Faced

- Handling missing and skewed data during preprocessing.
- Dealing with **class imbalance** which affected model performance.
- Selecting the right features and tuning hyperparameters for better generalization.
- Building a clean and interactive Streamlit app for demo purposes.

---

##  Deployment (Optional)

Deployed using **Streamlit** for live prediction:
```bash
cd streamlit_app
streamlit run app.py
Use Cases
Quick assessment of water quality in remote areas.

Support tool for environmental researchers.

Educational demo for classification problems in machine learning.

Future Improvements
Integrate with sensors/IoT devices for real-time predictions.

Add geographic data to visualize risk zones.

Use deep learning models for more complex predictions.

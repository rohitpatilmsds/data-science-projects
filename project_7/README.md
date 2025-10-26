# ❤️ Heart Disease Prediction Using Machine Learning: A Comprehensive Analysis of Personal Health Indicators  

## 🩺 Introduction of Topic / Problem  

Cardiovascular diseases (CVDs), especially heart disease, are the **leading cause of death worldwide**. According to the **World Health Organization (2022)**, CVDs caused approximately **20.5 million deaths** globally—a number expected to rise. This staggering statistic underscores the urgent need for efficient, accessible early detection systems.  

By identifying individuals at **high risk** of heart disease before acute or chronic symptoms appear, healthcare professionals can offer preventive strategies, lifestyle recommendations, and timely medical interventions. Such predictive approaches improve individual outcomes and reduce the long-term public health burden of heart disease.  

This study explores **machine learning–based predictive modeling** to estimate the probability of heart disease using **personal health indicators**.  
Our primary research question:  
> *Which machine learning algorithm is most accurate and reliable in predicting heart disease based on personal health indicators?*  

The ultimate goal is to identify a model that clinicians can use to support early cardiovascular risk assessment.  

---

## 📊 Overview of Data Used  

The analysis utilizes the **“Personal Key Indicators of Heart Disease”** dataset from the **Centers for Disease Control and Prevention (CDC)**, publicly available on **Kaggle**.  
The version used: `heart_2022_no_nans.csv` — a cleaned dataset with no missing values.  

- **Total Records:** 246,022  
- **Total Features:** 40  

### Feature Categories  
- **Demographics:** Age, Sex  
- **Behaviors:** Physical Activity, Smoking  
- **Clinical History:** Diabetes, Stroke, Asthma  
- **Health Status:** Self-rated overall health  

Collectively, these features provide a holistic view of individual health, enabling a comprehensive basis for heart disease risk modeling.  

---

## 🔍 Methods of Analysis  

A systematic, reproducible analytic workflow was employed, consisting of four major phases:  

### 1. Exploratory Data Analysis (EDA)  
Goals: identify patterns, trends, and relationships among variables.  
Key tasks included:  
- **Distribution analysis** – of heart disease presence/absence and demographics  
- **Risk factor analysis** – quantifying associations with known CVD risk factors  
- **Correlation matrix** – identifying multicollinearity  
- **Chi-square tests** – assessing statistical significance for categorical variables  

### 2. Data Pre-processing  
Key preparation steps:  
- **Feature-target separation:** 39 predictors (X), 1 target (‘HadHeartAttack’)  
- **Encoding:**  
  - Label encoding for binary features (Yes/No → 1/0)  
  - One-hot encoding for categorical features  
- **Scaling:** Standardized numerical features (mean = 0, std = 1)  
- **Train-Test Split:** 80/20 stratified sampling to maintain class balance  

### 3. Model Building and Training  
Four diverse ML algorithms were trained and tuned:  
- **Logistic Regression** – Interpretable linear baseline model  
- **Random Forest** – Ensemble model reducing variance via averaging  
- **Support Vector Machine (SVM)** – Captures complex non-linear boundaries  
- **XGBoost (Extreme Gradient Boosting)** – High-performance gradient boosting model  

To mitigate class imbalance, models were configured with **balanced class weights** where applicable.  

### 4. Model Evaluation  
Evaluation used a two-pronged strategy:  
- **5-Fold Stratified Cross-Validation** – Ensures stable and unbiased estimates  
- **Holdout Test Set Evaluation** – Final model validation on unseen data  

Performance metrics:  
- **Accuracy** – Overall correctness  
- **Precision** – True positives among predicted positives  
- **Recall (Sensitivity)** – True positives among actual positives  
- **F1-Score** – Harmonic mean of precision and recall  
- **ROC-AUC** – Model’s discriminative power  

---

## 📈 Results & Findings  

### Model Performance  

| Model | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
|--------|-----------|------------|----------|------------|-----------|
| **Logistic Regression** | **0.8304** | 0.2109 | **0.7678** | **0.3309** | **0.8857** |
| Random Forest | 0.8298 | 0.2081 | 0.7540 | 0.3261 | 0.8809 |
| SVM | 0.9479 | **0.5595** | 0.2170 | 0.3127 | 0.8856 |
| XGBoost | 0.8363 | 0.2145 | 0.7499 | 0.3335 | 0.8830 |

**Key Findings:**  
- **Logistic Regression** achieved the best overall performance, particularly in recall and ROC-AUC.  
- **SVM**, while highly accurate, exhibited poor recall—missing a large proportion of true positive (heart disease) cases, making it unsuitable for clinical application.  

### Feature Importance  

The top predictors across models were consistent with established medical knowledge:  
1. **History of Angina** – Strongest predictor of future heart attack  
2. **Age Group** – Increasing risk with advancing age  
3. **History of Stroke** – Strong cardiovascular risk indicator  
4. **General Health** – Self-rated “fair” or “poor” strongly associated with heart disease  
5. **Difficulty Walking** – Reflects physical limitations tied to cardiovascular conditions  

---

## 🧠 Conclusion  

This project demonstrates the **promise of machine learning in early heart disease prediction**. Among the evaluated algorithms, **Logistic Regression** proved most suitable for clinical application—balancing interpretability, recall, and robustness (ROC-AUC = 0.8857).  

While SVM and XGBoost achieved high accuracy, their low recall rates make them less viable for sensitive medical use cases where **false negatives carry high risk**.  

Furthermore, feature importance analysis reinforced well-established cardiovascular risk factors, offering actionable insights for preventive care.  

Future directions include integrating the model into **clinical decision support systems**, expanding the dataset to include **genetic or biochemical markers**, and **refining predictive accuracy** through model ensemble techniques.  

---

## 🚀 Future Work  

- Normalize analysis across multiple datasets (e.g., other CDC health surveys)  
- Implement **Monte Carlo simulations** for probabilistic modeling  
- Develop **interactive web dashboards** for clinicians and policymakers  
- Conduct **longitudinal validation** using real-world patient outcomes  

---

## 🙏 Acknowledgements  

- **Centers for Disease Control and Prevention (CDC)** – For creating and sharing the Personal Key Indicators of Heart Disease dataset  
- **Kaggle** – For hosting open-access health data for public research  
- **Scikit-learn, XGBoost, Matplotlib, Seaborn** – For enabling efficient modeling and visualization  

---

## 📚 References  

Centers for Disease Control and Prevention. (2022). *Personal Key Indicators of Heart Disease – Kaggle.*  
[https://www.kaggle.com/datasets/kamilpytlak/personal-key-indicators-of-heart-disease](https://www.kaggle.com/datasets/kamilpytlak/personal-key-indicators-of-heart-disease)

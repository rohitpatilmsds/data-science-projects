# 💡 Predicting Health Insurance Charges: A Data Science Approach  

## 🩺 Introduction  

### The Problem  
Estimating **fair and accurate insurance premiums** remains one of the most complex challenges in the health insurance industry. Insurers must forecast healthcare costs before any medical service is rendered — often with limited information. This uncertainty can lead to mispriced premiums, reduced profitability, and perceived unfairness among customers.  

This project addresses this issue using **machine learning techniques** to model and predict **health insurance charges** based on individual attributes such as **age, BMI, and smoking status**. By leveraging predictive analytics, insurers can achieve more accurate pricing, minimize risk, and improve both customer satisfaction and market competitiveness.  

### Why It Matters  
Accurate charge prediction has both **financial and operational benefits**:  
- Enables fair and evidence-based premium pricing  
- Reduces adverse selection and improves underwriting precision  
- Helps insurers proactively identify high-risk individuals  
- Enhances customer trust through transparency and fairness  

Data-driven models empower insurers to align pricing strategies with regulatory compliance while improving overall risk management and sustainable growth.  

### Stakeholder Pitch  
> “Imagine pricing every policyholder’s premium using just a few data points — with high confidence and precision.”  

That is the value proposition of this analysis. By introducing **predictive modeling into pricing functions**, insurers can dramatically reduce uncertainty, mitigate risk, and increase profitability. Far from replacing actuarial models, these machine learning techniques **augment** them, positioning the organization for the future of precision pricing and transparent insurance practices.  

---

## 📚 Data Source  

The analysis uses a **publicly available Kaggle dataset** — *“Insurance Charges Dataset”* — commonly employed in both academic and industry benchmarking exercises.  

- **Records:** ~1,300 individuals  
- **Features:** Age, Sex, BMI, Children, Smoker, Region, and Charges  
- **Target Variable:** `charges` (total medical costs)  

Although the dataset is synthetic, it realistically mirrors real-world insurance data and provides an ideal testbed for building and evaluating predictive models. The dataset’s cleanliness and reliability make it suitable for developing data-driven pricing prototypes.  

---

## 🔍 Exploratory Data Analysis (EDA)  

EDA revealed strong, interpretable relationships between **insurance charges** and several predictors, particularly **smoking status, age, and BMI**.  

### Key Insights from EDA  
1. **Distribution of Insurance Charges:** Positively skewed — a small number of individuals have exceptionally high charges.  
2. **Charges vs. Age by Smoker Status:** Smokers consistently incur higher costs across all age groups.  
3. **Charges by BMI Category:** Higher BMI correlates strongly with increased medical costs.  
4. **Charges by Region:** Some regional variation exists but is relatively minor compared to smoking and BMI effects.  
5. **Demographic Distribution:** Gender and region are balanced; about 20% of the population are smokers.  

These observations confirm the presence of meaningful relationships and justify predictive modeling.  

---

## 🧮 Data Preparation  

### Feature Selection  
The dataset includes six features with logical, domain-based relationships to the target variable (`charges`):  
- **age, sex, bmi, children, smoker, region**  

Each was retained, as all features contribute potentially useful information.  

### Data Cleaning and Transformation  
1. **Feature Retention:** No rows were removed — each observation provides valuable variation for generalizable model training.  
2. **Categorical Encoding:**  
   - `sex`, `smoker`, and `region` were **one-hot encoded** into dummy variables to convert categorical information into numerical form.  
3. **Feature Scaling:** Continuous variables like `age` and `bmi` were standardized to improve algorithm convergence.  
4. **Final Dataset:** Fully numeric, model-ready, and consistent with best practices for regression modeling.  

---

## 🧠 Model Building and Evaluation  

### Objective  
Predict **insurance charges** — a continuous outcome — using regression-based machine learning algorithms.  

### Selected Features  
Based on domain knowledge and correlation analysis, three key predictors were selected for focused modeling:  
- `smoker_yes` – Strongest predictor; smokers incur significantly higher costs  
- `age` – Charges increase with age due to greater health risks  
- `bmi` – Higher BMI often correlates with obesity-related expenses  

### Models Trained  
1. **Linear Regression** – Baseline model offering interpretability  
2. **Quadratic Polynomial Regression** – Captures nonlinear effects and curvature  
3. **Cubic Polynomial Regression** – Tests for higher-order nonlinear patterns  

---

## 📊 Model Insights  

### Linear Regression  
- **Interpretability:** Clear, linear relationships  
- **Key Finding:** Smokers pay approximately **$23,500 more** on average  
- **Performance:** Test R² ≈ **0.82**, suggesting strong explanatory power  

### Quadratic Polynomial Regression  
- **Improvement:** Enhanced training R², lower test RMSE and MAE  
- **Behavior:** Captures curvature between BMI and charges  
- **Outcome:** Achieved best balance of accuracy and generalization  

### Cubic Polynomial Regression  
- **Observation:** Overfit the training data — higher complexity without meaningful test performance gains  
- **Conclusion:** Additional polynomial terms introduced noise, not predictive value  

---

## 🧩 Model Comparison Summary  

| Model | Training R² | Test R² | Interpretation |
|--------|--------------|----------|----------------|
| **Linear Regression** | High | **0.82** | Strong, interpretable baseline |
| **Quadratic Regression** | Higher | **Best overall** | Best accuracy–generalization balance |
| **Cubic Regression** | Very High | Lower | Overfitting detected |

---

## ✅ Conclusion  

This analysis evaluated **linear, quadratic, and cubic regression models** to predict healthcare insurance charges using **smoking status, age, and BMI** as primary predictors.  

- **Quadratic Regression** emerged as the optimal model, offering the best combination of predictive power and interpretability.  
- **Smoking status** was the most influential variable, followed by **age** and **BMI**.  
- Increasing model complexity beyond the quadratic form reduced generalization capability, confirming that **simplicity often supports robustness** in predictive modeling.  

These results demonstrate that **data-driven pricing models** can effectively enhance the precision, fairness, and transparency of premium estimation, providing measurable value for insurers and policyholders alike.  

---

## 🚀 Future Work  

- Expand modeling to include **interaction terms** and additional health indicators  
- Implement **regularization techniques** (Ridge, Lasso) to improve model stability  
- Explore **ensemble regressors** like Random Forest or XGBoost for non-linear feature relationships  
- Integrate predictive pricing models into **real-world underwriting workflows** for validation  

---

## 🙏 Acknowledgements  

- **Kaggle** – For providing the open-access health insurance dataset  
- **Scikit-learn, Pandas, NumPy, Matplotlib, Seaborn** – For enabling efficient analysis and visualization  
- **Healthcare data science community** – For continued research on transparent and fair predictive modeling  

---

## 📚 References  

Kaggle. (n.d.). *Insurance Dataset.*  
[https://www.kaggle.com/datasets/mirichoi0218/insurance](https://www.kaggle.com/datasets/mirichoi0218/insurance)

# 🚗 Used Car Price Prediction and Market Analysis for the Indian Market

## 🧭 Business Problem
For online marketplaces such as **Cars24**, accurate pricing of used cars is essential to remain profitable, ensure faster inventory turnover, and build trust with both buyers and sellers.  
Overpricing vehicles can lead to stagnant inventory, while underpricing results in direct revenue loss.  
This project develops a **data-driven pricing model** to estimate a used car’s fair market value (the *as-is price*) based on key vehicle attributes.

---

## 📜 Background
Over the past decade, India’s used car market has grown exponentially — driven by rising new car prices, aspirational demand, and the rise of certified pre-owned platforms like Cars24.  
To remain competitive, marketplaces must understand **vehicle depreciation patterns** and **value drivers**.  
This project focuses on quantifying those factors through data science and predictive modeling.

---

## 📊 Dataset Overview
**Primary Dataset:** `cars24data.csv`  
Source: [Kaggle – Used Car Price Data from Cars24](https://www.kaggle.com/datasets/amanrajput16/used-car-price-data-from-cars24)

**Dataset Summary:**
- 1,445 records of used car listings from Cars24.com  
- Each record includes technical, mechanical, and condition-based attributes.

**Data Dictionary:**
| Feature | Description |
|----------|-------------|
| Model Name | Make and model of the car (e.g., “2017 Maruti Swift VXI”) |
| Price | Listing price of the car in INR *(Target Variable)* |
| Manufacturing Year | Year of manufacture |
| Engine Capacity | Engine capacity in cubic centimeters (CC) |
| Spare Key | Availability of a spare key (“Yes”/“No”) |
| Transmission | Transmission type (“Manual”/“Automatic”) |
| KM Driven | Total kilometers driven |
| Ownership | Number of previous owners |
| Fuel Type | Type of fuel (“Petrol”, “Diesel”, “CNG”) |
| Imperfections | Count of physical imperfections |
| Repainted Parts | Number of repainted parts |

---

## 🧹 Data Preparation
1. **Feature Engineering**
   - Created `Car_Age` = Current Year (2025) – `Manufacturing Year`
2. **Categorical Encoding**
   - One-hot encoded categorical variables: `Spare Key`, `Transmission`, and `Fuel Type`
3. **Feature Reduction**
   - Removed `Model Name` due to high cardinality
4. **Data Splitting**
   - 80% Training Set, 20% Test Set for unbiased evaluation

---

## 🧠 Methods
We implemented **supervised regression models** to predict used car prices:

1. **Linear Regression (Baseline Model)**  
   Established a benchmark for prediction accuracy using a simple linear relationship.
   
2. **Random Forest Regressor (Advanced Model)**  
   An ensemble-based algorithm that improves predictive performance by aggregating multiple decision trees.

**Model Evaluation Metrics:**
- **Mean Absolute Error (MAE):** Average deviation between predicted and actual prices  
- **R² (R-squared):** Proportion of variance in the price explained by the model

---

## 📈 Results and Analysis

### 🔹 Model Performance
| Model | R² | MAE (₹) |
|--------|----|----------|
| Linear Regression | 0.69 | 78,000 |
| Random Forest | **0.83** | **54,435** |

✅ The **Random Forest** model achieved superior accuracy and generalization.

### 🔹 Feature Importance
| Feature | Relative Importance |
|----------|---------------------|
| Engine Capacity | 63% |
| Car Age | 23% |
| Kilometers Driven | 5.5% |
| Imperfections / Repainted Parts | Minor but measurable impact |

---

## 💡 Key Insights
- **Engine capacity** is the strongest predictor of price.  
- **Car age** is inversely proportional to price — older cars depreciate significantly.  
- **Physical condition** (imperfections, repainting) contributes meaningfully to valuation.  
- The **Random Forest model** strikes the right balance between accuracy and interpretability.

---

## 🧩 Assumptions
- The dataset from Cars24 accurately represents the Indian used car market.  
- Selected features are sufficient for predicting price.  
- Relationships in historical data remain valid for future predictions.

---

## ⚠️ Limitations
- **Feature Scope:** ‘Model Name’ omitted; inclusion could boost accuracy.  
- **Sample Size:** 1,445 records — limited for complex ML models.  
- **Market Factors:** Does not account for city-level or seasonal price fluctuations.  
- **Static Model:** Must be retrained periodically to adapt to market trends.

---

## 🧗 Challenges
- **High Cardinality:** ‘Model Name’ feature required complex encoding.  
- **Data Sparsity:** Small dataset limited model complexity.  
- **Interpretability:** Random Forest models are less transparent than linear models.

---

## 🔮 Future Applications
- **Dynamic Pricing API:** Deploy as a REST API for real-time price estimation.  
- **Customer Price Estimator App:** Web app for sellers to estimate car value instantly.  
- **Residual Value Forecasting:** Predict future resale values for leasing or fleet management.  
- **Market Trend Monitoring:** Re-train models periodically to identify pricing trends.

---

## 💼 Recommendations
1. **Adopt Data-Driven Pricing** — Use the Random Forest model as a support tool for pricing specialists.  
2. **Highlight Price Drivers** — Showcase key features (engine size, car age, mileage) in listings.  
3. **Optimize Inventory Procurement** — Identify undervalued listings for better sourcing.  
4. **Feature Engineering Investment** — Enhance performance by encoding ‘Model Name’ properly.

---

## 🧩 Implementation Plan
### **Phase 1: Offline Validation (1–2 Months)**
- Back-test model on unseen data  
- Review predictions with pricing specialists  
- Improve feature engineering  

### **Phase 2: Internal Tool Development (2–3 Months)**
- Develop internal REST API  
- Build a simple dashboard for pricing specialists  

### **Phase 3: A/B Testing (3–6 Months)**
- Test model-driven pricing vs. manual pricing  
- Track performance metrics like time-to-sell and customer satisfaction  

### **Phase 4: Full Integration (Ongoing)**
- Integrate model into pricing workflow  
- Establish retraining and monitoring pipelines  

---

## ⚖️ Ethical Assessment

### **Algorithmic Bias**
Ensure fairness across car types and brands.  
✅ *Mitigation:* Regular audits and representative sampling.

### **Transparency and Explainability**
Random Forest is less interpretable.  
✅ *Mitigation:* Use **SHAP** or **LIME** to explain individual predictions.

### **Data Privacy**
No Personally Identifiable Information (PII) present in the dataset.  
✅ *Mitigation:* Maintain anonymization when integrating proprietary data.

---

## ❓ Top 10 Stakeholder Questions
1. How accurate is the model in real-world scenarios?  
2. Would including the car’s brand improve predictions?  
3. How often will the model be retrained?  
4. Can this model generalize to other vehicle types?  
5. What was the most surprising insight?  
6. How do you handle regional pricing differences?  
7. What steps are taken to ensure fairness?  
8. How long will implementation take?  
9. What are the limitations of a Cars24-only dataset?  
10. How can individual sellers benefit from this model?

---

## 📚 References
- Breiman, L. (2001). *Random Forests.* Machine Learning, 45(1), 5–32.  
- GeeksforGeeks. (2025). *Analyzing Selling Price of Used Cars Using Python.*  
  Retrieved from [GeeksforGeeks](https://www.geeksforgeeks.org/python/analyzing-selling-price-of-used-cars-using-python/)  
- IMARC Group. (2023). *India Used Car Market: Trends, Share, Growth, and Forecast 2025–2033.*  
  Retrieved from [IMARC Group](https://www.imarcgroup.com/india-used-car-market)

---

## 📎 Appendix
The following visualizations illustrate the model development and results:
1. Distribution of Used Car Prices  
2. Price vs. Car Age and Engine Capacity  
3. Feature Importance Chart  
4. Model Comparison (Linear vs Random Forest)  

---

**Author:** *Rohit*  
**Project Type:** Machine Learning / Predictive Modeling  
**Tools Used:** Python, Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn  
**Date:** 2025

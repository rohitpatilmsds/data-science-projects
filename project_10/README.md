# 📱 The Relationship Between Screen Time and Mental Wellness

## 🧩 Business Problem

With the rapid adoption of digital devices, screen time has become an integral part of daily life. However, its implications for mental health are increasingly recognized as a significant public health concern. Research indicates associations between prolonged screen exposure and adverse psychological outcomes such as **anxiety, depression, and reduced overall wellness**, particularly among **young adults and adolescents**.

Organizations and health professionals must better understand these relationships to design **practical wellness strategies and digital health policies**.

### Research Questions

1. To what degree is there a correlation between **self-reported anxiety**, **sleep quality**, and **total daily screen time**?  
2. Which **screen time activities** (e.g., work vs. leisure) are most associated with mental wellness?  
3. How do **demographic factors** such as age, gender, and occupation influence the relationships between screen time, anxiety, and mental health?

---

## 🕰️ Background / History

Earlier studies on “screen time” primarily examined **television exposure**, but the rise of **smartphones, computers, and social media** has vastly expanded both usage and its implications.  
Initial research focused on children’s developmental outcomes but has since extended to adults as **remote work and digital engagement** increased.

Studies such as *Stiglic & Viner (2019)* found strong links between **social media use** and **mental health issues**. The **COVID-19 pandemic** further blurred boundaries between work and leisure, making screen time a 24/7 phenomenon that affects **sleep, mood, and productivity**.

---

## 📊 Datasets

The dataset used in this project is the **“Screen Time vs Mental Wellness Survey – 2025”** by **Kumar (2025)**, available on [Kaggle](https://www.kaggle.com/datasets/adharshinikumar/screentime-vs-mentalwellness-survey-2025).

### Key Variables

| Variable | Description |
|-----------|-------------|
| `user_id` | Unique respondent ID |
| `age` | Age of respondent |
| `gender` | Gender of respondent |
| `occupation` | Occupation type |
| `work_mode` | Work environment (Remote / In-person) |
| `screen_time_hours` | Total daily screen time |
| `work_screen_hours` | Hours spent on work-related screens |
| `leisure_screen_hours` | Hours spent on leisure-related screens |
| `sleep_hours` | Average hours of sleep per night |
| `sleep_quality_1_5` | Sleep quality on a scale of 1 to 5 |
| `stress_level_0_10` | Self-reported stress level |
| `mental_wellness_index_0_100` | Composite index of mental wellness |

---

## 🧠 Methods

### 1. Data Cleaning and EDA
- Addressed missing values using **mean imputation**  
- Conducted **exploratory data analysis (EDA)** to assess distribution, outliers, and correlations  

### 2. Feature Engineering
- Encoded categorical variables (`gender`, `occupation`, `work_mode`) using **one-hot encoding**  
- Created a new feature: **`screen_time_ratio` = leisure_screen_hours / work_screen_hours**  

### 3. Visualization
- Used **Matplotlib** and **Seaborn** for histograms, scatter plots, and correlation heatmaps  

### 4. Regression Modeling
- Evaluated **10 regression algorithms**, including:  
  Linear, Lasso, Ridge, ElasticNet, SVR, Random Forest, and Gradient Boosting  
- Predicted **`mental_wellness_index_0_100`**

### 5. Model Selection
- Compared models using **R²**, **MAE**, and **RMSE**  
- **Ridge Regression** performed best, achieving **R² = 0.9336**

---

## 📈 Analysis & Insights

### Screen Time Distribution
Most participants reported **4–10 hours** of daily screen use, with a peak near **8 hours**—a level aligned with modern norms.

### Occupation & Sleep
Students and software engineers showed **lower sleep quality** compared to teachers and school administrators, suggesting occupational influence on digital fatigue.

### Leisure Screen Time & Wellness
A **negative correlation** exists between leisure screen time and mental wellness.  
Higher leisure screen usage corresponds with **lower wellness scores**.

### Correlation Highlights
| Variable | Correlation with Wellness |
|-----------|---------------------------|
| Sleep Quality | **+0.78** |
| Screen Time | **−0.69** |
| Stress Level | **−0.92** |

These findings confirm **sleep quality and stress** as dominant predictors of mental wellness.

---

## 🧩 Conclusion

This analysis reveals a **statistically significant negative relationship** between screen time—particularly leisure usage—and mental wellness.  
Sleep quality emerged as the **strongest positive predictor** of mental health.

📊 **Key takeaway:** Reducing leisure screen time and improving sleep quality may significantly enhance psychological well-being.

---

## ⚙️ Assumptions

- Survey responses are **truthful and reliable**  
- The sample is **representative** of broader technology users  
- Self-reported measures reflect **actual wellness states**

---

## ⚠️ Limitations

- **Correlation ≠ Causation:** Screen time may reflect, not cause, poor wellness  
- **Self-reported data** are prone to recall bias  
- **Generalizability** limited to similar populations

---

## 🧱 Challenges

Controlling for confounding variables (e.g., **diet, social life, health conditions**) was difficult, as they also influence mental wellness but were not captured in the dataset.

---

## 💡 Future Uses & Applications

- **Workplace wellness programs** promoting balanced digital habits  
- **Educational tools** for students to manage screen exposure  
- **Digital wellness apps** offering personalized recommendations  

---

## ✅ Recommendations

1. **Promote digital hygiene** — Encourage breaks, work–leisure boundaries, and reduced after-hours communication  
2. **Encourage mindful tech use** — Differentiate between *high-value* (connection) and *low-value* (passive scrolling) use  
3. **Prioritize sleep quality** — Integrate sleep awareness into wellness programs  

---

## 🗓️ Implementation Plan

| Phase | Description |
|--------|--------------|
| **1. Awareness** | Launch internal campaigns highlighting digital wellness findings |
| **2. Tools & Training** | Provide workshops, mindfulness resources, and digital management tools |
| **3. Policy & Culture** | Adopt cultural initiatives like “no-meeting Fridays” and focus hours |

---

## ⚖️ Ethical Considerations

All data were **anonymized** to ensure privacy.  
Results are reported **in aggregate**, avoiding individual-level conclusions or stigma.  
The project emphasizes **responsible communication** and **data ethics** in health analytics.

---

## 📚 References

- Kumar, A. (2025). *Screen Time vs Mental Wellness Survey - 2025*. Kaggle.  
  [https://www.kaggle.com/datasets/adharshinikumar/screentime-vs-mentalwellness-survey-2025](https://www.kaggle.com/datasets/adharshinikumar/screentime-vs-mentalwellness-survey-2025)

- Stiglic, N., & Viner, R. M. (2019). *Effects of screen time on the health and well-being of children and adolescents: A systematic review of reviews.* BMJ Open, 9(1), e023191.  
  [https://bmjopen.bmj.com/content/9/1/e023191](https://bmjopen.bmj.com/content/9/1/e023191)

---

## 🙋 10 Audience Questions

1. Does screen time *cause* poor mental wellness or *reflect* it?  
2. Were gender or age differences significant?  
3. What was the most surprising finding?  
4. How might results differ with **objective tracking data**?  
5. Which occupations show the greatest risk?  
6. How do you define *productive* vs. *non-productive* screen time?  
7. What explains the remaining **6.6% variance** not captured by the model?  
8. How could employers implement these insights without privacy invasion?  
9. What single message should individuals take away?  
10. What’s next for this research?

---

## 🙏 Acknowledgements

- **Kumar (2025)** – for providing the *Screen Time vs Mental Wellness* dataset  
- **Kaggle Community** – for open data collaboration  
- **Matplotlib, Seaborn, Scikit-learn, Pandas** – for enabling robust analysis and visualization tools  

# 🛫 TSA Complaints – Strategic Analysis of Passenger Experience Data

[![Python](https://img.shields.io/badge/Python-3.9-blue.svg)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

---

## 📌 Project Overview
The Transportation Security Administration (TSA) receives thousands of complaints from passengers annually. While often treated as isolated incidents, this analysis shows that **complaints are not random but systemic, recurring, and increasing over time**.  

This project builds a **data-driven narrative** aimed at senior TSA executives and DHS stakeholders, with one persuasive goal:  
👉 Secure approval for **a nationwide training program** to improve passenger experience and procedural consistency.  

---

## 🎯 Purpose
The analysis is designed to help TSA leadership understand three key points:
1. Passenger discontent is **systemic, quantifiable, and rising**.  
2. Specific, identifiable **procedural and behavioral issues** generate most complaints.  
3. A **targeted investment in training** is the most logical solution to address these root causes.  

---

## 📊 Dataset
- **Source:** TSA complaints data (FOIA/public release assumed).  
- **Scope:** Multiple years of nationwide complaint records.  
- **Features:**  
  - Complaint category and subcategory  
  - Airport code and location  
  - Date of complaint  
  - Narrative description (text)  

**Ethical Considerations:**  
- No personally identifiable information (PII) included.  
- All data cleaning, transformations, and assumptions are transparently documented in the notebook.  
- The analysis emphasizes **systemic improvement, not blame** of individuals or airports.  

---

## 🔄 Project Workflow
1. **Data Cleaning & Transformation**  
   - Renamed columns for clarity (`airport_x → iata_code`)  
   - Preserved all complaint counts; filled missing locations with `"Unknown"`  
2. **Exploratory Data Analysis (EDA)**  
   - Trend analysis of monthly/annual complaints  
   - Category and subcategory breakdowns  
   - Location-based complaint patterns  
   - Text analysis of complaint narratives (word cloud)  
3. **Visualization Strategy**  
   - Designed using Gestalt principles for clarity and impact  
   - Applied intentional color scales, spacing, and alignment  
   - Created a visual “funnel” → high-level overview → drill-down to actionable insights  
4. **Narrative Development**  
   - Built a persuasive storyline: "Systemic issue → Specific pain points → Training solution"  

---

## 📈 Key Findings
- **Complaints are increasing year-over-year**, with sharp spikes during peak travel seasons.  
- **Procedural issues** (screening, divestiture, staffing) and **behavioral issues** (courteousness, professionalism) dominate complaints.  
- A **small number of major hub airports** account for a disproportionate share of complaints.  
- Word cloud analysis highlights **recurring pain points** such as “rude,” “unprofessional,” and “confusing.”  

---
## 🚀 Future Work

- Normalize complaint counts by **passenger volume** for contextual fairness  
- Build **predictive models** to forecast complaint trends at specific airports  
- Develop an **interactive dashboard** for leadership to monitor ongoing complaint data in real time  
- Conduct **qualitative text analysis (NLP)** on complaint narratives to identify deeper sentiment patterns  
---
## 🙏 Acknowledgements

- **Transportation Security Administration (TSA)** – For making the data accessible through public channels  
- **Department of Homeland Security (DHS)** – For operational context and mission-driven objectives  
- **Matplotlib, Seaborn, Plotly** – For enabling high-quality data visualizations  
---

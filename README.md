# 🏙️ Clustering NYC 311 Service Requests for Smarter City Management

This project analyzes **New York City 311 Service Requests** to identify complaint patterns, optimize resource allocation, and assess service effectiveness. By applying **association rule mining, clustering techniques, and text mining**, we uncover actionable insights that can help city agencies improve service delivery and response efficiency.

---

## 📌 Problem Statement
NYC 311 receives millions of service requests each year, covering complaints like noise, heating, parking, and infrastructure.  
Key challenges include:
- Identifying complaint patterns
- Detecting geographic and temporal clusters
- Understanding agency workload and efficiency
- Extracting themes from resolution descriptions  

**Goal:** Enable smarter city management through data-driven insights.

---

## 📊 Dataset
- **Source:** [NYC Open Data – 311 Service Requests (2010–Present)](https://data.cityofnewyork.us/Social-Services/311-Service-Requests-from-2010-to-Present/erm2-nwe9/about_data)  
- **Size:** 28M+ records, 41 features  
- **Sample Used:** 1% of total dataset via stratified sampling  
- **Features Analyzed:** Complaint type, agency, borough, timestamps, location (lat/long, zip), resolution description, and request channel  

---

## 🛠️ Methodology
### 1. **Preprocessing**
- Missing value handling for timestamps, locations, and complaint descriptors  
- Feature engineering (complaint resolution time, time-based features)  
- Encoding categorical variables (one-hot, label encoding)  
- Scaling numerical features  
- PCA for dimensionality reduction (~90% variance retained)  

### 2. **Analysis & Models**
- **Association Rule Mining (Apriori Algorithm)**  
  - Found recurring complaint patterns by borough, agency, and type  
  - Example: *Noise complaints dominate weekends in Manhattan & Brooklyn; parking handled entirely by NYPD*  

- **Clustering Analysis (Hierarchical & K-Means)**  
  - Segmented complaints into geographic and density-based clusters  
  - High-density clusters in Brooklyn, Manhattan, and Bronx → slower resolution times  
  - PCA improved cluster separation, despite scalability limits  

- **Text Mining (BoW, TF-IDF, Topic Modeling, Sentiment Analysis)**  
  - Extracted themes from resolution descriptions  
  - Identified 4 distinct topics (General, Public Space, Urgent, Housing)  
  - Sentiment trends showed seasonal variations (lower in winter months due to heating issues)  

---

## 🔑 Key Findings
- **Complaint Categories:** Noise, heating, and parking dominate (50%+ of total complaints).  
- **Geographic Trends:** Brooklyn & Queens have the highest volume; Manhattan has concentrated hotspots.  
- **Temporal Trends:** Peaks on weekdays, especially Tuesdays; midnight spikes for noise.  
- **Agency Workload:** NYPD, HPD, and DOT handle the majority of cases.  
- **Resolution Efficiency:** High-density complaint zones correlate with slower resolution.  
- **Sentiment Analysis:** Lower satisfaction during winter months (heating) and November resource bottlenecks.  

---

## 💡 Impact & Applications
- **Faster Responses:** Allocate resources dynamically to high-complaint clusters.  
- **Urban Planning:** Identify persistent service gaps for long-term city improvements.  
- **Automated Complaint Routing:** Use text mining to direct requests to the right agencies.  
- **Crisis Management:** Anticipate demand surges (e.g., heating in winter, noise in nightlife-heavy areas).  

---

## 🛠️ Tools & Libraries
- **Python:** `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`, `mlxtend`, `nltk`, `gensim`  
- **Techniques:** PCA, Apriori Association Rules, K-Means, Hierarchical Clustering, LDA Topic Modeling, Sentiment Analysis  

---

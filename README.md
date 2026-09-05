# Aadhaar Growth & Maintenance Phase Analysis

## 📌 Project Overview

This project analyzes UIDAI Aadhaar data to understand whether different regions are in a **Growth Phase** (new enrolment focused) or a **Maintenance Phase** (update focused).

The project also analyzes **5–17 age-group demographic and biometric updates** to understand Aadhaar update activity and identify areas that may require enrolment camps or biometric-update campaigns.

---

## 🎯 Problem Statement

Our project identifies whether regions are in an **Aadhaar Growth or Maintenance phase** and maps **5–17 age-group biometric activity** to help UIDAI target enrolment camps and biometric-update campaigns more effectively.

---

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Jupyter Notebook
* CSV Dataset
* Exploratory Data Analysis (EDA)
* Feature Engineering
* Data Cleaning
* Data Visualization

---

## 📂 Project Workflow

The project is divided into three major stages:

### 1. Data Cleaning

The raw UIDAI dataset was cleaned by:

* Removing unnecessary columns
* Removing duplicate records
* Removing extra spaces from state names
* Standardizing inconsistent state names
* Converting the date column into datetime format
* Keeping only valid 6-digit pincodes
* Saving the cleaned dataset as `uidai_cleaned_simple.csv`

---

### 2. Feature Engineering

New features were created to make the Aadhaar data easier to analyze.

#### Total Enrolment

Total enrolment is calculated using:

`age_0_5 + age_5_17 + age_18_greater`

#### Total Demographic Updates

`demo_age_5_17 + demo_age_17_`

#### Total Biometric Updates

`bio_age_5_17 + bio_age_17_`

#### Update-to-Enrolment Ratio

This measures update activity compared with new enrolment activity.

#### Child Share

This represents the fraction of enrolments belonging to children aged 0–17.

#### Time-Based Features

The following features were extracted from the date:

* Year
* Month
* Weekday
* Weekend indicator

#### Rolling 7-Day Average

A 7-day rolling average of enrolment was created to smooth daily fluctuations.

#### District Z-Score

A district-level z-score was created to identify unusually high or low enrolment activity.

The final feature-engineered dataset was saved as:

`uidai_features.csv`

---

## 📊 Exploratory Data Analysis

The project performs both **Univariate and Bivariate Analysis**.

### Key Analyses

* Top states by total Aadhaar enrolment
* Busiest districts
* States with high update-to-enrolment ratios
* Growth vs Maintenance activity
* 5–17 demographic vs biometric updates
* Monthly enrolment and biometric trends
* District-level anomaly detection

---

## 🔍 Key Insights

### State-wise Enrolment

* Uttar Pradesh has the highest enrolment among the analyzed states.
* Madhya Pradesh ranks second.
* Rajasthan and Maharashtra also show high enrolment activity.

### Update Activity

* Dadra and Nagar Haveli has the highest update-to-enrolment ratio.
* Chhattisgarh also shows a high update ratio.
* Maharashtra and Bihar show strong update activity compared with enrolment.

### Growth vs Maintenance

The analysis shows a positive relationship between enrolment and update activity.

Regions with higher enrolment activity generally also show higher update activity, indicating different levels of Growth and Maintenance activity across states.

### 5–17 Age Group

Biometric updates are significantly higher than demographic updates across the top analyzed states.

Uttar Pradesh shows the highest biometric update activity, followed by states such as Maharashtra and Rajasthan.

### Monthly Trend

* Biometric updates remain higher than enrolment during the analyzed period.
* Activity decreases from April to June.
* Activity increases sharply from July onwards.
* September shows particularly high activity.

### Anomaly Detection

District-level z-scores were used to identify unusual activity.

Some districts such as **Pune, Nashik, Aurangabad, Kancheepuram, Ajmer and Nagpur** show significant unusual activity and may require further investigation.

---

## 📈 Visualizations

The project includes visualizations such as:

1. Top 10 States by Enrolment
2. States with Highest Update Ratio
3. Growth vs Maintenance Scatter Plot
4. 5–17 Age Group Updates
5. Monthly Enrolment vs Biometric Updates
6. Top Anomaly Districts

---

## 📁 Project Structure

```text
aadhaar-growth-maintenance-analysis/
│
├── Aadhar_Lenc_Data_Cleaning.ipynb
├── Feature_Engineering.ipynb
├── Data_Visualization.ipynb
│
├── uidai_cleaned_simple.csv
├── uidai_features.csv
│
├── top_states.png
├── update_ratio.png
│
└── README.md
```

---

## 💡 Business Use Case

This analysis can help identify areas where:

* New Aadhaar enrolment demand is high
* Aadhaar update activity is high
* Child biometric updates require attention
* Unusual district-level activity needs investigation
* Enrolment camps can be planned
* Biometric-update campaigns can be targeted

---

## 🚀 Future Scope

* Build a machine learning model to automatically classify regions into Growth and Maintenance phases.
* Create an interactive dashboard using Power BI or Tableau.
* Add district-level geographic visualization using maps.
* Develop predictive models for future Aadhaar update demand.
* Analyze seasonal patterns in greater detail.

---

## 👨‍💻 Project Skills Demonstrated

* Data Cleaning
* Data Preprocessing
* Exploratory Data Analysis
* Feature Engineering
* Statistical Analysis
* Data Visualization
* Python Programming
* Pandas & NumPy
* Matplotlib & Seaborn
* Business Insight Generation

---

## 📌 Conclusion

This project provides a data-driven view of Aadhaar enrolment and update activity across different regions.

By comparing **new enrolments, demographic updates, biometric updates, age-group activity and district-level anomalies**, the analysis helps understand whether regions show stronger Growth or Maintenance characteristics and where Aadhaar-related activities may need greater attention.

# 📊 HR People Analytics: Strategic Workforce Insights Dashboard

## 📝 Project Overview
This project transforms raw HR data into a strategic decision-making tool. Unlike standard descriptive reports that just show headcount, this dashboard utilizes **Predictive Analytics** to identify high-value talent at risk, evaluate recruitment ROI by source, and audit internal pay equity.

The analysis covers a workforce of **311 employees** with a focus on moving from "What happened?" to "Why is it happening and who is at risk?"

---

## 🔍 Deep-Dive Insights & Analysis ("The Real Analysis")

### 1. Recruitment ROI & Retention Paradox
* **The Finding:** A massive disparity exists in candidate quality by source. **Website hires** boast a **92.3% retention rate**, whereas **Google Search** hires plummeted to **38.8%** (only 30 active out of 49 hires).
* **Strategic Insight:** The organization is likely attracting "passive" candidates through search ads who lack long-term alignment.
* **Recommendation:** Reallocate recruitment budget away from broad search engines toward optimizing the internal Career Portal to improve long-term stability.

### 2. The "Missing Generation" Risk (Age Anomaly)
* **The Finding:** While the average age is 46, the distribution reveals a critical gap. The workforce is heavily weighted toward the **35-44 bracket (150 employees)**, with a staggering drop-off in the **25-34 bracket (only 5 employees)**.
* **Strategic Insight:** This demographic "cliff" signals a broken entry-level pipeline and a future leadership vacuum.
* **Recommendation:** Implement a Graduate or Junior Associate program immediately to ensure institutional knowledge transfer.

### 3. Predictive "Silent Leaver" Identification
* **The Finding:** Cross-referencing performance with satisfaction scores flagged **11 "perfect score" (4/4) performers** who reported low job satisfaction (3/4).
* **Strategic Insight:** These are the most valuable assets. Their dissatisfaction is correlated with identified compensation gaps compared to departmental averages.
* **Action:** Created a "Flight Risk" panel to flag these specific individuals for immediate retention conversations.

### 4. Pay Equity & Diversity Audit
* **The Finding:** Identified a **$3,000 annual salary gap** between Male ($70.8K) and Female ($67.8K) employees.
* **Diversity Lens:** Mapped racial demographics (187 White, 80 Black, 29 Asian) against salary bands to ensure objective, data-driven compensation adjustments.

---

## 🛠️ Technical Implementation

### Data Architecture & ETL
* **Schema:** Implemented a **Star Schema** with a centralized `Fact_Employees` table linked to dimensions for `Recruitment`, `Performance`, and `Geography`.
* **Power Query:** Normalized messy termination reasons into categorized buckets and created custom "Age Bins" for demographic grouping.

### Advanced DAX Logic
* **Retention %:** Developed dynamic measures to track tenure cohorts over time.
* **Flight Risk Flag:** Used nested logic to automatically flag high-performers with low satisfaction and below-average salary.
* **Gender Pay Gap:** Utilized `AVERAGEX` to iterate across filtered tables to ensure the gap analysis was departmentalized.

---

## 📈 Key Performance Indicators (KPIs)
* **Total Employees:** 311 (209 Active)
* **Average Age:** 46
* **Production Department:** 67% of total headcount (208 staff)
* **Primary Exit Driver:** "Another position" (20 exits) followed by "Unhappy" (14)

---

## 🖼️ Dashboard Preview

### Workforce Overview
![Workforce Overview](pic%201.PNG)

### Retention & Risk Analysis
![Retention & Risk Analysis](pic%202.PNG)

---

## 🧰 Tools Used
* **Power BI Desktop** (Visualization & Modeling)
* **DAX** (Advanced Analytics)
* **Power Query** (ETL & Data Cleaning)
* **Dataset:** `HRDataset_v14.xlsx`

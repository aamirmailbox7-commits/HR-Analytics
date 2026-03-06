HR Analytics Dashboard - Technical Report
Overview
Tool Stack: Power BI, DAX, Data Modeling
Dataset: 311 employees, 209 active, 6 departments, 50 states
Focus: Predictive retention analytics beyond standard HR reporting
Key Findings
Finding 1: Retention-Source Paradox
Website hires: 92.3% retention (13 hired, 1 exit)
Google Search hires: 38.8% retention (49 hired, 30 exits)
Gap: 53.5 percentage points between best and worst channels
Insight: Volume-based hiring through low-retention channels drives preventable turnover
Finding 2: High Performer Flight Risk
11 employees with perfect performance scores (4/4) flagged
Common thread: Below-average compensation, satisfaction scores at 3/4 or 3/5
Risk: 63.6% show dissatisfaction despite peak performance
Top exit drivers support this: "more money" (11), "unhappy" (14), "another position" (20)
Workforce Demographics (Page 1)
Total: 311 | Active: 209 | Avg Age: 46
Age skew: 48.2% in 35-44 bracket, only 1.6% in 25-34
Gender: 56% male ($70.8K avg), 44% female ($67.8K avg) — $3K gap
Department: Production dominates at 66.9% (208 employees)
Race: 60.1% White, 25.7% Black/African American, 9.3% Asian
Retention Analytics (Page 2)
Hiring Source Rankings by Retention:
Website 92.3% | Employee Referral 80.6% | LinkedIn 76.3% | Indeed 75.9% | CareerBuilder 52.2% | Other 50.0% | Diversity Job Fair 44.8% | Google Search 38.8%
Termination Root Causes (102 total exits):
Top 3 voluntary: Another position (20), unhappy (14), more money (11) = 44.1% of all turnover, all addressable
Technical Implementation
DAX Logic:
Retention Rate = DIVIDE(Active, Hired, 0)
Flight Risk = IF(Performance=4 AND Satisfaction<=3 AND Salary<BandAvg, "Critical", "Stable")
Visualizations: KPI cards, distribution bars, donut charts, performance matrix, geo-map, executive alert panel
Recommended Actions
Immediate: Compensation audit for 11 flagged high performers; shift 30% budget from Google Search to Website/Referral channels
30-90 days: Deploy predictive flight risk scoring; set channel retention minimums
90+ days: Reduce turnover from 32.8% to <20%; eliminate compensation-driven exits for top talent
Data Quality
Complete active employee records; all exits coded with reason. Cross-sectional snapshot—trend analysis requires time-series expansion.

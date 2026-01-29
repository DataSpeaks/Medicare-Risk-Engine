🏥 Medicare Risk Engine: Proactive Improper Payment Mitigation
📌 Executive Summary
Medicare improper payments cost billions annually, yet most organizations manage them reactively. This project utilizes the 2024 CMS CERT dataset (116k claims) to build a Weighted Risk Scoring Engine that flags high-probability errors before submission.

The Impact:

Precision: Identified a "Red Tier" with a 34.2% actual error rate (2.1x the baseline).

Efficiency: Focuses 100% of audit resources on just 1.6% of total volume.

Root Cause: Proved that Insufficient Documentation in specific provider types (Nephrology, Physical Medicine) is the primary driver of preventable risk.

🔬 Research Questions
The Integrity Gap: Does missing billing data ("Unknown" types) correlate with higher audit disagreement rates?

Complexity vs. Risk: How do clinical specialties like DME (Durable Medical Equipment) compare to standard inpatient hospital services?

The Audit Solution: Can we statistically isolate the 1% of claims causing the most financial risk?

⚙️ How the Risk Engine Works
The engine calculates a final_risk_score using three weighted pillars:

Identity Score (50%): Weighted based on historical Provider Type error rates.

Integrity Score (25%): A "Transparency Penalty" for claims missing critical billing structure data.

Complexity Score (25%): Prioritizes high-risk categories like DME and Part B services.

Claims are then stratified into three actionable tiers: Green (Low Risk), Yellow (Standard), and Red (Hard Stop).

📊 Key Visualizations<img width="908" height="577" alt="Screenshot 2026-01-28 175506" src="https://github.com/user-attachments/assets/799df4c1-40c4-423c-97ee-44ad1453b325" />
<img width="545" height="671" alt="Screenshot 2026-01-28 175543" src="https://github.com/user-attachments/assets/8ce538fc-ebef-4bfb-86d8-ecbfe2a48e08" />
<img width="816" height="561" alt="Screenshot 2026-01-28 175613" src="https://github.com/user-attachments/assets/527427c6-b0d6-4426-8510-b5fcdca314be" />


🛠️ Tech Stack & Resources
Language: Python 3.x

Libraries: Pandas (Data Manipulation), Seaborn/Matplotlib (Visualization), NumPy

Data Source: CMS 2024 CERT Public Use File

Environment: Jupyter Notebook / Anaconda

🚀 Future Roadmap
ML Integration: Transition from weighted scoring to XGBoost for non-linear risk capture.

Feature Engineering: Integrate NPI (National Provider Identifier) data for deeper provider-level behavioral analysis.

API Deployment: Wrap the engine in FastAPI to allow real-time "Risk Checks" at the point of claim entry.

📫 Contact & Portfolio
Name: Latavia Brown

LinkedIn: (https://www.linkedin.com/in/latavia-brown-57864a235/#:~:text=www.linkedin.com/in/latavia%2Dbrown%2Ddataanalyst)

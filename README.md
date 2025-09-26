# Cloud Cost Anomaly Detection & Forecasting Using Data Analytics

## Project Overview
This project simulates a real-world IT analytics problem:  
- Detecting **anomalies** in cloud spend (unexpected spikes, inefficiencies).  
- Forecasting **future cloud costs** for both short-term (30 days) and long-term (6 months).  
- Delivering insights via an **interactive Power BI dashboard**.

## Business Problem
Cloud costs are unpredictable and can quickly exceed budgets.  
The solution provides:
- **Anomaly detection** → early alerts on unusual spend.  
- **Forecasting** → budget planning and capacity management.  
- **Dashboarding** → actionable insights for IT managers and finance teams.

## Approach (PACE Framework)
1. **Plan** → Define business problem, objectives, dataset.  
2. **Analyze** → Clean messy data, EDA, anomaly exploration.  
3. **Construct** → Build anomaly detection models (Z-score, Isolation Forest) and forecasting (Prophet).  
4. **Execute** → Deploy insights in a Power BI dashboard.

## Dataset
- Synthetic dataset (~1M rows, 12 months).  
- Fields: timestamp, service_tag, team, region, usage, cost_usd, currency, etc.  
- Includes anomalies, missing values, duplicates for realism.  

## Tech Stack
- **Python (Jupyter Notebooks)** → pandas, numpy, matplotlib, seaborn, scikit-learn, Prophet.  
- **Power BI** → Interactive dashboards.  
- **Joblib** → Model saving & reuse.

## Key Results
- Anomaly detection model: Precision ~44%, Recall ~87% (best trade-off).  
- Forecasts: Stable overall costs, seasonal peaks (May–July), dips (Sept–Nov).  
- Service-level forecasts: RDS & ELB volatile, S3 & Lambda stable.

## Deliverables
- [x] Cleaned dataset  
- [x] Anomaly detection notebooks  
- [x] Forecasting notebooks  
- [x] Saved ML model (`isolation_forest_final.joblib`)  
- [x] Forecast & anomaly CSVs  
- [x] Power BI dashboard file (`Cloud_Cost_Analytics.pbix`)  

## Dashboard Features
- **Executive Overview** → KPIs, global spend trends.  
- **Anomaly Insights** → anomalies by service/team.  
- **Forecasting Insights** → global + service-level forecasts.  
- **Team & Region Insights** → drill-down by team/region.

## How to Run
1. Clone this repo.  
2. Install dependencies: `pip install -r requirements.txt`
3. Access raw & cleaned files from [Google drive](https://drive.google.com/drive/folders/1gEp19NKV4JgQNqxtNcI_CK2HteuaY24I?usp=drive_link)
   - Raw Files(`cloud_usage_data.csv` ➡ `cloud_usage_datafile.parquet`)
   - Cleaned File (`clean_cloud_date.parquet`)
5. Run Jupyter notebooks in order:  
   - `1_DataCleaning.ipynb`  
   - `2_ExploratoryDataAnalysis.ipynb`  
   - `3_AnomalyDetection.ipynb`  
   - `4_ForecastingCloudCosts.ipynb`  
6. Open `Cloud_Cost_Analytics.pbix` in Power BI for dashboards.

## Recommendations
- Use anomaly alerts to monitor RDS/ELB spikes.  
- Plan budgets around seasonal patterns & month-end effects.  
- Optimize weekend/month-end jobs for cost savings.  
- Adopt cloud FinOps practices for continuous monitoring.

## Contact
Created by Shijin Ramesh
[LinkedIn](https://www.linkedin.com/in/shijinramesh/) | [Portfolio](https://www.shijinramesh.co.in/)

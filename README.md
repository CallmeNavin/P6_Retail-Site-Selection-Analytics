# Retail Site Selection Analytics

**VERSION 1 - DESCRIPTIVE ANALYSIS**

**A. Project Overview**

- This project analyzes the sales, rent, profit, occupancy rate and other ratio for an convenience storechain using Python Power BI.
- The focus is on identifying operational gaps, uncovering opportunities for optimization and providing insights for future guidelines.
- For this project, the company strategy is prioritize development in adjacent or secondary cities to diversify beyond the saturated major hubs.

![Dashboard Overview](https://github.com/CallmeNavin/P6_Retail-Site-Selection-Analytics/blob/main/Version%201/Visualization/Overview.png)
_Explore more insights in the full Power BI dashboard_

**B. Dataset Information**

**Source**

- Synthetic dataset created for educational and portfolio purposes.
- The data structure and variables are designed to mirror real-world commercial leasing datasets in the retail sector in Vietnam.
- Geolocation coordinates are pre-generated within realistic city boundaries.

**Period**

- Lease start date in the range from 2019 - 2025, allowing analysis of both current and historical leasing performances as well as forecasting future result.

**C. Methodoly**

Data cleaning → descriptive analysis → segmentation & KPI metrics → actionable insights.

**D. Key Findings and Actionable Plans**

**I. Overview**

- Strong Revenue vs Rent: Monthly Average Rent is 92.8M VND, while Monthly Average Sales reach 750.64M VND → Profit margin before other expenses: 657.84M VND → strong performance overall.
- Adequate Store Size: Average Store Area is 87.53 m² → suitable for convenience store operations.
- 2 specific stores (Active/Potential) show extremely high ratios of 65.56% and 79.73% → high-risk locations. If other operating costs are considered, these stores have a high potential for deficit.
- Healthy Average Rent-to-Sales Ratio: Overall ratio is 15.24%, exceed the industry benchmark (≤ 15%) → There is 01 case (Store S0123) which has too-high Rent-to-Sales Ratio (126.79%), influenced the overall Average Rent-to-Sales ratio → Flagged for Closure
- Low Occupancy Rate: Average Occupancy Rate is 64.27% → Optimize immediately by creating decision matrix to identify site for expansion and store optimization.

**II. Findings by Business Theme**

**1. Site Expansion**

_**Key Findings**_

- Current Footprint: The chain currently operates in 5 key cities: Hanoi, Hai Phong, Da Nang, Ho Chi Minh City (HCMC), and Can Tho.
- Cost efficiency (Rent-to-Sales Ratio): Lowest in Can Tho (6.95%), Hai Phong (7.72%), and Da Nang (10.04%).
- Competition (Competitor Count): Fewest competitors in Can Tho (5.27%), Hai Phong (6.22%), and Da Nang (7.8%).
- Demand (Foot Traffic per Day): Lowest traffic in Can Tho (5.47%), Hai Phong (6.26%), and Da Nang (8.47%).
- Financial Performance Simulation:
  + Assumed Operating Expense = 20% of Monthly Sales (industry-safe benchmark).
  + Net Profit = Monthly Sales – Rent – Operating Expense.
  + ROI = Net Profit ÷ Rent.
  + Results:
    Highest profit (absolute): HCMC & Hanoi.
    Highest efficiency (ROI): Da Nang (854.07%), Can Tho (818.71%), Hai Phong (645.74%) – ~1.5x higher than HCMC & Hanoi.

_**Actionable Plans**_

- Trade-off identified:
  + Big cities (HCMC & Hanoi) → Higher profit volume, but lower ROI (efficiency).
  + Smaller cities (Da Nang, Can Tho, Hai Phong) → Lower absolute profit, but much higher ROI, making capital deployment more efficient.
  + Using the Site Expansion Decision Matrix and Priority Level (for more details: "Appendix" section): Da Nang emerges as both “Pilot” and “Strong” candidate.
  + Decision: Prioritize Da Nang for the next expansion.

**2. Current Store Optimization**

_**Key Findings**_

- ~85% of stores need restructuring (Optimize/Close). The two stores initially flagged with abnormally high rent-to-sales ratios (65.56% and 79.73%) were later included in the optimization/removal list.

**_Actionable Plans_**

- Close: Exit 127 stores to cut costs.
- Optimize: Improve 94 stores via cost control, rent renegotiation, and CX upgrades.
- Keep: Protect 38 top stores.

**III. Roadmap & Guidelines** 

Based on Decision List in Current Store Optimization section,
- Short-term: Consider to close weak stores.
  + For stores in close list: Store managers report local issues → attempt lease renegotiation → if no improvement → proceed with closure.
- Long-term: Optimize current store & consider to open new store in DaNang province.
  + Optimize Current Store: Ops team assess causes (traffic, SKU, staffing) → apply targeted fixes (SKU mix, layout, training, campaigns).
  + Expand to DaNang province: Validate shortlisted sites with local manager input → pilot 2–3 sites with rent & sales projection before rollout.

**E. Appendix**

**1. Site Expansion Decision Matrix**

_This framework evaluates potential cities for new store openings by combining ROI (Return on Investment), Market Size (Foot Traffic), and Strategic Fit._

_**1.1. Segmentation**_

**_ROI (Return on Investment)_**

Absolute cut-off:
- ROI < 100% → Not considered (below minimum hurdle).
- ROI ≥ 100% → Eligible for benchmarking.
Based on dataset min–max after cut-off:
- Low ROI: min – 1/3 range
- Medium ROI: 1/3 – 2/3 range
- High ROI: 2/3 – max

_**Market Size (Foot Traffic)**_

Based on dataset min–max:
- Low: min – 1/3 range
- Medium: 1/3 – 2/3 range
- High: 2/3 – max

(Thresholds automatically adapt to the dataset, ensuring fair comparison between cities.)

_**1.2. Site Expansion Decision Matrix**_

**_Step 1: ROI × Market Size Matrix_**

| ROI ↓ \ Market → | Low Market Size | Medium Market Size    | High Market Size |
| ---------------- | --------------- | --------------------- | ---------------- |
| **Low ROI**      | Reject (RE)     | Reject (RE)           | Reject (RE)      |
| **Medium ROI**   | Reject (RE)     | Secondary Option (SE)  | Pilot (P)        |
| **High ROI**     | Risky (RI)      | Strong (S) | Top (T) |

Priority Levels (Descending): Top (T) - Strong (S) - Pilot (P) - Secondary Option (SE) - Risky (RI) - Reject (RE)

_**Step 2: Strategic Fit Adjustment**_

After positioning a city in the ROI × Market Size matrix, apply Strategic Fit:
- High Fit: Keep.
- Medium Fit: Downgrade by 1 Priority level.
- Low Fit: Reject.

**2. Current Store Optimization Decision Matrix**

_**2.1. Segmentation**_

**_ROI (Return on Investment)_**

Absolute cut-off:
- ROI < 100% → Not considered (below minimum hurdle).
- ROI ≥ 100% → Eligible for benchmarking.
Based on dataset min–max after cut-off:
- Low ROI: min – 1/3 range
- Medium ROI: 1/3 – 2/3 range
- High ROI: 2/3 – max

**_Rent to Sales Ratio (RTSr)_**

Based on dataset min–max:
- Low RTSr: min – 1/3 range
- Medium RTSr: 1/3 – 2/3 range
- High RTSr: 2/3 – max

**_Lease Date (Lease_End - Lease_Start)_**

Based on dataset min–max:
- Short: min – 1/3 range
- Medium: 1/3 – 2/3 range
- Long: 2/3 – max

_**2.2. Current Store Optimization Decision Matrix**_

**_Step 1: ROI × Rent to Sales ratio (RTSr) Matrix_**

| ROI ↓ \ RTSr → | Low RTSs | Medium RTSs    | High RTSs |
| ---------------- | --------------- | --------------------- | ---------------- |
| **Low ROI**      | Close (C)     | Close (C)           | Close (C)      |
| **Medium ROI**   | Optimization (O)     | Optimization (O)  | Close (C)        |
| **High ROI**     | Keep (K)      | Optimization (O) | Close (C) |

Priority Levels (Descending): Keep (K) - Optimization (O) - Close (C)

_**Step 2: Lease Date Adjustment**_

After positioning a store in the ROI × RTSr, apply Lease Date:
- Short: Downgrade by 1 Priority level.
- Medium: Keep.
- Long: Upgrade by 1 Priority level.

**VERSION 2 - PREDICTIVE ANALYSIS**

**A. Project Overview**

- This version predict the ROI ratio of active/potential stores using machine learning models (Linear Regression, Random Forest, and XGBoost).

**B. Methodoly**

- I. Data Preparation:
  + I.1. Remove rows which have status "Closed"
  + I.2. Add columns "Total_Sales_mVND" = Sales_per_sqm_mVND * Area_sqm
  + I.3. Add columns "ROI" = (Total_Sales_mVND - 20% * Total_Sales_mVND) / Monthly_Rent_mVND
- II. Predictive Analysis:
  + II.1. One-hot encoding for Column "City"
  + II.2. Define & Split x & y:
    - y: Column "ROI"
    - x: Columns "City", "Foot_Traffic_per_day", "Competitor_Count_500m", "Occupancy_Rate"
  + II.3. Train/Test Split
  + II.4. StandardScaler for input numeric columns
  + II.5. Modeling
    - II.5.1. Linear Regression + Coeffient
    - II.5.2. Random Forest Regressor + Feature Importances
    - II.5.3. XGB Regressor
  + II.6. Feature Engineering:
    + II.6.1. Add Column "Traffic_per_sqm" = Foot_Traffic_per_day / Area_sqm
    + II.6.2. Add Column "Rent_per_sqm" = Monthly_Rent_mVND / Area_sqm
    + II.6.3. Add Column "Lease_Term" = Lease_End - Lease_Start
    + II.6.4. Split x & y
    + II.6.5. Train/Test Split
    + II.6.6. StandardScaler for input numeric columns
    + II.6.7. Remodeling

**C. Key Findings and Actionable Plans**

**_Key Findings_**

- Before FE: R² only ranged from 0.14 to 0.39 → models explained ROI very poorly. Initial raw inputs lacked predictive power. After FE: R² jumped to 0.82–0.88 (peaking with Random Forest), while MAE and RMSE dropped significantly.
→ Feature Engineering fundamentally improved accuracy. Newly engineered variables (Traffic_per_sqm, Rent_per_sqm, Lease_Term) captured the economic essence of ROI far better than raw features.
- Foot_Traffic_per_day (+2.3): Higher traffic consistently drives ROI up → busy stores generate stronger returns. Rent_per_sqm (–2.7): Higher rent per m² consistently drags ROI down → expensive leases erode profitability.
→ High traffic = ROI ↑. High rent per sqm = ROI ↓.
- Rent_per_sqm (52%) + Foot_Traffic (34%) together account for 86% of ROI variance → the two core pillars of ROI performance. City dummies lost significance after FE. Before FE, ROI seemed heavily city-driven.
→ ROI is not determined by which city but by the balance between traffic density and rent efficiency at the site level.

**_Actionable Plans_**

- Prioritize sites with strong foot traffic and reasonable rent per m², regardless of whether they are in HCMC/Hanoi or secondary cities.
- Focus site selection decisions on economic efficiency metrics (traffic vs. rent) rather than purely geographical expansion.

**D. Appendix**

_**I. Modeling Metrics Result**_

| Metric | Linear Regression (Before FE) | Random Forest (Before FE) | XGBoost (Before FE) | Linear Regression (After FE) | Random Forest (After FE) | XGBoost (After FE) |
| ------ | ----------------------------- | ------------------------- | ------------------- | ---------------------------- | ------------------------ | ------------------ |
| MAE    | 1.929                         | 2.002                     | 2.284               | 1.061                        | 0.897                    | 0.853              |
| RMSE   | 2.389                         | 2.449                     | 2.836               | 1.305                        | 1.053                    | 1.107              |
| R²     | 0.392                         | 0.361                     | 0.143               | **0.819**                    | **0.882**                | **0.869**          |
| MAPE   | 0.750                         | 0.792                     | 0.640               | 0.726                        | 0.491                    | **0.388**          |

_**II. Linear Regression – Coefficients**_

| Feature                | Coefficient (Before FE) | Coefficient (After FE) |
|-------------------------|-------------------------|------------------------|
| Foot_Traffic_per_day    | +2.520                  | +2.276                 |
| Occupancy_Rate          | +0.096                  | +0.095                 |
| Competitor_Count_500m   | –0.300                  | –0.220                 |
| City_DaNang             | –1.352                  | –1.213                 |
| City_HaiPhong           | –2.587                  | –1.102                 |
| City_HCMC               | –5.402                  | +0.130                 |
| City_HaNoi              | –5.516                  | –0.774                 |
| Traffic_per_sqm         |                       | –0.062                 |
| Rent_per_sqm            |                       | –2.744                 |
| Lease_Term              |                       | –0.390                 |

_**III. Random Forest – Feature Importances**_

| Feature                | Importance (Before FE) | Importance (After FE) |
|-------------------------|------------------------|-----------------------|
| Foot_Traffic_per_day    | 0.525                  | 0.343                 |
| Competitor_Count_500m   | 0.160                  | 0.019                 |
| Occupancy_Rate          | 0.153                  | 0.023                 |
| City_DaNang             | 0.057                  | 0.002                 |
| City_HCMC               | 0.049                  | 0.002                 |
| City_HaNoi              | 0.041                  | 0.006                 |
| City_HaiPhong           | 0.015                  | 0.001                 |
| Traffic_per_sqm         |                      | 0.064                 |
| Rent_per_sqm            |                      | 0.520                 |
| Lease_Term              |                      | 0.020                 |

**VERSION 3 - DEPLOY MODEL**

**A. Project Overview**

- In this version, I used a new dataset to apply the best-performing model from Version 2.
- The goal was to simulate a real deployment scenario where the input dataset does not perfectly match the training dataset schema.

**B. Dataset Information**

**Source**

- US Stores Sales
- https://www.kaggle.com/datasets/dsfelix/us-stores-sales

**Period**

- Jan 2010 - Dec 2011

**Assumption**

Column Mapping (New Dataset → Old Dataset)
- State → City.
- ROI → Sales, Profit, Margin, Total Expenses:
  + ROI = Profit / Total Expenses.
- Date → Lease Term:
  + Lease_Term = (Reference Date – Date). Reference Date: 01/01/2025

**C. Methodoly**

- Calculate new columns or generate values (by mean) if raw data was missing.
- Drop irrelevant columns.
- Reuse the trained Scaler from Version 2.
- Load the best model from Version 2 (Random Forest Regressor).
- Predict ROI and evaluate results.
- Export predictive ROI data.

**D. Results & Findings**

**_Results_**
Deployment pipeline was successful: the Version 2 model was applied to the new dataset by aligning features, reusing the scaler, and generating ROI predictions.
- R²: -36.05  
- MAE: 8.21  
- RMSE: 8.63  


**_Findings_**
- High MAE & RMSE, with R² < 0 → the model performed worse than a naive baseline.  
- The main reasons: missing critical features (e.g., Foot Traffic, Occupancy), inconsistent Lease_Term distribution, and schema mismatch.  
→ ML models cannot be directly deployed to new datasets if feature distributions differ. Data pipelines must ensure feature consistency, and new features should trigger retraining. Without standardized data collection, ROI predictions become unreliable, leading to risky decisions.  

_**About Me**_

Hi, I'm Navin (Bao Vy) – an aspiring Data Analyst passionate about turning raw data into actionable business insights.
I’m eager to contribute to data-driven decision making and help organizations translate analytics into business impact.
For more details, please reach out at:

🌐 LinkedIn: https://www.linkedin.com/in/navin826/

📂 Portfolio: https://github.com/CallmeNavin/

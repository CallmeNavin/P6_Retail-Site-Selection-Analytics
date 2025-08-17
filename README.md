# Retail Site Selection Analytics

**A. Project Overview**

This project analyzes the sales, rent, profit, occupancy rate and other ratio for an convenience storechain using Python Power BI. The focus is on identifying operational gaps, uncovering opportunities for optimization and providing insights for future guidelines.
For this project, the company strategy is prioritize development in adjacent or secondary cities to diversify beyond the saturated major hubs.

**B. Dataset Information**

**Source**

- Synthetic dataset created for educational and portfolio purposes.
- The data structure and variables are designed to mirror real-world commercial leasing datasets in the retail sector in Vietnam.
- Geolocation coordinates are pre-generated within realistic city boundaries.

**Period**

- Lease start date in the range from 2019 - 2025, allowing analysis of both current and historical leasing performances as well as forecasting future result.

**C. Methodoly**

Data cleaning → descriptive analysis → segmentation & KPI metrics → actionable insights.

**D. Dashboard Structure, Key Findings and Actionable Insights**

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
  Assumed Operating Expense = 20% of Monthly Sales (industry-safe benchmark).
  Net Profit = Monthly Sales – Rent – Operating Expense.
  ROI = Net Profit ÷ Rent.
  Results:
  Highest profit (absolute): HCMC & Hanoi.
  Highest efficiency (ROI): Da Nang (854.07%), Can Tho (818.71%), Hai Phong (645.74%) – ~1.5x higher than HCMC & Hanoi.

_**Actionable Insights**_

- Trade-off identified:
  Big cities (HCMC & Hanoi) → Higher profit volume, but lower ROI (efficiency).
  Smaller cities (Da Nang, Can Tho, Hai Phong) → Lower absolute profit, but much higher ROI, making capital deployment more efficient.
- Using the Site Expansion Decision Matrix and Priority Level (for more details: "Appendix" section): Da Nang emerges as both “Pilot” and “Strong” candidate.
- Decision: Prioritize Da Nang for the next expansion.

**2. Current Store Optimization**

_**Key Findings**_

- ~85% of stores need restructuring (Optimize/Close). The two stores initially flagged with abnormally high rent-to-sales ratios (65.56% and 79.73%) were later included in the optimization/removal list.

**_Actionable Insights_**

- Close: Exit 127 stores to cut costs.
- Optimize: Improve 94 stores via cost control, rent renegotiation, and CX upgrades.
- Keep: Protect 38 top stores.

**III. Roadmap & Guidelines** 

Based on Decision List in Current Store Optimization section,
- Short-term: Consider to close weak stores.
  For stores in close list: Store managers report local issues → attempt lease renegotiation → if no improvement → proceed with closure.
- Long-term: Optimize current store & consider to open new store in DaNang province.
  Optimize Current Store: Ops team assess causes (traffic, SKU, staffing) → apply targeted fixes (SKU mix, layout, training, campaigns).
  Expand to DaNang province: Validate shortlisted sites with local manager input → pilot 2–3 sites with rent & sales projection before rollout.

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

_**F. About Me**_

Hi, I'm Navin (Bao Vy) – an aspiring Data Analyst passionate about turning raw data into actionable business insights. 
For more details, please reach out at:

🌐 LinkedIn: https://www.linkedin.com/in/navin826/

📂 Portfolio: https://github.com/CallmeNavin/

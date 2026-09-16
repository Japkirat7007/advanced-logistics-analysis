# Advanced Logistics Data Analysis and Visualization

## Logistics Data Analyst Internship Project — Yuva Intern

This repository contains my Advanced Data Analysis and Visualization in Logistics project completed as part of the Logistics Data Analyst Internship at Yuva Intern.

The project demonstrates how Python-based exploratory data analysis, statistical analysis, KPI measurement, and data visualization can be used to evaluate logistics performance and convert shipment-level data into meaningful operational insights.

The analysis is based on a hypothetical logistics dataset containing **1,500 simulated shipments and 13 variables** covering delivery performance, transportation cost, shipment volume, warehouse processing, delays, transport modes, regional performance, monthly shipment activity, and customer ratings.

---

## Project Objectives

The main objectives of this project are to:

- Simulate a structured logistics dataset suitable for advanced analysis.
- Perform exploratory data analysis (EDA) using descriptive statistics and logistics KPIs.
- Analyze delivery-time and transportation-cost distributions.
- Investigate potential transportation cost drivers.
- Compare the performance of different transportation modes.
- Examine warehouse processing as a possible operational bottleneck.
- Analyze shipment delays and delivery reliability.
- Explore the relationship between shipment delay and customer rating.
- Evaluate monthly shipment activity and regional performance.
- Create meaningful visualizations using Python.
- Translate analytical findings into practical logistics recommendations.
- Clearly document the feasibility and limitations of the analysis.

---

## Dataset Overview

The hypothetical dataset contains **1,500 shipment records** covering the period from January 2025 to December 2025.

The dataset contains the following variables:

- Shipment_ID
- Shipment_Date
- Region
- Transport_Mode
- Distance_km
- Shipment_Volume_kg
- Priority
- Warehouse_Processing_Hours
- Delivery_Time_Hours
- Transportation_Cost
- Delay_Hours
- On_Time_Delivery
- Customer_Rating

### Data Quality Validation

Before performing the analysis, the dataset was validated for completeness and consistency.

- Total records: **1,500**
- Total variables: **13**
- Missing values: **0**
- Duplicate rows: **0**
- Duplicate Shipment IDs: **0**

---

## Key Logistics KPIs

| KPI | Result |
|---|---:|
| Total Shipments | 1,500 |
| Average Delivery Time | 30.11 hours |
| Median Delivery Time | 26.16 hours |
| Average Transportation Cost | 1,346.28 |
| Average Delay | 4.44 hours |
| On-Time Delivery Rate | 69.07% |
| Average Warehouse Processing Time | 3.97 hours |
| Average Customer Rating | 4.24 / 5 |

For this simulated project, a shipment with a delay of **5 hours or less** is classified as on time. This threshold is a project-specific analytical rule and is not presented as a universal logistics-industry standard.

---

## Exploratory Data Analysis

The EDA examines central tendencies, variability, distributions, relationships, and operational performance across the logistics dataset.

Major areas analyzed include:

- Delivery time distribution
- Transportation cost distribution
- Shipment distance and transportation cost
- Shipment volume and transportation cost
- Transportation mode performance
- Warehouse processing and shipment delay
- Shipment delay and customer rating
- Correlations among logistics variables
- On-time delivery performance
- Monthly shipment activity
- Regional logistics performance

---

## Key Analytical Findings

### Delivery Performance

The average delivery time is **30.11 hours**, while the median is **26.16 hours**. The higher mean indicates a positively skewed delivery-time distribution, with a smaller number of long-duration shipments increasing the average.

The maximum simulated delivery time is approximately **95.39 hours**.

### Transportation Cost

Average transportation cost is **1,346.28**, compared with a median of approximately **1,144.08**.

The distribution is positively skewed, indicating that a smaller number of high-cost shipments raise the overall average.

### Distance as a Cost Driver

Shipment distance and transportation cost have a Pearson correlation of:

**r = 0.600**

This represents a moderate positive linear association, suggesting that longer simulated shipment distances tend to be associated with higher transportation costs.

### Shipment Volume and Cost

Shipment volume and transportation cost have a correlation of:

**r = 0.071**

This is a very weak positive linear relationship. Therefore, shipment weight alone provides little explanation for transportation-cost variation in this simulated dataset.

### Warehouse Processing and Delay

Warehouse processing time and shipment delay have a correlation of:

**r = 0.221**

This weak positive association indicates that warehouse processing may contribute to delays, but it is not the only simulated operational factor affecting shipment performance.

### Delivery Reliability

Out of 1,500 simulated shipments:

- **1,036 shipments were classified as on time**
- **464 shipments were classified as delayed**
- **On-time delivery rate: 69.07%**
- **Delayed shipment rate: 30.93%**

### Customer Rating and Delay

Shipment delay and customer rating have a strong negative simulated relationship:

**r = -0.847**

This relationship was intentionally incorporated into the simulation design, where increasing delay reduces the expected customer rating. Therefore, it should not be interpreted as an independently discovered causal relationship.

---

## Transportation Mode Analysis

The project compares Air, Rail, Road, and Sea transportation.

| Mode | Avg. Cost | Avg. Delivery Time | On-Time Rate |
|---|---:|---:|---:|
| Air | 2,613.68 | 10.07 hours | 70.32% |
| Rail | 898.76 | 28.96 hours | 68.73% |
| Road | 1,162.53 | 33.86 hours | 67.88% |
| Sea | 749.92 | 48.26 hours | 71.24% |

The results demonstrate a clear simulated **cost-service trade-off**.

Air provides the shortest average delivery time but has the highest average transportation cost. Sea has the lowest average cost but the longest average delivery duration.

Therefore, no transportation mode is treated as universally superior. Mode selection should depend on service requirements, urgency, cost constraints, and operational priorities.

---

## Regional Performance Analysis

Regional analysis identified differences in simulated logistics performance.

- **North** handled the largest shipment volume with 409 shipments and recorded the highest on-time rate at **72.37%**.
- **East** recorded the lowest on-time rate at **65.62%** and the highest average delay at approximately **4.58 hours**.
- **West** recorded the highest average delivery time and average transportation cost.

Because the regions are part of a hypothetical simulation, these differences are treated as analytical signals for further investigation rather than evidence of geographic causation.

---

## Monthly Shipment Analysis

Monthly shipment activity varies throughout the simulated year.

- Highest shipment volume: **August — 142 shipments**
- Lowest shipment volume: **March — 98 shipments**
- Difference: **44 shipments**

The monthly pattern does not demonstrate a consistent increasing or decreasing trend.

Since shipment dates are simulated, the observed monthly variation is not presented as evidence of real seasonality.

---

## Visualizations

The project contains 10 visualization outputs:

1. Delivery Time Distribution
2. Transportation Cost Distribution
3. Transportation Cost vs Shipment Distance
4. Transportation Cost vs Shipment Volume
5. Average Transportation Cost by Transport Mode
6. Warehouse Processing Time vs Shipment Delay
7. Shipment Delay vs Customer Rating
8. Logistics Correlation Matrix
9. On-Time vs Delayed Shipments
10. Monthly Shipment Volume

All visualization files are available in the **Charts** folder.

Different visualization types were selected according to the analytical purpose:

- **Histograms** — distribution, spread, skewness, and long-tail analysis
- **Scatter plots** — relationships between quantitative logistics variables
- **Bar charts** — categorical performance comparisons
- **Correlation heatmap** — comparison of multiple pairwise relationships
- **Line chart** — month-to-month shipment activity

---

## Actionable Recommendations

Based on the simulated analytical findings, the project recommends:

1. Strengthening shipment delay and exception monitoring.
2. Monitoring warehouse processing time while investigating additional delay sources.
3. Selecting transportation modes according to cost and service requirements rather than using a single mode universally.
4. Including shipment distance in transportation cost planning.
5. Avoiding the use of shipment weight as the sole basis for cost estimation.
6. Monitoring severe delays and validating their relationship with customer satisfaction using real operational data.
7. Tracking monthly shipment workload to support capacity and resource planning.
8. Investigating regional performance differences through transport-mode mix, distance, processing time, and delay-source analysis.

---

## Tools and Technologies

- Python
- Google Colab
- pandas
- NumPy
- Matplotlib
- GitHub
- Microsoft Word

---

## Repository Structure

```text
advanced-logistics-analysis/
│
├── Charts/
│   ├── README.md
│   └── 10 visualization PNG files
│
├── Task_3_Hypothetical_Logistics_Dataset.csv
├── Yuva_Intern_Task_3_Advanced_Logistics_Analysis.ipynb
├── Task_3_Advanced_Logistics_Analysis_Report.docx
└── README.md

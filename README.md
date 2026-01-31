# Project Background
This project simulates a real-world analytics engagement for a motor insurance company operating in the personal and commercial auto insurance space. The company underwrites vehicle insurance policies across multiple regions and customer segments, with revenue driven by policy premiums and profitability heavily influenced by claim frequency and claim severity.

As a Data Analyst working within the insurance analytics team, my objective was to consolidate fragmented policyholder and claims data into a single source of truth and enable business stakeholders—such as risk managers, underwriting teams, and senior leadership—to quickly understand:

- **Who the policyholders are**
- **Where claims are concentrated**
- **Which customer and vehicle segments drive higher risk and cost**

The DAX measures used to calculate KPIs, enable dynamic measure switching, and support interactive insights in this analysis can be found here [link]. 

The outcome is a two-page interactive Power BI dashboard designed to support data-driven decisions around pricing, risk assessment, and portfolio optimization.

### Business Objective & Key Analysis Area
Insights and recommendations are provided on the following key areas:

- **Category 1: Policyholder Demographics & Risk Profile** 
- **Category 2: Claims Behavior & Financial Impact** 
- **Category 3: Vehicle & Usage-Based Risk Analysis** 
- **Category 4: Geographic & Coverage Zone Insights** 

### Dashboard Overview
The analysis is delivered through two interactive dashboard views:
### Total Claim Amount
![1759364325633](https://github.com/user-attachments/assets/0955fb14-0d62-4d3d-bf4e-d7270629d7d9)
### Total Policies
![1759364326157](https://github.com/user-attachments/assets/50e198d9-8435-4c61-956e-f0955460c018)

All visuals are dynamically driven by two core measures:
* Total Policies
* Total Claim Amount

This design allows stakeholders to seamlessly switch between exposure analysis (policy volume) and financial risk analysis (claim value) using the same visual framework.

### Key KPIs
* Total Policies – Size of the active policyholder base
* Total Claim Amount – Overall financial exposure from claims
* Claim Frequency – How often claims occur
* Average Claim Amount – Claim severity and risk intensity
* Gender-wise Policy Distribution – Customer segmentation insights 

# Data Structure & Initial Checks
The company’s analytical dataset is structured around policyholder, vehicle, and claims attributes, enabling multi-dimensional analysis.
### Core data entities include:
* Policy information (policy count, usage type, coverage zone)
* Customer demographics (age, gender, education, marital status)
* Vehicle attributes (make, model year, usage)
* Claims data (claim amount, frequency)

_Note: This project uses a flattened analytical dataset suitable for BI reporting rather than a transactional OLTP schema._

### Initial checks included:
* Validation of null and zero claim values
* Consistency checks for categorical fields (e.g., car use, zones)
* Aggregation sanity checks for policy and claim totals

# Executive Summary

### Overview of Findings
From a risk and profitability perspective, three insights stand out:

* **Claim costs are not evenly distributed**—specific demographic and vehicle segments contribute disproportionately to total claim value.
* **Middle-aged policyholders (26–65)** represent the largest share of both policies and claims, making them the most critical segment for underwriting optimization.
* **Private vehicle usage dominates the portfolio,** but commercial usage shows higher claim severity relative to volume.

These findings provide clear opportunities to refine pricing, improve risk segmentation, and focus loss-control strategies.

# Insights Deep Dive
### Category 1: Policyholder Demographics & Risk Profile
Key Insights:
* Policy distribution is almost evenly split between male and female policyholders, indicating balanced market penetration.
* The 26–65 age group holds the majority of policies, with consistent exposure across multiple age bands.
* Customers with Bachelor’s and High School education levels account for the highest claim amounts, suggesting higher exposure volume within these segments.
* Single and married customers drive the largest share of total claims, making marital status a meaningful segmentation variable.

### Category 2: Claims Behavior & Financial Impact
Key Insights:
* Total claim amount reaches $187.8M, with an average claim amount of ~$5K.
* Claim frequency remains relatively low (~0.5), but high-cost claims significantly impact total loss.
* Claim amounts are concentrated within a few high-volume customer segments rather than being evenly distributed.
* Education and marital status combined reveal distinct claim cost patterns, useful for actuarial modeling.

### Category 3: Vehicle & Usage-Based Risk Analysis
Key Insights:
* Private vehicles account for the majority of policies and total claim value.
* Certain car manufacturers (e.g., high-volume brands) consistently appear among top claim contributors.
* Vehicles manufactured between the early 2000s and mid-2010s show higher claim exposure, indicating potential aging-related risk.
* Commercial vehicles, while fewer in number, show relatively higher average claim impact. 

### Category 4: Geographic & Coverage Zone Insights
Key Insights:
* Claim amounts are evenly spread across coverage zones, but subtle differences exist between urban and rural segments.
* Highly urban and suburban zones contribute slightly higher claim totals, likely due to traffic density and accident exposure.
* No single zone dominates risk entirely—suggesting portfolio diversification across regions is currently effective.

# Recommendations:
Based on the insights above, the insurance underwriting and risk teams should consider the following actions:

* Refine pricing models for high-claim demographic segments (mid-age, high-volume education groups).
* Introduce targeted risk-adjusted premiums for older vehicle models with consistently higher claims.
* Enhance commercial vehicle underwriting rules, given their higher claim severity despite lower policy volume.
* Use education and marital status as secondary risk indicators in segmentation and cross-sell strategies.
* Maintain geographic diversification, while monitoring urban zones for emerging risk trends.
  
# Assumptions and Caveats:

* Claim frequency is treated as an average metric due to the absence of individual claim timelines.
* The dataset represents a snapshot-style analytical extract, not real-time transactional data.
* No external economic or weather factors were included, which may influence real-world claim behavior.

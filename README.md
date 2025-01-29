# COVID-19 Policy Analytics and Data Infrastructure

## Overview
This project focuses on analyzing and recommending effective COVID-19 policies to control the pandemic in the fictional country of **Caladan** (population: 3.2 million). By leveraging **Azure Data Factory**, **SQL Data Warehouse**, **Power BI**, and other cloud-based tools, this project builds a robust data infrastructure for ingesting, transforming, and analyzing COVID-19-related data. The goal is to identify the **most effective yet unrestrictive policies** that minimize growth rates for deaths and cases.

---

##  Data Pipeline and Architecture

### **Data Flow Overview**
1. **Data Sources**:
   - Data is ingested from **Azure SQL**, **CosmosDB**, and **Azure VM** into the pipeline via **Azure Data Factory**.
   - Key datasets include case rates, death rates, policy details, and demographic data.

2. **Data Transformation**:
   - Cleaned and stored as **parquet** files in **Azure Data Lake**.
   - Schema optimized for querying using **ODS (Operational Data Store)** techniques.

3. **Data Warehousing**:
   - Transformed data is stored in **Azure SQL Data Warehouse**.
   - Accessible via **Azure Synapse Analytics** for reporting and visualization.

4. **Visualization**:
   - Power BI dashboards provide insights into policy effectiveness and trends.

---

###   Architecture Diagram
![architecture drawio](https://github.com/user-attachments/assets/b7402a16-3833-4d0d-a63a-6eebd45c5de4)


---

###  Schema Diagram
![team17covid19schema drawio](https://github.com/user-attachments/assets/45de8eae-ddcb-46ea-b97c-0295cd57b6f0)



---

##  Key Components and Files

### **1. ARM Templates**
- **[Factory Template](ds310Team7Covid19_ARMTemplateForFactory.json)**: Deploys the Azure Data Factory.
- **[Parameters Template](ds310Team7Covid19_ARMTemplateParametersForFactory.json)**: Parameter configuration for resource deployment.
- **[Master Templates](ArmTemplate_master.json)**: Unified templates for all resources.

### **2. Power BI Dashboard**
- File: `DS310.pbix`
- Includes:
  - Correlation matrices for policy effectiveness.
  - Trend analysis of cases and death growth rates.
  - Policy effectiveness by time period and region.

### **3. Reports**
- **[Executive Summary](covid 19 executive summary copy.pdf)**: Highlights key insights and recommendations.
- **[Team Report](team 17 ds310 covid19 project copy.pdf)**: Detailed documentation of the data pipeline, analysis, and results.

---

##  Key Findings

### **Policy Effectiveness**
- **Top Performing Policies**:
  - **C2 (Workplace Closures)**: Significant in reducing case growth.
  - **C5 (Public Transport Closures)**: Highly effective with minimal disruption.
  - **C6 (Stay-at-home Orders)**: Effective when implemented during peaks.

### **Data Insights**
- Countries like **Canada** and **New Zealand** implemented the most effective policies, with the lowest growth rates in deaths and cases.
- Growth rates below **1% for deaths** and **3% for cases** were achieved through a combination of moderate restrictions and high compliance.



##  Future Work
- Incorporate real-time data updates to enhance decision-making.
- Expand analysis to include **vaccine distribution data**.
- Apply advanced machine learning models to predict the long-term effects of policies.


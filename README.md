# 🚀 Project Overview

Enterprise Sales Performance dashboard built with **Power BI**. Features advanced modeling, **70+ complex DAX measures**, and custom analytics including **Row-Level Security (RLS)**, dynamic KPI achievement trackers, and sophisticated time intelligence functions for executive and operational reporting.

---

## ⚙️ Project Structure & Technical Deep Dive

### Process (Enterprise Level – Step by Step)

1.  **Data Acquisition & Modeling:** Initial data ingestion, cleaning, and transformation using Power Query (M Language).
2.  **Star Schema Design:** Establishing a robust and efficient Star/Snowflake Hybrid data model to optimize performance.
3.  **DAX Development:** Implementing over 70 complex DAX measures for time intelligence, context control, and financial calculations (Profit, Margin, Target vs. Actual).
4.  **Security Implementation:** Applying **Row-Level Security (RLS)** roles (User A, User B) to enforce data access restrictions based on category and subcategory.
5.  **Dashboard Design & UX:** Creating two distinct, professionally formatted dashboards (Executive & Sales) using custom visuals, color coding, and alignment.
6.  **Advanced Interactivity:** Integrating Drill-Throughs, dynamic Tooltips (3-year comparison), and button-based slicer interaction for marketing analysis.

---

## ⚙️ Data Model

The data model is built upon a **Star Schema/Snowflake Hybrid** design to ensure high efficiency and performance in analytical processes.

* **Fact Table:** The central **Sales** table contains the sales metrics (Quantity, Amount, Profit, Cost, etc.) and links to all surrounding dimension tables.
* **Dimension Tables:** Includes **Product**, **Stores**, **Geography**, **Date\_New**, **Promotion**, **Marketing**, and **Channel**.
* **Relationships:** **One-to-Many (1:\*)** relationships were established to ensure correct filter propagation from dimensions to the fact table.

---
## Visuals Used :

* **KPI Cards / Gauges:** For displaying performance metrics (Sales, Profit, Orders) against targets and LY%.
* **Bar/Column Charts:** Used for categorical breakdown (T-Sales by Product Category, T-Orders by Channel).
* **Line Charts:** Essential for trend analysis (T-Sales over time, Monthly Trend comparison).
* **Donut/Pie Charts:** For status breakdown (Sales by Status, T-Profit & T-Cost by Continent).
* **Maps (Shape Map/Filled Map):** For geographical analysis of Sales/Profit distribution.
* **Matrix/Table Visuals:** For detailed breakdown and RLS validation (Country % of Continent Sales).

## Interactive Slicers (Synced Across All Pages) :

* **Year Slicer (Single-Select)**
* **Month Slicer (Single-Select)**
* **Country Slicer**
* **Date Slicer (Day-level selection)**


---

## 🔢 Technical Achievement: Advanced DAX Measures

**The project significantly exceeds the use of 70 DAX Measures!**

Advanced functions from the language **DAX (Data Analysis Expressions)** were extensively utilized to create complex and dynamic measures that support all required analyses.

* **Examples of DAX Functionality Employed:**
    * **Time Intelligence:** Use of functions like `CALCULATE`, `SAMEPERIODLASTYEAR`, `DATEADD`, and `DATESYTD` for executing crucial time comparisons (LY, YTD LY).
    * **Aggregation and Filtering:** Use of `CALCULATE`, `FILTER`, and `ALL`/`ALLEXCEPT`/`REMOVEFILTERS` to implement advanced calculations such as **Sales % of Continent Total** and target achievement logic.
    * **Conditional Logic:** Use of `IF`, `SWITCH`, and `HASONEVALUE` to create dynamic targeting logic and KPI performance tracking (Target Achievement Cards).
    * **Windowing/Range Functions:** Use of `DATEADD` and `DATEINPERIOD` to create advanced future-dated time period analysis (e.g., next 1 week, 1 month, 6 months for future orders).

---

## 📊 Key Dashboards

Four main dashboards, along with specialized Drill-Through and analysis pages, were developed:

### 1. Executives Dashboard
* **Focus:** Strategic metrics (Total Cost, T-Profit, Total Discount) and overall target performance.
* **Geographic Analysis:** Distribution of Profit and Sales by Continent and Country, including a table analyzing the **Country's Contribution as a Percentage of Continent Sales (Context Control)**.

### 2. Sales Dashboard
* **Focus:** Detailed sales performance by product category and temporal trend.
* **Features:** Display of main metrics (T-Sales, T-Profit, Total Orders) with achievement percentages, and a dynamic monthly trend comparison of Ordered vs. Delivered amounts.

### 3. Drill-Down Pages (Category & Region)
* **Category Overview:** In-depth analysis of the top sales category, displaying the **Top 5 Subcategories dynamically**, and tracking Discount vs. Profit.
* **Region Overview (Drill-Through Target):** Regional performance analysis (US, North America), tracking total orders and sales vs. cost over the years.

### 4. Marketing Dashboard
* **Focus:** Analyzing marketing campaign performance (Clicks) across custom and dynamic time periods (YTD, Last 15/30/45 days, and custom period comparisons).
---

## Dashboard Screenshots (Click to enlarge) :
<img src="https://github.com/Mohamed-Nofal-DataAnalysis/PowerBI-Enterprise-Sales-Solution/blob/main/Sales%20Dashboard.png">
<img src="https://github.com/Mohamed-Nofal-DataAnalysis/PowerBI-Enterprise-Sales-Solution/blob/main/Dril_Category%20Dashboard.png">
<img src="https://github.com/Mohamed-Nofal-DataAnalysis/PowerBI-Enterprise-Sales-Solution/blob/main/Dril_Subcategory%20Dashboard.png">
<img src="https://github.com/Mohamed-Nofal-DataAnalysis/PowerBI-Enterprise-Sales-Solution/blob/main/Region%20Dashboard.png">
<img src="https://github.com/Mohamed-Nofal-DataAnalysis/PowerBI-Enterprise-Sales-Solution/blob/main/Dill_Region%20Dashboard.png">
<img src="https://github.com/Mohamed-Nofal-DataAnalysis/PowerBI-Enterprise-Sales-Solution/blob/main/Store%20Dashboard.png">
<img src="https://github.com/Mohamed-Nofal-DataAnalysis/PowerBI-Enterprise-Sales-Solution/blob/main/Marketing%20Dashboard.png">
<img src="https://github.com/Mohamed-Nofal-DataAnalysis/PowerBI-Enterprise-Sales-Solution/blob/main/Model.png">
---

## ❓ Questions (KPIs) Answered Instantly Across Dashboards

| Requirement | Description and Achievement |
| :--- | :--- |
| **1 & 2: Advanced Monthly Trend Analysis** | **Q: What is the monthly trend difference between Ordered Amount and Delivered Amount, compared with the values from the last three years?** |
| **3: Row-Level Security (RLS)** | **Q: How to enforce data access so User B can only see 'Car Video' data within 'TV and Video' category?** (Addressed via RLS). |
| **4: Strategic KPIs** | **Q: What is the current Total Sales, Profit, and Cost, versus target and YTD Last Year performance?** |
| **5: Dynamic Top 5 Subcategories** | **Q: What are the Top 5 best-performing subcategories within the current highest-selling main category?** |
| **6: Advanced Drill-Through** | **Q: What is the full historical sales trend for a specific country, regardless of the year currently selected on the dashboard?** |
| **7: Percentage of Continent (Context Control)** | **Q: What is the sales contribution of a specific country as a percentage of its entire continent's sales?** (Filtering context controlled via DAX). |
| **8: Future Delivery Orders** | **Q: How many orders are scheduled for delivery in the next 1 week, 15 days, 1 month, and 6 months from today?** |
| **9: Active Promotions** | **Q: How many promotions were actively running in any given month between 2011 and 2014, including open-ended promotions?** |
| **10: KPI Performance Dashboard** | **Q: Out of the 10 core KPIs, how many are currently exceeding their assumed targets?** (Visualized via dynamic cards and detailed tooltips). |
| **11: Dynamic Marketing Analysis** | **Q: What is the Clicks Change % (with trend) when comparing the Last 15 Days vs. the same 15 days Last Year, or any two manually selected periods?** |

---

## 🔎 Project Insights

* **Performance Gap:** Initial analysis consistently highlights a performance gap (indicated by the negative percentage changes across T-Sales and T-Profit in the main KPIs) compared to last year's performance (LY). This requires deeper investigation into the specific categories or regions driving the decline.
* **Geographic Contribution:** While North America is the dominant sales region, the relative performance and profitability of other continents (Asia, Europe) must be tracked closely, especially their contribution percentage to the total.
* **Marketing Efficacy:** The dynamic marketing analysis shows significant fluctuations in Avg Clicks, especially in Q4 of 2025. The ability to compare arbitrary periods will be critical for the marketing team to isolate the impact of specific campaigns or external events.

## ⭐ Final Conclusion

This Advanced Sales Analytics Project in Power BI demonstrates **superior proficiency** in complex data modeling, a **mastery of the DAX language** with over 70 measures implemented, and exceptional skills in professional dashboard design. The solution successfully addresses highly specific, advanced analytical requirements (RLS, dynamic top-N, advanced time intelligence) and provides a powerful, scalable, and insightful platform for data-driven decision-making across all levels of the organization.

# 🚀 Project Overview

This project represents a comprehensive and advanced data analytics solution developed using **Power BI**. Its primary goal is to transform raw sales data into strategic and actionable operational insights. The solution is designed to equip executive management and the sales team with dynamic and effective tools for performance evaluation, KPI tracking, and analysis of market, geographical, and marketing trends.

## 💡 Key Objectives

* **Strategic and Operational Dashboards:** Create two main dashboards (Executives Dashboard and Sales Dashboard) to cater to different user levels.
* **Performance vs. Target Analysis:** Develop sophisticated measures to track Sales, Profit, and Cost against annual targets and Year-to-Date Last Year (YTD LY) performance.
* **Drill-Through and Drill-Down Capabilities:** Integrate advanced navigation features for in-depth analysis across product category, region, and store level.
* **Row-Level Security (RLS):** Implement advanced security constraints to ensure users can only access their designated data (as per Requirement 3).
* **Time-Based Marketing Analysis:** Establish a dedicated marketing dashboard to analyze Clicks performance across dynamic and variable timeframes (YTD, Last 15/30/45 days, and custom period comparisons).

---

## ⚙️ Data Model

The data model is built upon a **Star Schema/Snowflake Hybrid** design to ensure high efficiency and performance in analytical processes.

* **Fact Table:** The central **Sales** table contains the sales metrics (Quantity, Amount, Profit, Cost, etc.) and links to all surrounding dimension tables.
* **Dimension Tables:** Includes **Product**, **Stores**, **Geography**, **Date\_New**, **Promotion**, **Marketing**, and **Channel**.
* **Relationships:** **One-to-Many (1:\*)** relationships were established to ensure correct filter propagation from dimensions to the fact table.

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

## ✅ Summary of Completed Requirements and Enhancements

| Requirement | Description and Achievement |
| :--- | :--- |
| **1 & 2: Advanced Monthly Trend Analysis** | Line chart comparing "Ordered Amount" vs. "Delivered Amount." **Advanced Feature:** A sophisticated Tooltip shows the selected month's values for the last 3 years. The selected month is visually highlighted. |
| **3: Row-Level Security (RLS)** | RLS table created and **User A** (full "TV and Video" category access) and **User B** (limited to "Car Video" subcategory) roles implemented successfully. |
| **4: Strategic KPIs** | Five strategic KPIs (e.g., T-Sales, T-Profit, Total Orders) were created, each featuring **LY, LY YTD, Target, Actual vs Target, and % vs LY YTD** comparisons. |
| **5: Dynamic Top 5 Subcategories** | Used dynamic `RANKX` logic to first identify the **Highest Selling Category**, and then display the top 5 subcategories **within that category**, dynamically changing with slicers. |
| **6: Advanced Drill-Through** | Implemented a Drill-Through that allows navigation from a country to the "Region Overview" page to view the **country's full historical data** (past years) **regardless** of the year selected on the main page (overriding the year filter). |
| **7: Percentage of Continent (Context Control)** | Created the `Sales % of Continent Total` measure using `ALLEXCEPT`/`REMOVEFILTERS` to control the filter context, ensuring the percentage remains fixed to the continent total even when filtering by country. |
| **8: Future Delivery Orders** | Complex DAX logic utilizing `DATEADD`/`FILTER` on the **Sales** table to count orders scheduled for delivery within the **Next 1 Week, 15 Days, 1 Month, and 6 Months** from a selected date. |
| **9: Active Promotions** | Created a measure to calculate the number of promotions active in any month (2011-2014), correctly handling promotions that **do not have an End Date** (assuming they are permanently valid). |
| **10: KPI Performance Dashboard** | Created two dynamic cards for **10 KPIs** showing the count of KPIs **On Target** and **Under Target**. **Advanced Feature:** A Tooltip displays a clean, structured list of the specific KPIs in each category upon hover. |
| **11: Dynamic Marketing Analysis** | Designed the Marketing Dashboard to allow users to toggle between **YTD, Last N Days (15/30/45)**, and **Custom Periods (Period 1 vs Period 2)** for comparison, displaying percentage change and trend lines. |

---

## 🔎 Project Insights

* **Performance Gap:** Initial analysis consistently highlights a performance gap (indicated by the negative percentage changes across T-Sales and T-Profit in the main KPIs) compared to last year's performance (LY). This requires deeper investigation into the specific categories or regions driving the decline.
* **Geographic Contribution:** While North America is the dominant sales region, the relative performance and profitability of other continents (Asia, Europe) must be tracked closely, especially their contribution percentage to the total.
* **Marketing Efficacy:** The dynamic marketing analysis shows significant fluctuations in Avg Clicks, especially in Q4 of 2025. The ability to compare arbitrary periods will be critical for the marketing team to isolate the impact of specific campaigns or external events.

## ⭐ Final Conclusion

This Advanced Sales Analytics Project in Power BI demonstrates **superior proficiency** in complex data modeling, a **mastery of the DAX language** with over 70 measures implemented, and exceptional skills in professional dashboard design. The solution successfully addresses highly specific, advanced analytical requirements (RLS, dynamic top-N, advanced time intelligence) and provides a powerful, scalable, and insightful platform for data-driven decision-making across all levels of the organization.

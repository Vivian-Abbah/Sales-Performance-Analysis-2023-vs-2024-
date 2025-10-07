🧮 Sales Performance Analysis (2023 vs 2024)

📘 Introduction
This project explores company-wide sales data to uncover revenue, cost, and profit trends across multiple product categories and regions between **2023** and **2024**.  
Using **Microsoft Excel** and **Power Query**, the dataset was transformed, cleaned, and visualized to create an interactive dashboard that highlights sales performance, profitability, and year-over-year growth.

<img width="919" height="459" alt="Sales Performance Dashboard" src="https://github.com/user-attachments/assets/87dee875-07e0-48a9-b146-6f52278f6bc7" />

🎯 Objective of the Project
The main goal was to:
- Track and compare **year-over-year (YoY)** sales and profit growth.  
- Identify **top-performing products** and **underperforming regions**.  
- Understand **seasonality** and **monthly revenue trends**.  
- Provide actionable, data-driven recommendations for the next business cycle.

🧭 Executive Summary
The analysis revealed a strong **34 % YoY increase in profit**, accompanied by **24 % growth in quantity sold** and **11 % growth in cost**.  
This indicates an overall improvement in operational efficiency and a healthy margin expansion.  
Key drivers include:
- High demand for **Monitors** and **Mice** products.  
- Better supply-chain cost control.  
- Strong regional performance in the **South and West** markets.

Conversely, **Laptops** and **Printers** showed weaker results, suggesting opportunities for pricing or promotional adjustments.

❗ Problem Statement
Although total company revenue increased, **sales performance across regions and products was inconsistent**.  
There was a need to understand:
- Why some regions lagged behind,  
- Which products contributed most to profit,  
- How seasonal trends affected revenue, and  
- How to sustain year-round growth without margin erosion.

🧰 Tools and Methodologies
| Tool | Purpose |
|------|----------|
| **Microsoft Excel** | Data analysis, pivot tables, dashboard creation |
| **Power Query** | Data cleaning, transformation, and loading |
| **Conditional Formatting** | KPI highlighting for performance tracking |
| **Data Visualization** | Charts, trends, and comparative analysis |

💡 Problem Being Addressed
The business needed a **clear view of year-over-year performance** to evaluate marketing effectiveness, pricing efficiency, and operational cost control.  
This dashboard addressed that by linking data directly from Excel tables through Power Query to provide near real-time, dynamic updates.

🔍 Key Dataset and Methodology
**Dataset Fields:**  
Product_Name, Company, Export_Country, Date, Month, Year, Units_Sold, Unit_Price, Profit_per_Unit, Export_Value, Destination_Port, Transportation_Mode

Data Story & Process
1. **Data Source:** Internal Excel workbook with monthly export and sales logs.  
2. **Data Cleaning:** Removed blanks, standardized date formats, fixed currency symbols.  
3. **Transformations:** Added calculated columns for:
   - Total_Profit = Units_Sold * Profit_per_Unit
   - YoY%_Growth
   - MoM%_Growth
4. **Data Structure:** Tabular format with time dimension (month/year).  
5. **Bias & Limitations:** Seasonal spikes may distort year-end averages; incomplete data from one region (North) required interpolation.

🧹 Data Pre-Processing
- **Missing Values:** Replaced using median or interpolation where appropriate.  
- **Outlier Handling:** Detected using IQR and capped extreme profit values.  
- **Transformations:** Created KPI measures for:
  - Monthly revenue
  - YoY % profit growth
  - MoM % profit change
- **Data Splitting:** Split into 2023 and 2024 subsets for comparison.

🌍 Industry Context & Stakeholders
The analysis represents a **consumer electronics and accessories company** with a distribution network across four main regions — **North, South, East, and West**.  
Stakeholders include:
- Sales and marketing teams  
- Regional managers  
- Financial analysts  
- Executive leadership  
The insights directly influence regional sales planning, cost control, and marketing campaigns.

🔎 Pre-Analysis Phase
During exploration, initial questions included:
- Which regions generated the highest revenue in 2024?  
- Which product lines contributed most to profit?  
- How do monthly trends differ between 2023 and 2024?  
- Are costs rising faster than revenue?  

Preliminary analysis suggested potential underperformance in **Laptops and Printers** and room for regional improvement in the **North**.

📊 In-Analysis Phase
The following KPIs were calculated:
- **Total Sales** = $465 ,605  
- **Total Profit** = $411 ,627  
- **Total Cost** = $63 ,978  
- **Quantity Sold** = 899  
- **Profit Growth YoY:** + 34 %  
- **Sales Growth YoY:** + 30 %  
- **Cost Growth YoY:** + 11 %  

Conditional formatting was applied:
- 🔺 Green = Above Target Growth (> 25 %)  
- ⚪ Amber = Moderate Growth (10–25 %)  
- 🔻 Red = Below Target (< 10 %)  

📈 Key Insights
1. **Profit Surge:** + 34 % YoY growth with improved cost control.  
2. **Regional Leaders:** South and West regions dominate revenue share.  
3. **Product Winners:** Monitors and Mice are the top-selling categories.  
4. **Underperformers:** Laptops and Printers show declining demand.  
5. **Seasonality:** Peak sales during May–August; December dip suggests missed opportunities.  
6. **Accessories vs Electronics:** Accessories outperformed core electronics, reflecting consumer price sensitivity.  
7. **Cost Efficiency:** Moderate cost growth despite higher volume sales → better procurement control.

🧩 Bonus Insights & Metric Correlations
- Positive correlation between **units sold** and **profit** (ρ ≈ 0.82).  
- **YoY profit growth** linked to regions with **optimized transportation modes**.  
- **Accessories sales growth** aligns with **lower cost per unit**, improving margin.

🧠 Recommendations
1. **Expand North & East Regions:** replicate South region strategies.  
2. **Revitalize Laptops & Printers:** bundle offers and seasonal discounts.  
3. **Enhance Q4 Promotions:** target holiday sales to counter December dip.  
4. **Maintain Margin Discipline:** use Power Query to track supplier cost trends.  
5. **Diversify Accessories Portfolio:** add wireless and ergonomic peripherals.  
6. **Forecasting & Planning:** build Excel predictive models for revenue projection.

🔄 Post-Analysis Phase
Follow-up evaluation shows consistent margin gains and regional performance improvement.  
Ongoing Power Query refresh cycles enable real-time tracking of YoY and MoM KPIs.

💥 Observations & Business Impact
- **Operational Efficiency Improved:** revenue grew faster than costs.  
- **Regional Gaps Identified:** insight for marketing and distribution plans.  
- **Product Lifecycle Clarity:** strategic reallocation toward high-margin items.  

📉 Data Visualization
Dashboard includes:
- **KPI Cards** for Sales, Profit, Cost, and Quantity.
-  📊 KPI Calculations and Formula Guide

This section explains how the **Year-over-Year (YoY)** and **Month-over-Month (MoM)** KPIs were calculated in **Excel** and **Power Query**, including logic, sample formulas, and conditional formatting rules.

🧮 1. KPI Summary Table

| KPI | Description | Formula (Excel) | Formula (Power Query) |
|-----|--------------|-----------------|-----------------------|
| **Total Sales** | Total sales revenue for each year | =SUMIFS(Sales, Year, 2024) | = List.Sum(#"Filtered Rows"[Sales]) |
| **Total Profit** | Profit across all products | =SUMIFS(Profit, Year, 2024) | = List.Sum(#"Filtered Rows"[Profit]) |
| **YoY % Sales Growth** | Growth from 2023 to 2024 | =((Sales_2024 - Sales_2023) / Sales_2023) | (CurrentYearSales - PrevYearSales) / PrevYearSales|
| **YoY % Profit Growth** | Year-over-year profit change | =((Profit_2024 - Profit_2023) / Profit_2023) | (CurrentYearProfit - PrevYearProfit) / PrevYearProfit |
| **MoM % Profit Growth** | Monthly change in profit | =(CurrentMonthProfit - PreviousMonthProfit) / PreviousMonthProfit | (Profit - PreviousMonthProfit) / PreviousMonthProfit |
| **Average Unit Price** | Price per unit sold | =AVERAGE(Unit_Price)| = List.Average(#"Filtered Rows"[Unit_Price]) |
| **Cost Efficiency Ratio** | Cost as % of sales | =(Total_Cost / Total_Sales) | (Cost / Sales) |
| **Profit Margin %** | Profit as % of sales | =(Profit / Sales) | (Profit / Sales) |
🧩 2. Power Query Transformation Steps

Here’s a simplified Power Query process used to build the KPI dataset:
Source → Promoted Headers → Changed Type →
Added Column: "Total Profit" = [Units Sold] * [Profit per Unit] →
Grouped by Year & Month →
Added Custom Columns:
   - YoY_Profit_Growth = ([Profit] - [PrevYearProfit]) / [PrevYearProfit]
   - MoM_Profit_Growth = ([Profit] - [PrevMonthProfit]) / [PrevMonthProfit] →
Loaded into Excel Table for Dashboard

- **Line Charts** for Monthly Revenue Trend (2023 vs 2024).  
- **Bar Charts** for Regional and Product-wise Performance.  
- **Category Filter Buttons** (Accessories vs Electronics).  
- **Conditional Formatting** for YoY and MoM Profit Indicators.  

🏁 Conclusion
This Excel + Power Query analysis provides a clear, data-driven view of the company’s performance.  
By combining YoY comparisons, regional breakdowns, and product trends, the organization can:
- Make faster, more accurate decisions.  
- Focus resources on high-growth segments.  
- Plan marketing initiatives around seasonality.  

The results prove that **even with Excel**, a well-structured data model and Power Query automation can deliver enterprise-grade insights.

🧭 Key Learnings
- Clean data = credible insights.  
- Visual storytelling enhances executive decision making.  
- Continuous refresh with Power Query keeps KPIs relevant.  

⚠️ Limitations
- Limited historical data (2 years only).  
- Manual entry errors in some records.  
- Does not include inventory or marketing cost factors.

🔮 Future Research
- Extend analysis to 5 years for trend forecasting.  
- Integrate Power BI for automated dashboards.  
- Combine CRM and regional marketing data for deeper customer segmentation.

📚 References & Appendices
- Internal Excel dataset (2023–2024 Sales).  
- Power Query transformation scripts.  
- Dashboard visuals created using Excel charts and conditional formatting.

🎨 Dashboard Color Codes
| Element | Color Code | Description |
|----------|------------|-------------|
| Background | `#A97B64` | Warm brown theme for neutral contrast |
| Highlight Text | `#F5DEB3` | Wheat tone for emphasis |
| Cards & Borders | `#3B2A22` | Deep coffee accent |
| Trend Lines | `#E0B090` (2023)  /  `#C08457` (2024) | Distinguish year-on-year performance |

🧩 Author
Data Analyst – Abbah Vivian Chidimma
📊 Project developed using Excel 2024 and Power Query for insight-driven decision support.


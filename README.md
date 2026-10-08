<div align="center">
 <h1>📊<br/>Gurdeep Singh : Business Intelligence & Sales Operations Analyst</h1>
 <img src="https://img.shields.io/badge/Experience-6%2B%20Years-brightgreen?style=normal"/>
 <img src="https://img.shields.io/badge/Location-Las%20Vegas%2C%20NV-blue?style=normal"/>
 <img src="https://img.shields.io/badge/Focus-BI%20%7C%20Sales%20Ops%20%7C%20Supply%20Chain-orange?style=normal"/>
 <img src="https://komarev.com/ghpvc/?username=YOUR_GITHUB_USERNAME&style=flat"/>
</div>
<br/>

I turn cross-functional data into revenue-protecting, cost-saving, and growth-driving decisions across hospitality, CPG, retail, and supply chain. I work directly with sales, finance, and operations teams to clean up reporting workflows and turn dense datasets into something leadership can act on.

# What I Do

### ⚡ Dashboards That Leadership Uses
I design and maintain Power BI and Excel dashboards that track KPIs in real time. At Monster Energy I built and owned 15+ of them for performance reviews and territory decisions.

### 📊 Reporting You Can Trust
I standardize reporting templates, audit CRM and ERP data, and catch errors before they reach a dashboard. This lifted reporting accuracy by 25% and cut reporting cycle time by 30%.

### 🎯 Forecasting and Demand Planning
I model demand patterns and track booking pace against forecast. At Mars this raised forecast accuracy by 18% and allocation accuracy from roughly 85% to 93%+ across 20+ distribution centers.

### 🧮 SQL and Automation
I write complex SQL to pull, join, and validate large sales and operational datasets, and automate recurring reports with Python and Excel macros.

### 🤝 Working With Teams
I partner with sales, finance, merchandising, procurement, and logistics teams, and present findings to regional and executive leadership.

## Where I Work

<details>
<summary>🏨 Sales Operations Analyst : GCG LLC (Jul 2025 - Present, Las Vegas, NV)</summary>

- Analyze sales, operational, financial, and guest-service data across a multi-property portfolio of premium franchised and IHG hotels
- Design and maintain real-time Power BI dashboards tracking hospitality KPIs
- Track group, corporate, and transient booking pace against forecast to flag pipeline gaps
- Maintain and audit CRM and RFP data across Marriott/IHG systems
- Prepare weekly and monthly performance packages for ownership and regional leadership
- Standardized month-end reporting templates across properties

</details>

<details>
<summary>🥤 Business & Data Analyst : Monster Energy (Feb 2022 - Jul 2025, Riverside County, CA)</summary>

- Built and owned 15+ KPI Excel and Power BI dashboards used by leadership
- Standardized enterprise reporting templates company-wide: +25% data accuracy, -30% reporting cycle time
- Wrote and optimized complex SQL queries against enterprise databases
- Automated recurring reporting workflows with Python and Excel macros
- Caught 40+ SKU-level errors before product launch by cross-checking sales data against master files
- Migrated legacy Excel reporting to Power BI

</details>

<details>
<summary>🍫 Supply Chain Analyst : Mars (Oct 2019 - Dec 2021, New Delhi, India)</summary>

- Mined ERP and Warehouse Management System (WMOS) data across 20+ distribution centers
- Raised forecast accuracy by 18% through demand-pattern modeling
- Built allocation-review dashboards adopted as the standard tool in supply chain planning meetings
- Reconciled ERP and WMOS data discrepancies weekly

</details>

<details>
<summary>📡 Data Analyst : Airtel (Jun 2019 - Sep 2019, Delhi, India)</summary>

- Built Excel variance-tracking reports comparing forecast vs. actual for regional planning

</details>

<details>
<summary>🍕 Junior Data Analyst : Domino's (Jan 2018 - May 2019, Ludhiana, India)</summary>

- Analyzed sales and inventory data across 50+ locations to support regional planning
- Flagged slow-moving SKUs and optimized stock reallocation

</details>

## Analytics Commands 🧮

<details>
<summary>SQL</summary>

```sql
-- sales vs master file check, catch SKU errors before they hit dashboards
SELECT s.sku, s.region, SUM(s.units) AS units_sold
FROM   sales s
LEFT JOIN sku_master m ON s.sku = m.sku
WHERE  m.sku IS NULL
GROUP  BY s.sku, s.region;

-- booking pace vs forecast by segment
SELECT segment,
       SUM(booked_rooms)                       AS booked,
       SUM(forecast_rooms)                     AS forecast,
       SUM(booked_rooms) - SUM(forecast_rooms) AS pace_gap
FROM   booking_pace
GROUP  BY segment;
```

</details>

<details>
<summary>DAX (Power BI)</summary>

```dax
Occupancy % = DIVIDE ( [Rooms Sold], [Rooms Available] )

ADR = DIVIDE ( [Room Revenue], [Rooms Sold] )

RevPAR = [Occupancy %] * [ADR]

Budget Variance % =
DIVIDE ( [Actual Revenue] - [Budget Revenue], [Budget Revenue] )
```

</details>

<details>
<summary>Python</summary>

```python
import pandas as pd

df = pd.read_excel("weekly_sales.xlsx")
df["variance"] = df["actual"] - df["forecast"]
summary = df.groupby("region")[["actual", "forecast", "variance"]].sum()
summary.to_excel("weekly_summary.xlsx")
```

</details>

<details>
<summary>Excel</summary>

```excel
=IFERROR((Actual - Forecast) / Forecast, 0)
=SUMIFS(Revenue, Region, A2, Month, B1)
=XLOOKUP(SKU, MasterList[SKU], MasterList[Category], "Not found")
```

</details>

## Tech Used
![SQL](https://img.shields.io/badge/sql-%23336791.svg?style=for-the-badge&logo=postgresql&logoColor=white)
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![Power BI](https://img.shields.io/badge/power_bi-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![Excel](https://img.shields.io/badge/Microsoft_Excel-217346?style=for-the-badge&logo=microsoftexcel&logoColor=white)
![Salesforce](https://img.shields.io/badge/Salesforce-00A1E0?style=for-the-badge&logo=salesforce&logoColor=white)
![SAP](https://img.shields.io/badge/SAP-0FAAFF?style=for-the-badge&logo=sap&logoColor=white)
![Snowflake](https://img.shields.io/badge/Snowflake-29B5E8?style=for-the-badge&logo=snowflake&logoColor=white)
![MySQL](https://img.shields.io/badge/mysql-4479A1.svg?style=for-the-badge&logo=mysql&logoColor=white)
![Oracle](https://img.shields.io/badge/Oracle-F80000?style=for-the-badge&logo=oracle&logoColor=white)

**Also:** Manhattan WMOS, ERP systems, ETL & data validation, KPI tracking, financial reporting, dashboard design

## Education 🎓
- M.S., Information Technology : California Baptist University
- MBA, Business Administration : California Baptist University
- B.S., Information Technology : Lovely Professional University

## Certifications 📜
- Oracle Database SQL Certified Associate
- SAP Certified Associate : Business Technology Platform (BTP)
- SAP Certified Associate : SAP Analytics Cloud (SAC)
- Salesforce Certified Administrator
- The Ultimate MySQL Bootcamp : Udemy, 2023
- Microsoft Azure & IBM : Microsoft, 2024

## Flex My GitHub Stats 📊
![Stats](https://github-readme-stats.vercel.app/api?username=YOUR_GITHUB_USERNAME&show_icons=true&theme=radical&count_private=true)
![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=YOUR_GITHUB_USERNAME&layout=compact&theme=radical)

![Streak](https://streak-stats.demolab.com/?user=YOUR_GITHUB_USERNAME&theme=radical)

## GitHub Trophies 🏆
![Trophies](https://github-profile-trophy.vercel.app/?username=YOUR_GITHUB_USERNAME&theme=radical&row=1&column=7)

## Connect With Me
[![LinkedIn](https://img.shields.io/badge/linkedin-%230077B5.svg?style=normal&logo=linkedin&logoColor=white)](YOUR_LINKEDIN_URL)
[![Portfolio](https://img.shields.io/badge/Portfolio-black?style=normal&logo=googlechrome&logoColor=white)](YOUR_PORTFOLIO_URL)
[![Email](https://img.shields.io/badge/Email-D14836?style=normal&logo=gmail&logoColor=white)](mailto:gurdeepsaini05@gmail.com)

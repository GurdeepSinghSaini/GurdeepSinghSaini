<h1 align="center"> Hi 👋🏻, I'm Gurdeep Singh </br>
</h1>
<p align="center">Business Intelligence and Sales Operations Analyst 📊</p>
<p align="center">Turning dense data into decisions leadership can act on ⚡</p>
<p align="center">
<a href="YOUR_LINKEDIN_URL" target="_blank"><img alt="" src="https://img.shields.io/badge/LinkedIn-000?logo=linkedin&logoColor=0A66C2&style=for-the-badge" style="vertical-align:center" /></a>
<a href="YOUR_PORTFOLIO_URL" target="_blank"><img alt="" src="https://img.shields.io/badge/Portfolio-000?logo=googlechrome&logoColor=yellow&style=for-the-badge" style="vertical-align:center" /></a>
<a href="mailto:gurdeepsaini05@gmail.com" target="_blank"><img alt="" src="https://img.shields.io/badge/Email-000?logo=gmail&logoColor=D14836&style=for-the-badge" style="vertical-align:center" /></a></p>

```bash
$ whoami
gurdeep_singh

$ cat about.txt
role        : Business Intelligence and Sales Operations Analyst
experience  : 6+ years
industries  : hospitality, CPG, retail, supply chain
location    : Las Vegas, Nevada
works_with  : sales, finance and operations teams
focus       : clean reporting, reliable forecasts, decisions leadership can act on
```

## Results 🚀

```sql
SELECT metric, impact
FROM   career_results
ORDER  BY impact DESC;
```

| metric | impact |
|---|---|
| reporting_accuracy | +25% |
| forecast_precision | +18% |
| reporting_cycle_time | -30% |
| allocation_accuracy | ~85% to 93%+ |
| sku_errors_caught_before_launch | 40+ |

## Analytics Commands 🧮

**SQL** : joining and validating large sales datasets

```sql
-- sales vs master file check, catch SKU errors before they hit dashboards
SELECT s.sku, s.region, SUM(s.units) AS units_sold
FROM   sales s
LEFT JOIN sku_master m ON s.sku = m.sku
WHERE  m.sku IS NULL
GROUP  BY s.sku, s.region;
```

```sql
-- booking pace vs forecast by segment
SELECT segment,
       SUM(booked_rooms)                      AS booked,
       SUM(forecast_rooms)                    AS forecast,
       SUM(booked_rooms) - SUM(forecast_rooms) AS pace_gap
FROM   booking_pace
GROUP  BY segment;
```

**DAX** : Power BI measures

```dax
Occupancy % = DIVIDE ( [Rooms Sold], [Rooms Available] )

ADR = DIVIDE ( [Room Revenue], [Rooms Sold] )

RevPAR = [Occupancy %] * [ADR]

Budget Variance % =
DIVIDE ( [Actual Revenue] - [Budget Revenue], [Budget Revenue] )
```

**Python** : automating recurring reports

```python
import pandas as pd

df = pd.read_excel("weekly_sales.xlsx")
df["variance"] = df["actual"] - df["forecast"]
summary = df.groupby("region")[["actual", "forecast", "variance"]].sum()
summary.to_excel("weekly_summary.xlsx")
```

**Excel** : forecast vs actual

```excel
=IFERROR((Actual - Forecast) / Forecast, 0)
=SUMIFS(Revenue, Region, A2, Month, B1)
=XLOOKUP(SKU, MasterList[SKU], MasterList[Category], "Not found")
```

## Work Experience 💼

```bash
$ git log --oneline --career
```

### 🏨 Sales Operations Analyst : GCG LLC
*Jul 2025 - Present | Las Vegas, NV*
Reporting and revenue analysis across a multi-property portfolio of premium franchised and IHG hotels. Real-time Power BI dashboards for hospitality KPIs, booking pace tracking against forecast, CRM and RFP data audits across Marriott/IHG systems, and weekly and monthly performance packages for ownership and regional leadership.

### 🥤 Business & Data Analyst : Monster Energy
*Feb 2022 - Jul 2025 | Riverside County, CA*
Built and owned 15+ KPI dashboards in Excel and Power BI used by leadership for performance reviews and territory decisions. Standardized reporting templates company-wide, moved legacy Excel reporting to Power BI, wrote complex SQL against enterprise databases, and automated recurring reports with Python and Excel macros.

### 🍫 Supply Chain Analyst : Mars
*Oct 2019 - Dec 2021 | New Delhi, India*
Worked with ERP and WMOS data across 20+ distribution centers. Raised forecast accuracy by 18% through demand-pattern modeling and built allocation-review dashboards that became the standard tool in supply chain planning meetings.

### 📡 Data Analyst : Airtel
*Jun 2019 - Sep 2019 | Delhi, India*
Forecast vs. actual variance reports in Excel for regional planning.

### 🍕 Junior Data Analyst : Domino's
*Jan 2018 - May 2019 | Ludhiana, India*
Sales and inventory analysis across 50+ locations to support regional planning.

## Tech Stack 💻

```bash
$ ls ~/stack
```

#### Languages / Querying
![SQL](https://img.shields.io/badge/-SQL-000?style=for-the-badge&logo=postgresql)
![Python](https://img.shields.io/badge/-Python-000?style=for-the-badge&logo=python)

#### BI / Reporting
![Power BI](https://img.shields.io/badge/-Power%20BI-000?style=for-the-badge&logo=powerbi&logoColor=F2C811)
![Excel](https://img.shields.io/badge/-Excel-000?style=for-the-badge&logo=microsoftexcel&logoColor=217346)
![SAP Analytics Cloud](https://img.shields.io/badge/-SAP%20Analytics%20Cloud-000?style=for-the-badge&logo=sap&logoColor=0FAAFF)

#### CRM / ERP / Warehouse Systems
![Salesforce](https://img.shields.io/badge/-Salesforce-000?style=for-the-badge&logo=salesforce&logoColor=00A1E0)
![SAP](https://img.shields.io/badge/-SAP%20ERP-000?style=for-the-badge&logo=sap&logoColor=0FAAFF)
![Manhattan WMOS](https://img.shields.io/badge/-Manhattan%20WMOS-000?style=for-the-badge)

#### Databases / Data Warehouse
![Snowflake](https://img.shields.io/badge/-Snowflake-000?style=for-the-badge&logo=snowflake&logoColor=29B5E8)
![MySQL](https://img.shields.io/badge/-MySQL-000?style=for-the-badge&logo=mysql&logoColor=4479A1)
![Oracle](https://img.shields.io/badge/-Oracle-000?style=for-the-badge&logo=oracle&logoColor=F80000)

#### Also
ETL & Data Validation • KPI Tracking • Forecasting • Financial Reporting • Dashboard Design • Cross-Functional Collaboration

## Education 🎓

```bash
$ cat education.txt
M.S.  Information Technology    California Baptist University
MBA   Business Administration    California Baptist University
B.S.  Information Technology    Lovely Professional University
```

## Certifications 📜

```bash
$ cat certifications.txt
Oracle Database SQL Certified Associate
SAP Certified Associate : Business Technology Platform (BTP)
SAP Certified Associate : SAP Analytics Cloud (SAC)
Salesforce Certified Administrator
The Ultimate MySQL Bootcamp : Udemy, 2023
Microsoft Azure & IBM : Microsoft, 2024
```

```sql
SELECT insights
FROM   data
WHERE  decisions = 'better';
-- Gurdeep Singh
```

## Current GitHub Stats 📊
![Stats](https://github-readme-stats.vercel.app/api?username=YOUR_GITHUB_USERNAME&show_icons=true&hide_border=false&theme=jolly&count_private=true&include_all_commits=true)
![Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=YOUR_GITHUB_USERNAME&show_icons=true&hide_border=false&theme=jolly&count_private=true&include_all_commits=true&layout=compact)

## GitHub Streaks 🔥
![Streaks](https://nirzak-streak-stats.vercel.app/?user=YOUR_GITHUB_USERNAME&theme=jolly&date_format=j%20M%5B%20Y%5D)

### Thanks for Visiting my GitHub Profile!

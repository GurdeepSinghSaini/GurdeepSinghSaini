from docx import Document
from docx.shared import Pt, Inches, RGBColor
from docx.enum.text import WD_ALIGN_PARAGRAPH, WD_LINE_SPACING

doc = Document()

# Page setup
sec = doc.sections[0]
sec.top_margin = Inches(0.5)
sec.bottom_margin = Inches(0.5)
sec.left_margin = Inches(0.6)
sec.right_margin = Inches(0.6)

# Base styles
normal = doc.styles['Normal']
normal.font.name = 'Calibri'
normal.font.size = Pt(10.5)
normal.paragraph_format.space_after = Pt(4)
normal.paragraph_format.line_spacing = 1.15

ACCENT = RGBColor(31, 58, 138)  # navy-ish accent

def add_section_title(text):
    p = doc.add_paragraph()
    run = p.add_run(text.upper())
    run.bold = True
    run.font.size = Pt(12)
    run.font.color.rgb = ACCENT
    p.space_before = Pt(10)
    p.space_after = Pt(4)

def add_bullets(lines):
    for line in lines:
        p = doc.add_paragraph(style='List Bullet')
        p.paragraph_format.space_after = Pt(2)
        p.add_run(line)

def add_experience(company, title, dates, bullets):
    # Header line: Company — Title ............. Dates
    p = doc.add_paragraph()
    r1 = p.add_run(f"{company} — {title}")
    r1.bold = True
    p.paragraph_format.space_after = Pt(2)
    # Add dates on next line (cleaner for ATS)
    p2 = doc.add_paragraph(dates)
    p2.paragraph_format.space_after = Pt(2)
    add_bullets(bullets)

# Header
name_p = doc.add_paragraph()
name_run = name_p.add_run("Gurdeep Singh")
name_run.bold = True
name_run.font.size = Pt(20)
name_run.font.color.rgb = ACCENT
name_p.alignment = WD_ALIGN_PARAGRAPH.LEFT

tag_p = doc.add_paragraph("Business Analytics Professional | MBA, MS-IT")
tag_p.paragraph_format.space_after = Pt(2)

contact_p = doc.add_paragraph("CA | 702-324-3864 | gurdeepsaini05@gmail.com")
contact_p.paragraph_format.space_after = Pt(8)

# Summary
add_section_title("Summary")
doc.add_paragraph(
    "Results-driven Business Intelligence and Data Analytics Professional with 9+ years of experience in financial reporting, "
    "forecasting, and data strategy across retail, beverage, and technology sectors. Skilled in SQL, Python, R, Tableau, Power BI, "
    "and advanced Excel to deliver automated solutions, predictive analytics, and executive dashboards that drive revenue growth and "
    "operational efficiency. Proven expertise in P&L management, budgeting, compliance reporting, and variance analysis, with a strong "
    "record of aligning analytics to business objectives. Adept at ETL processes, ERP implementations, data warehousing, and data "
    "governance frameworks, ensuring accuracy and scalability of enterprise reporting systems. Collaborative and detail-oriented; "
    "experienced in leading cross-functional teams, mentoring analysts, and partnering with executives to translate raw data into "
    "actionable insights. Pursuing AWS Cloud Practitioner Certification to expand cloud-based analytics expertise."
)

# Education
add_section_title("Education")
add_bullets([
    "Master of Business Administration — California Baptist University, Riverside, CA",
    "Master of Science in Information Technology — California Baptist University, Riverside, CA",
])

# Skills
add_section_title("Skills")
add_bullets([
    "Financial Management: P&L Management, Budgeting & Forecasting, EBITDA Enhancement, Financial Compliance & Governance",
    "Leadership: Stakeholder Collaboration, Team Leadership & Mentorship, Strategic Planning",
    "Analytics & Tools: SQL, Tableau, Power BI, Advanced Excel (Pivot Tables, Forecasting Models, Dashboards)",
    "Programming: Python, R (Data Modeling, Automation)",
    "Other: Data Governance, Audit & Validation, Reporting Optimization, SOP Documentation",
])

# Experience
add_section_title("Experience")

add_experience(
    "Burlington Stores, CA", "Business Intelligence Analyst", "Dec 2023 – Present",
    [
        "Lead BI initiatives to enhance operational efficiency, merchandising strategies, and sales performance through advanced reporting and visualization tools.",
        "Design and deploy scalable Tableau and Power BI dashboards providing executives and managers real-time financial, operational, and customer insights.",
        "Develop and optimize SQL queries and Python automation to streamline ETL, integration, cleansing, and validation across multiple systems.",
        "Collaborate with finance, merchandising, and operations to support forecasting, budgeting, and inventory strategies that improve bottom-line results.",
        "Implement data governance frameworks and ensure compliance with corporate and regulatory reporting requirements.",
        "Train and mentor junior analysts on BI tools, SQL optimization, and financial reporting best practices.",
    ]
)

add_experience(
    "Monster Energy, Corona, CA", "Data Analyst", "Feb 2022 – Nov 2023",
    [
        "Delivered actionable insights on sales performance, marketing ROI, and financial outcomes informing executive decisions.",
        "Built and maintained enterprise-grade Tableau and Power BI dashboards tracking KPIs across finance, sales, and operations.",
        "Conducted variance analysis and financial modeling to evaluate promotional campaigns, distribution strategies, and supply chain performance.",
        "Standardized KPI definitions and streamlined reporting, reducing turnaround time by 25%.",
        "Developed automated data pipelines using SQL and Python to integrate disparate data sources into unified reporting environments.",
        "Partnered with senior leadership to identify revenue opportunities and reduce operational inefficiencies.",
    ]
)

add_experience(
    "Mars, Incorporated (Infosys), NY", "Business & Data Analyst", "Oct 2019 – Dec 2021",
    [
        "Managed enterprise analytics projects supporting ERP and financial system implementations across multinational business units.",
        "Collaborated with supply chain, finance, and IT to gather and translate business requirements.",
        "Developed and implemented data integration solutions to unify ERP and warehouse management systems across global locations.",
        "Designed dashboards and reports to track product traceability, inventory levels, and supply chain KPIs.",
        "Developed advanced financial models for forecasting, scenario planning, and profitability analysis influencing strategic investment decisions.",
        "Built executive dashboards in Tableau and Power BI for revenue, expense, and market trends.",
        "Partnered with technology teams to migrate legacy reporting into modern BI platforms, improving scalability and user adoption.",
        "Validated data migration to ensure accuracy, consistency, and compliance; delivered training and comprehensive documentation; supported change management and continuous improvements.",
    ]
)

add_experience(
    "Airtel, Delhi, India", "Data Analyst", "Jun 2017 – Sep 2019",
    [
        "Analyzed large datasets to support corporate budgeting, forecasting, and strategic planning efforts.",
        "Implemented Power BI and Excel-based reporting frameworks to monitor business performance and identify growth opportunities.",
        "Enhanced data governance procedures and validation processes to ensure high-quality financial and operational reporting.",
        "Collaborated with finance, sales, and operations to align analytics with organizational KPIs and performance benchmarks.",
        "Designed automation in SQL and VBA to reduce manual reporting effort and improve efficiency by 20%.",
        "Supported leadership in evaluating market expansion and pricing strategies using data-driven insights.",
    ]
)

add_experience(
    "Domino’s, Delhi, India", "Data Analytics Intern", "Aug 2016 – May 2017",
    [
        "Assisted in managing client databases, financial records, and reporting processes for startup clients across technology and retail sectors.",
        "Supported the design and testing of Tableau dashboards for client presentations and executive reviews.",
        "Conducted data cleansing, transformation, and validation to ensure data quality for reporting and analysis.",
        "Prepared financial and operational performance reports supporting client funding rounds and strategic decisions.",
        "Researched and documented SOPs for data collection and reporting workflows.",
    ]
)

# Certifications
add_section_title("Certifications")
add_bullets([
    "Microsoft Technology Associate — Exam 98-381",
    "MySQL for Data Analysis — Udemy",
])

# Save
doc.save("Gurdeep_Singh_Resume.docx")
print("Created Gurdeep_Singh_Resume.docx")

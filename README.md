
# Credit Card Financial Report Dashboard

## What did I do in this project?
1. Developed interactive dashboards using transaction and customer data from an SQL database to provide real-time insights.
2. Streamlined data processing and analysis to monitor key performance metrics and trends.
3. Shared actionable insights with stakeholders based on dashboard findings to support the decision-making process.

## Project Report

### Objective
To develop a comprehensive credit card weekly dashboard that provides real-time insights into key performance metrics and trends, enabling stakeholders to monitor and analyze credit card operations effectively.

### Data Collection
Data was collected from an online open-source platform. It was then imported into the SQL server using PostgreSQL. The SQL server was connected to Power BI, from which the data was imported into Power BI dashboards. If the SQL server data updates, the dashboard updates after refreshing the data in Power BI.

### DAX Queries
current_week_revenue = CALCULATE(
    SUM('public cc_detail'[revenue]),
    FILTER(
        ALL('public cc_detail'),
        'public cc_detail'[week_num2] = MAX('public cc_detail'[week_num2])
    )
)
prev_week_revenue = CALCULATE(
    SUM('public cc_detail'[revenue]),
    FILTER(
        ALL('public cc_detail'),
        'public cc_detail'[week_num2] = MAX('public cc_detail'[week_num2]) - 1
    )
)
wow_revenue = DIVIDE(([current_week_revenue] - [prev_week_revenue]), [prev_week_revenue])

### Dashboards
![Dashboard 1](https://github.com/lut-ful/Credit-Card-Financial-Report-Dashboard/assets/108027559/da23340a-aa76-48d2-857c-e3b036581ce8)
![Dashboard 2](https://github.com/lut-ful/Credit-Card-Financial-Report-Dashboard/assets/108027559/cb2c9d0d-41f8-4cb6-806d-dae290be41ae)
![Report Insights](https://github.com/lut-ful/Credit-Card-Financial-Report-Dashboard/assets/108027559/deb688d9-b4db-47f0-97ed-fd2938e2647b)

### Insights in Week 53
#### Week-on-Week Change
- Revenue increased by 28.8%
- Total transaction amount and volume increased by 35% and 3.4%, respectively
- Customer count increased by 12.8%

#### Year-to-Year Overview
- Overall revenue: 56.5 Million
- Total interest: 8 Million
- Total transaction amount: 45.5 Million
- Male customers contribute more to revenue
- Blue and Silver credit card holders contribute 93% of overall transactions
- TX, NY, and CA contribute 68% of total transactions
- Overall activation rate: 57.5%
- Overall delinquent rate: 6.06%

## Connect
- [LinkedIn](https://www.linkedin.com/in/mdlutfulkabir/)

---

Feel free to explore the [GitHub Repository](https://github.com/lut-ful/Credit-Card-Financial-Report-Dashboard) for more details and to view the full project.

# [Power BI] Bicycle Manufacturing Procurement KPI Tracking - Cost Control
## I. Introduction 
### Overview
This project utilizes the AdventureWorks dataset, a comprehensive database representing a fictional bicycle manufacturing company, to analyze business operations and extract insights. By focusing on procurement and cost control, we aim to enhance decision-making, improve efficiency, and boost profitability through data visualization and analysis tools.

### Dataset 


## II. Insights and Recommendations 
### Insights 

### Recommendations 

## III. Design Thinking Applying (Road to solve this problem) 
> Do phần này vừa được copy paste qua nên Cần chỉnh sửa lại nội dung cho đúng với project
### Step 1 - Empathize 
Applied 5W1H to define the problem

| 5W1H | Answer |
|-|-
| Who will use this dashboard? <br> -> Choose only one Stakeholder | Purchasing Dept. <br> -> **Purchasing Staff** | 
| What problem this dashboard will tackle? <br> -> Describe the problem in one sentence | Monitor work performance in real-time <br>Supervise purchasing activities <br>Control prices <br>Manage suppliers <br>Forecast production demand <br>Control and forecast inventory demand <br> -> **Managing price discrepancies and overseeing raw material purchasing activities (the return rate).** |
| When and where will Stakeholders view this Dashboard? | This dashboard can be view daily on the morning and during working time. |
| Why the Stakeholders need this dashboard? | It's essential to understand the department's current performance, ascertain if efficiency targets have been met, and verify if progress is on schedule. <br>Evaluate whether the timing and quantities of orders are optimized to minimize costs (shipping costs, production volumes, etc.). <br>Ensure inventory levels are optimized (avoiding excess or shortage) to meet production demand effectively.
| How have the Stakeholders been achieving their goals so far? | Analyze and compare the cost of product materials across various vendors throughout the month.

|EMPATHY MAP | |
|-|-|
| Pains |There is a lack of detailed work performance monitoring, making it difficult to identify if there are any issues in supplier management.
| Thinking and feeling |The team leader thinks that they need an efficient solution that enables the team to swiftly and effectively monitor and compare supplier pricing activities.
| Seeing |The team leader recognizes the potential to leverage existing data to compare the performance of various suppliers. This will provide insights into how different suppliers manage their logistics and determine if their proposed prices are competitive.
| Saying and doing |We require a report that allows for ongoing monitoring and comparison of supplier performance, and provides alerts if any supplier has pricing issues. <br> Action: Explore better tools and processes for data analysis
| Gains |Based on the report, the purchasing team can manage and collaborate with suppliers to ensure the company always acquires goods at optimal prices.

The Dataset 

|Fact table | Dim table |
|-|-
| 1. PurchaseOrderDetail <br>2. PurchaseOrderHeader | 1. Vendor <br>2. ProductVendor <br>3. Product <br>4. ProductTable <br>5. Dim_date

### Step 2 - Define POV 
Find the North star metric

| Questions | North star metric 1 | North star metric 2 
|-|-|- 
|What VALUE you want to measure?	|Revenue and Margin Profit | The products were actually sold without return |
|WHEN the value DELIVERY SUCCESS?	|When will the product bring profit to company? | When and Why the products was returned? |
|Northstar Metric Name	|% margin profit | % return rate |
|WHY do you choose this metric?	|For high-profit products, we can launch promotional programs in new markets while maintaining reasonable profit margins initially.| High profitability is irrelevant if a product has a high return rate.|

Dimension Data Group 

| Group 1 | Group 2 | Group 3 | Group 3 |
|-|-|-|-
|Product |Market, Regions |Sales Person analysis | Return rates 

| The Views | Description | Why |
|-|-|-
| Revenue, Profit and Growth rate by Years, Months | Business performance over the years, growth rate, revenue share by customers, market | How the company works over years 
| Product revenue, Return rates analysis | Mainly analyze sub-category, revenue, sales volume, and profit, return rate - which products are returned, and how is the proportion | gain valuable insights into your business's performance across different types of the products, allowing to make informed decisions to drive growth and profitability
| Region & Sales person analysis | How do different markets consume products, and what are the corresponding profits and return rates? | To understand the characteristics of each market, markets segmentation and performance of the sales persons of each market <br> This helps us gain insights into the new market where we plan to release the product and determine if it shares any similarities with the existing markets 


### Step 3 - Ideate 

| Idea name | Layer 0 dimension: <br> Total metric | Layer 1 dimension: <br> Breakdown the metric by 1 dimension | Layer 0 dimension: <br> Breakdown the metric by 2 dimension | Is there anything missed 
|-|-|-|-|-
| Revenue | Revenue, Profit | Revenue, Profit by yearly, monthly <br> % Growth rate by yearly, monthly |
| Product analysis | Return rate | Product revenue <br> Product profit <br> Product return rate | Revenue contribution by product <br> Product revuenue and return rate |
| Market, Region analysis | Return rate | Market revunue <br> Market profit <br> Segment revenue, profit | Revenue contribution by market <br> Segment revenue and return rate <br> Market profit and return rate | Sales persons performance 

Next, I moved on to Step 4 - Prototype and Review, iterating multiple times to refine the results. The final output will be showcased in the following section as a dashboard.

## IV. Dashboard 

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
| Who will use this dashboard? <br> -> Choose only one Stakeholder | Purchasing Dept. <br> -> Purchasing Staff | 
| What problem this dashboard will tackle? <br> -> Describe the problem in one sentence | Monitor work performance in real-time <br> Supervise purchasing activities <br> Control prices <br> Manage suppliers <br> Forecast production demand <br> Control and forecast inventory demand <br> -> **have a right decision on expansion stratergy base on data** |
| When and where will Stakeholders view this Dashboard? | This dashboard can be view weekly or monthly in the meeting. |
| Why the Stakeholders need this dashboard? | 1. To know how products have progressed in sales over the past period <br> 2. Identify products with potential for further development <br> 3. Determine which products should be improved or discontinued <br> 4. Gain an overall understanding of the business situation <br> 5. Have a basis for making decisions
| How have the Stakeholders been achieving their goals so far? | Investigate and research the impact of each product on revenue and profit, by region or by different times of the year.

|EMPATHY MAP | |
|-|-|
| Thinking and feeling |1. The sales manager believes that business performance is very good and that the company is operating smoothly. <br> 2. They believe there is potential for market development and expansion.
| Seeing |Sales manager sees potential for further development.
| Saying and doing |"We need more data-driven insights for the market expansion strategy" <br> Action: Explore better tools and processes for data analysis
| Pains |The manager sees a growth trend but is unsure if this trend reflects the entire market or all products. Is the growth due to a specific product, or is it because a particular market has increasing demand?
| Gains |What the stakeholder wants: <br> -> To use data to analyze overall performance and the details of each product. <br> -> To avoid bias in evaluations.

The Dataset 

|Fact table | Dim table |
|-|-
| orders | returns <br> people <br> date

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

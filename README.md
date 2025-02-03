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
|What VALUE you want to measure?	| Cost | Returned Product |
|WHEN the value DELIVERY SUCCESS?	|By optimizing purchasing costs, we can minimize unnecessary expenses. | When orders are delivered accurately, in full, and without any returns. |
|Northstar Metric Name	|% Cost difference ratio | % Perfect Order Ratio |
|WHY do you choose this metric?	|Optimizing purchasing costs can lead to a substantial improvement in sales profits.| To assess supplier performance, it is crucial to track frequent under-deliveries and defective goods, as these issues can greatly affect the company's time and expenses.|

Dimension Data Group 

| Group 1 | Group 2 | Group 3 
|-|-|-
|Cost components |Vendor's Product quantity | Vendor's Orders 
|Freight <br>Tax <br>Cost Discrepancy | OnOrdering Products <br>Delivered Products <br>Rejected Products | Total orders placed with suppliers. <br>Quantity of incorrectly delivered orders (either under-delivered or delivered in full but with defects).

| The Views | Description | Why |
|-|-|-
| Overview | Time: Within the last month <br>Provides a summary of activities for the past month | To analyze recent activities within the last month
| Vendor Evaluate | Detailed information on suppliers, categorized by reliability, average delivery time, and the discrepancy between proposed and actual costs. | To understand how each supplier operates, their delivery speed, and the differences between proposed and actual prices.
| Daily KPI tracking | Access detailed information about products, including stock levels, warnings for shortages, product prices, and identifying frequently returned products. | Monitor the status of purchased goods to ensure adequacy, create warnings, and track return rates. Excessive prices can also be used to assess whether the delivery issues are due to the supplier or the product itself.

### Step 3 - Ideate 

| Idea name | Layer 0 dimension: <br> Total metric | Layer 1 dimension: <br> Breakdown the metric by 1 dimension | Layer 2 dimension: <br> Breakdown the metric by 2 dimension | Is there anything missed 
|-|-|-|-|-
| Cost components analysis | Aggregate for a specified period | Breakdown of costs for each supplier | A comprehensive breakdown of each order component, including logistics costs, ordering fees, and storage fees.
| Vendor analysis | Perfect Orders ratio <br>Return ratio | Cost difference | Avg. Lead time |

Next, I moved on to Step 4 - Prototype and Review, iterating multiple times to refine the results. The final output will be showcased in the following section as a dashboard.

## IV. Dashboard 

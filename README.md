
![Adventureworks](https://github.com/user-attachments/assets/f4051290-f9a6-4982-bd26-93fd9ad815cf)

# 📊 Project Title: Bicycle Manufacturing Procurement KPI Tracking - Cost Control   
🤵 Author: [Tri Nguyen](https://www.linkedin.com/in/chilamviec/) <br> 
📆 Date: Dec. 12, 2024  <br> 
💻 Tools Used: Power BI

---

## 📑 Table of Contents  
1. [📌 Background & Overview](#-background--overview)  
2. [📂 Dataset Description & Data Structure](#-dataset-description--data-structure)  
3. [🧠 Design Thinking Process](#-design-thinking-process)  
4. [📊 Key Insights & Visualizations](#-key-insights--visualizations)  
5. [🔎 Final Conclusion & Recommendations](#-final-conclusion--recommendations)

---

## 📌 Background & Overview  

### Objective:
### 📖 What is this project about? 
 
- This project leverages the AdventureWorks dataset to analyze business operations and extract insights for a fictional bicycle manufacturing company.
- By focusing on procurement and cost control, it aims to enhance decision-making, improve efficiency, and boost profitability through data visualization and analysis tools.

### 👤 Who is this project for?  

The dashboard empowers **Purchasing Staffs** to efficiently manage costs, suppliers, and overall operations.

###  ❓Business Questions:  

- **Cost and Supplier Management**: How can Purchasing Staff efficiently manage costs, supplier relationships, and price discrepancies?
- **Performance and Efficiency Monitoring**: What strategies can be implemented to enhance performance monitoring and overall efficiency in purchasing operations?
- **Demand and Inventory Forecasting**: How can Purchasing Staff accurately forecast demand and manage inventory to ensure quality control and avoid shortages or excesses?

### 🎯Project Outcome:  
Summarize key findings and insights/ trends/ themes in a concise, bullet-point 
format.  

 _Example:_

✔️ Sales Trends: The top X% of products generate Y% of revenue.  
✔️ Inventory Optimization: Certain products are frequently out-of-stock, causing revenue loss.  
✔️ Customer Behavior: Returning customers spend Z% more per transaction than new customers.  

---

## 📂 Dataset Description & Data Structure  

### 📌 Data Source  
- Source: from [Microsoft sample database](https://learn.microsoft.com/en-us/sql/samples/adventureworks-install-configure?view=sql-server-ver16&tabs=ssms)
- Size: Over 121000 rows 
- Format: 
  <details>
  <summary>To access the dataset, follow these step</summary>
  
  - Access to the Microsoft sample database website.
  - Download version of database you want.
  - Import to SQL Server
  - Import to Power BI through SQL Server 
  
  </details>


### 📊 Data Structure & Relationships  

#### 1️⃣ Tables Used:  
Mention how many tables are in the dataset.  

#### 2️⃣ Table Schema & Data Snapshot  

Table 1: Products Table  

👉🏻 Insert a screenshot of table schema 

 _Example:_

| Column Name | Data Type | Description |  
|-------------|----------|-------------|  
| Product_ID  | INT      | Unique identifier for each product |  
| Name        | TEXT     | Product name |  
| Category    | TEXT     | Product category |  
| Price       | FLOAT    | Price per unit |  



Table 2: Sales Transactions  

👉🏻 Insert a screenshot of table schema 


 _Example:_

| Column Name    | Data Type | Description |  
|---------------|----------|-------------|  
| Transaction_ID | INT      | Unique identifier for each sale |  
| Product_ID     | INT      | Foreign key linking to Products table |  
| Quantity       | INT      | Number of items sold |  
| Sale_Date      | DATE     | Date of transaction |  



#### 3️⃣ Data Relationships:  
Describe the connections between tables—e.g., one-to-many, many-to-many.  

👉🏻 Include a screenshot of Data Modeling to visualize relationships.  

---

## 🧠 Design Thinking Process  

Explain the step-by-step approach taken to solve the problem.  

👉🏻 Insert a screenshot of the Design Thinking steps (Screenshot your Excel design thinking tables for better presentation).  

1️⃣ Empathize  
2️⃣ Define point of view  
3️⃣ Ideate  
4️⃣ Prototype and review  

---

## ⚒️ Main Process

1️⃣ Data Cleaning & Preprocessing  
2️⃣ Exploratory Data Analysis (EDA)  
3️⃣ SQL/ Python Analysis 

- In each step, show your Code

- Include query/ code execution screenshots or result samples

- Explain its purpose and its findings


4️⃣ Power BI Visualization  (applicable for PBI Projects)

---

## 📊 Key Insights & Visualizations  

### 🔍 Dashboard Preview  

#### 1️⃣ Dashboard 1 Preview  
👉🏻 Insert Power BI dashboard screenshots here  

📌 Analysis 1:  
- Observation: _Describe trends, key metrics, and patterns._  
- Recommendation: _Suggest actions based on insights._  

#### 2️⃣ Dashboard 2 Preview  
👉🏻 Insert Power BI dashboard screenshots here

📌 Analysis 2:   
- Observation: _Describe trends, key metrics, and patterns._  
- Recommendation: _Suggest actions based on insights._  

#### 3️⃣ Dashboard 3 Preview  
👉🏻 Insert Power BI dashboard screenshots here  

📌 Analysis 3:  
- Observation: _Describe trends, key metrics, and patterns._  
- Recommendation: _Suggest actions based on insights._  

---

## 🔎 Final Conclusion & Recommendations  

👉🏻 Based on the insights and findings above, we would recommend the [stakeholder team] to consider the following:  

📌 Key Takeaways:  
✔️ Recommendation 1  
✔️ Recommendation 2  
✔️ Recommendation 3






































































































# [Power BI] Bicycle Manufacturing Procurement KPI Tracking - Cost Control
## I. Introduction 
### Overview
This project utilizes the AdventureWorks dataset, a comprehensive database representing a fictional bicycle manufacturing company, to analyze business operations and extract insights. By focusing on procurement and cost control, we aim to enhance decision-making, improve efficiency, and boost profitability through data visualization and analysis tools.

### Dataset 
Dataset: adventureworks2019 (public Google BigQuery dataset)

Dataset dictionary: "Data Dictionary" (attached above)

Dataset access:

- Log in to your Google Cloud Platform account and create a new project.
- Navigate to the BigQuery console and select your newly created project.
- In the navigation panel, select "Add Data" and then "Star a project by name".


## II. Insights and Recommendations 
### Insights 

### Recommendations 

## III. Design Thinking Applying (Road to solve this problem) 
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
### Data modeling 
![image](https://github.com/user-attachments/assets/c29e6718-d46c-4809-9983-c30e12950ddf)

### View 1: PROCUREMENT OVERVIEW
![image](https://github.com/user-attachments/assets/efbd2c76-961e-4378-a9dc-021e589ffd91)
How to use: 

### View 2: PROCUREMENT DETAIL VIEW
![image](https://github.com/user-attachments/assets/72c01e33-2e58-45cb-9ae4-c3fa4f329f3d)
How to use: 


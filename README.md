
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

- **Improved Standard Order Ratio**: Supplier management strategies improved significantly from 2013 onwards, increasing and stabilizing the standard order rate to an average of over 90%.
- **Effective Cost Management**: The cost discrepancy level decreased from 5% in 2011 to 2% in 2013, showing effective cost management. The Superior group of vendors demonstrated the lowest cost discrepancy rate, at 4.3%, contributing to overall cost efficiency.

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
There are 6 tables were used in this project   

#### 2️⃣ Table Schema & Data Snapshot  

<details> 
<summary>Table 1: Product_Product </summary>

| Column Name             | DataType          | Description                                                                 |
|-------------------------|-------------------|-----------------------------------------------------------------------------|
| ProductID               | Integer           | Unique identifier for each product.                                         |
| Name                    | String            | The name of the product.                                                    |
| ProductNumber           | String            | A unique number assigned to each product.                                   |
| SafetyStockLevel        | Integer           | The minimum quantity of stock that must be kept on hand to prevent stockouts.|
| ReorderPoint            | Integer           | The inventory level at which a new order should be placed to replenish stock.|
| StandardCost            | Decimal           | The standard cost to produce or purchase the product.                       |
| ListPrice               | Decimal           | The price at which the product is listed for sale.                          |
| Style                   | String            | The style or category of the product.                                       |
| ProductSubcategoryID    | Integer           | Identifier for the subcategory to which the product belongs.                |
| SellStartDate           | Date              | The date when the product became available for sale.                        |
| SellEndDate             | Date              | The date when the product was no longer available for sale.                 |
| DiscontinuedDate        | Date              | The date when the product was discontinued.                                 |
| ModifiedDate            | Date              | The date when the product information was last modified.                    |

</details>

<details> 
<summary>Table 2: Product_ProductTable  </summary>

| Column Name            | DataType         | Description                                  |
|------------------------|------------------|----------------------------------------------|
| ProductID              | Integer          | Unique identifier for each product.          |
| Name                   | String           | The name of the product.                     |
| ProductCategoryID      | Integer          | Identifier for the category to which the product belongs. |
| ProductSubcategoryID   | Integer          | Identifier for the subcategory to which the product belongs. |
| Category               | String           | The category of the product.                 |
| Subcategory            | String           | The subcategory of the product.              |
 
</details>

<details> 
<summary>Table 3: Purchasing_OrderDetail </summary>

| Column Name            | DataType         | Description                                                            |
|------------------------|------------------|------------------------------------------------------------------------|
| PurchaseOrderID        | Integer          | Unique identifier for each purchase order.                             |
| PurchaseOrderDetailID  | Integer          | Unique identifier for each detail line within a purchase order.        |
| DueDate                | Date             | The date when the order is due to be received.                         |
| OrderQty               | Integer          | The quantity of items ordered.                                         |
| ProductID              | Integer          | Unique identifier for each product.                                    |
| UnitPrice              | Decimal          | The price per unit of the product ordered.                             |
| LineTotal              | Decimal          | The total cost for the line item (OrderQty * UnitPrice).               |
| ReceivedQty            | Integer          | The quantity of items actually received.                               |
| StockedQty             | Integer          | The quantity of items stocked.                                         |
| ModifiedDate           | Date             | The date when the purchase order detail was last modified.             |
| RejectedQty            | Integer          | The quantity of items that were rejected.                              |

</details>

<details> 
<summary>Table 4: Purchasing_OrderHeader  </summary> 

| Column Name         | DataType  | Description                                              |
|---------------------|-----------|----------------------------------------------------------|
| PurchaseOrderID     | Integer   | Unique identifier for each purchase order.               |
| RevisionNumber      | Integer   | The revision number of the purchase order.               |
| Status              | Integer   | The status of the purchase order.                        |
| EmployeeID          | Integer   | Identifier for the employee associated with the order.   |
| VendorID            | Integer   | Identifier for the vendor associated with the order.     |
| ShipMethodID        | Integer   | Identifier for the shipping method used for the order.   |
| OrderDate           | Date      | The date when the purchase order was created.            |
| ShipDate            | Date      | The date when the order is expected to be shipped.       |
| SubTotal            | Decimal   | The subtotal amount of the order.                        |
| TaxAmt              | Decimal   | The amount of tax applied to the order.                  |
| Freight             | Decimal   | The shipping cost associated with the order.             |
| TotalDue            | Decimal   | The total amount due for the order.                      |
| ModifiedDate        | Date      | The date when the purchase order was last modified.      |

</details>

<details> 
<summary>Table 5: Purchasing_ProductVendor  </summary>

| Column Name        | DataType  | Description                                        |
|--------------------|-----------|----------------------------------------------------|
| ProductID          | Integer   | Unique identifier for each product.                |
| BusinessEntityID   | Integer   | Unique identifier for each business entity.        |
| AverageLeadTime    | Integer   | The average lead time for the product.             |
| StandardPrice      | Decimal   | The standard price of the product.                 |
| LastReceiptCost    | Decimal   | The cost of the last receipt of the product.       |
| LastReceiptDate    | Date      | The date of the last receipt of the product.       |
| MinOrderQty        | Integer   | The minimum order quantity for the product.        |
| MaxOrderQty        | Integer   | The maximum order quantity for the product.        |
| OnOrderQty         | Integer   | The quantity of the product currently on order.    |
| ModifiedDate       | Date      | The date when the product information was last modified. |
| CostDiffRatio      | Decimal   | The cost difference ratio for the product.         |

</details>

<details> 
<summary>Table 6: Purchasing_Vendor  </summary>

| Column Name            | DataType         | Description                                                        |
|------------------------|------------------|--------------------------------------------------------------------|
| BusinessEntityID       | Integer          | Unique identifier for each business entity.                        |
| AccountNumber          | String           | The account number associated with the business entity.            |
| Name                   | String           | The name of the business entity.                                   |
| CreditRating           | Integer          | The credit rating of the business entity.                          |
| PreferredVendorStatus  | Boolean          | Indicates whether the vendor is a preferred vendor.                |
| ActiveFlag             | Boolean          | Indicates whether the business entity is active.                   |
| ModifiedDate           | Date             | The date when the business entity information was last modified.   |

</details>

#### 3️⃣ Data Relationships:  

![image](https://github.com/user-attachments/assets/c29e6718-d46c-4809-9983-c30e12950ddf)


## 🧠 Design Thinking Process  

1️⃣ Empathize  

➡️ Applied 5W1H to define the problem

| 5W1H | Answer |
|-|-
| Who will use this dashboard? <br> -> Choose only one Stakeholder | Purchasing Dept. <br> -> **Purchasing Staff** | 
| What problem this dashboard will tackle? <br> -> Describe the problem in one sentence | Monitor work performance in real-time <br>Supervise purchasing activities <br>Control prices <br>Manage suppliers <br>Forecast production demand <br>Control and forecast inventory demand <br> -> **Managing price discrepancies and overseeing raw material purchasing activities (the return rate).** |
| When and where will Stakeholders view this Dashboard? | This dashboard can be view daily on the morning and during working time. |
| Why the Stakeholders need this dashboard? | It's essential to understand the department's current performance, ascertain if efficiency targets have been met, and verify if progress is on schedule. <br>Evaluate whether the timing and quantities of orders are optimized to minimize costs (shipping costs, production volumes, etc.). <br>Ensure inventory levels are optimized (avoiding excess or shortage) to meet production demand effectively.
| How have the Stakeholders been achieving their goals so far? | Analyze and compare the cost of product materials across various vendors throughout the month.

➡️ Empathy Map for Stakeholders 

|EMPATHY MAP | |
|-|-|
| Pains |There is a lack of detailed work performance monitoring, making it difficult to identify if there are any issues in supplier management.
| Thinking and feeling |The team leader thinks that they need an efficient solution that enables the team to swiftly and effectively monitor and compare supplier pricing activities.
| Seeing |The team leader recognizes the potential to leverage existing data to compare the performance of various suppliers. This will provide insights into how different suppliers manage their logistics and determine if their proposed prices are competitive.
| Saying and doing |We require a report that allows for ongoing monitoring and comparison of supplier performance, and provides alerts if any supplier has pricing issues. <br> Action: Explore better tools and processes for data analysis
| Gains |Based on the report, the purchasing team can manage and collaborate with suppliers to ensure the company always acquires goods at optimal prices.

2️⃣ Define point of view  

➡️ Find the North star metric

| Questions | North star metric 1 | North star metric 2 
|-|-|- 
|What VALUE you want to measure?	| Cost | Returned Product |
|WHEN the value DELIVERY SUCCESS?	|By optimizing purchasing costs, we can minimize unnecessary expenses. | When orders are delivered accurately, in full, and without any returns. |
|Northstar Metric Name	|% Cost difference ratio | % Perfect Order Ratio |
|WHY do you choose this metric?	|Optimizing purchasing costs can lead to a substantial improvement in sales profits.| To assess supplier performance, it is crucial to track frequent under-deliveries and defective goods, as these issues can greatly affect the company's time and expenses.|

➡️ Dimension Data Group 

| Group 1 | Group 2 | Group 3 
|-|-|-
|Cost components |Vendor's Product quantity | Vendor's Orders 
|Freight <br>Tax <br>Cost Discrepancy | OnOrdering Products <br>Delivered Products <br>Rejected Products | Total orders placed with suppliers. <br>Quantity of incorrectly delivered orders (either under-delivered or delivered in full but with defects).

| The Views | Description | Why |
|-|-|-
| Overview | Time: Within the last month <br>Provides a summary of activities for the past month | To analyze recent activities within the last month
| Vendor Evaluate | Detailed information on suppliers, categorized by reliability, average delivery time, and the discrepancy between proposed and actual costs. | To understand how each supplier operates, their delivery speed, and the differences between proposed and actual prices.
| Daily KPI tracking | Access detailed information about products, including stock levels, warnings for shortages, product prices, and identifying frequently returned products. | Monitor the status of purchased goods to ensure adequacy, create warnings, and track return rates. Excessive prices can also be used to assess whether the delivery issues are due to the supplier or the product itself.

3️⃣ Ideate  

| Idea name | Layer 0 dimension: <br> Total metric | Layer 1 dimension: <br> Breakdown the metric by 1 dimension | Layer 2 dimension: <br> Breakdown the metric by 2 dimension | Is there anything missed 
|-|-|-|-|-
| Cost components analysis | Aggregate for a specified period | Breakdown of costs for each supplier | A comprehensive breakdown of each order component, including logistics costs, ordering fees, and storage fees.
| Vendor analysis | Perfect Orders ratio <br>Return ratio | Cost difference | Avg. Lead time |

4️⃣ Prototype and review  


## ⚒️ Main Process

1️⃣ Apply CodeM to create Dim_Date table 

| Column Name     | Description                            |
|-----------------|----------------------------------------|
| Date            | The specific date.                     |
| Year            | The year of the given date.            |
| Month           | The month of the given date.           |
| WeekofYear      | The week number within the year.       |
| WeekDay         | The day of the week for the given date.|

2️⃣ Apply DAX to calculate the metrics 

| Column Name            | Description                                                |
|------------------------|------------------------------------------------------------|
| %_Comp_TtlOrders       | Percentage of completed total orders.                      |
| %_Freight_Tcost        | Percentage of freight total cost.                          |
| %_Net_Tcost            | Percentage of net total cost.                              |
| %_perf_orders          | Percentage of performed orders.                            |
| %_Received_Ordered     | Percentage of received ordered items.                      |
| %_Rejected_Received    | Percentage of rejected received items.                     |
| %_Stocked_Qty          | Percentage of stocked quantity.                            |
| %_Tax_Tcost            | Percentage of tax total cost.                              |
| Comp_Orders            | Number of completed orders.                                |
| Cost_Freight           | Total cost of freight.                                     |
| Cost_Net               | Net cost.                                                  |
| Cost_Tax               | Total tax cost.                                            |
| Cost_total             | Total cost.                                                |
| Good_Orders            | Number of good orders.                                     |
| Perf_Orders            | Number of performed orders.                                |
| Qty_OnOrder            | Quantity of items on order.                                |
| Qty_Order              | Quantity of items ordered.                                 |
| Qty_Received           | Quantity of items received.                                |
| Qty_Rejected           | Quantity of items rejected.                                |
| Qty_Stocked            | Quantity of items stocked.                                 |
| Total_Order            | Total number of orders.                                    |
| Vendor_count           | Number of vendors.                                         |

3️⃣ Power BI Visualization  (applicable for PBI Projects)

📊 Dashboard 1: PROCUREMENT OVERVIEW 

![Screenshot 2025-02-13 005643](https://github.com/user-attachments/assets/ae87fa0a-5bdf-42b0-bb99-f77ebc12467d)

📊 Dashboard 2: PROCUREMENT DETAIL VIEW 

![Screenshot 2025-02-13 020812](https://github.com/user-attachments/assets/8a806788-a033-41fa-9bb0-a7cd16f4789e)

---

## 📊 Key Insights & Visualizations  

### 🔍 Dashboard Preview  

#### 1️⃣ Dashboard 1 Preview  

📌 Analysis 1:  

![image](https://github.com/user-attachments/assets/b22961ee-516a-40b7-86d2-1a020c849bfd)

- **Standard Order Rate:** During the period of 2011 and 2012, the standard order rate fluctuated significantly, indicating poor supplier management. However, from 2013 onwards, thanks to changes in supplier management strategies, this rate increased substantially and remained relatively stable, with the average standard order rate exceeding 90%.

📌 Analysis 2:  

![image](https://github.com/user-attachments/assets/c71f16cb-9d80-41c0-a312-88e01e216464)

- **Cost Discrepancy Level:** This is the rate between the supplier's calculated price and the final actual cost that the business must pay, reflecting the efficiency of cost management.
- The trend shows that this rate decreased from 5% in early 2011 to 2% in 2013, indicating effective and stable cost management strategies. However, the 2013-2014 period saw significant fluctuations due to macroeconomic policy changes and market conditions.

📌 Analysis 3:  

![image](https://github.com/user-attachments/assets/69d8fe9e-9c30-4241-8d23-114844c4b2f3)

- The data also shows that the Superior group are vendors with good cost management efficiency, with an average cost discrepancy rate of around 4.3%, the lowest among the groups. Prioritizing vendors from the Superior group, who always ensure minimal additional costs, proves to be a wise decision that brings effective cost management to the business.


## 🔎 Final Conclusion & Recommendations  

💡 Insights 

- The standard order rate showed significant fluctuations in 2011 and 2012 but improved dramatically and remained stable from 2013 onwards, with an average rate exceeding 90%, thanks to better supplier management strategies.
- The cost discrepancy level decreased from 5% in early 2011 to 2% in 2013, indicating effective cost management. The Superior group of vendors demonstrated good cost management efficiency, with an average discrepancy rate of 4.3%.
- Prioritizing vendors from the Superior group, who ensure minimal additional costs, proved to be a wise decision for effective cost management.
- In 2014, the company spent 43.5M USD, accounting for about 62% of the total material purchase costs over the four years, indicating thriving business efficiency and higher market demand for its products.
- The cost discrepancy rate in 2014 averaged around 0.5%, a record low, predicting a booming year for revenue and profit growth. Superior Bicycle and Chicago City Saddles maintained a 100% standard order rate, showcasing excellent logistics management.

📌 Key Takeaways:  

> To keep cost discrepancies low

- **Implement Robust Supplier Performance Metrics:** Regularly evaluate suppliers based on key performance indicators (KPIs) such as delivery time, quality of goods, and adherence to agreed prices. Maintain a performance scorecard to track and analyze these metrics.
- **Strengthen Supplier Relationships:** Foster strong partnerships with suppliers through regular communication, collaboration, and mutual trust. Building long-term relationships can lead to better negotiation of prices and terms, and enhanced overall performance.
- **Enhance Forecasting and Planning:** Utilize advanced forecasting tools and techniques to accurately predict demand and plan orders. This can help in minimizing rush orders and associated higher costs, ensuring better cost management.
- **Leverage Technology and Automation:** Invest in supply chain management software and automation tools to streamline processes, reduce manual errors, and improve efficiency. Automation can also help in tracking and managing costs more effectively.
- **Negotiate Better Contracts:** Negotiate contracts with clear terms and conditions, including penalties for non-compliance and incentives for excellent performance. Establishing a strong contractual framework can help in reducing cost discrepancies.
- **Conduct Regular Audits:** Perform regular audits of supplier invoices and internal processes to identify and rectify discrepancies. Audits help in maintaining transparency and accountability in cost management.
- **Diversify Supplier Base:** Avoid dependency on a single supplier by diversifying the supplier base. Having multiple reliable suppliers can ensure competitive pricing and mitigate risks associated with cost discrepancies.







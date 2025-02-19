
![16f357b7-c72b-4864-81ea-864ebbaba84c](https://github.com/user-attachments/assets/cdb1dca0-8c73-4724-80d1-a59ec5661ffd)

# 📊 Project Title: Stationery Retail Sales Data - Market Expansion Analysis  
🤵 Author: [Tri Nguyen](https://www.linkedin.com/in/chilamviec/) <br> 
📆 Date: Nov. 30, 2024  <br> 
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

- **Business Performance and Market Expansion:** The sales manager believes business performance is very good, sees potential for market development, and emphasizes the need for more data-driven insights for market expansion strategies.
- **Opportunities and Challenges:** The manager recognizes growth opportunities but is uncertain if the trend reflects the entire market or specific products. They aim to use data to analyze overall performance and avoid bias in evaluations.

### 👤 Who is this project for?  

➡️ **The Sales Manager** can make data-driven decisions on expansion strategies.

###  ❓Business Questions:  

- How can we leverage data-driven insights to enhance business performance and support market expansion?
- What are the specific growth opportunities, and do these trends accurately reflect the overall market or particular products?
- How can we ensure that our performance analysis remains unbiased and comprehensive while pursuing market development strategies?

### 🎯Project Outcome:  

- **Overall Business Performance**: The business shows strong growth with a Month-on-Month (MoM) growth rate of 4%. The average profit margin is 12%, and the successful order rate is approximately 95%.
- **Regional Insights**: APAC is the largest revenue contributor, while Canada has the smallest revenue share but the highest profit margins at 26.6%.
- **Customer Segments**: The Consumer group leads in revenue contribution, followed by the Corporate and Home Office groups. Profit margins across these segments are consistent, ranging from 11.8% to 12.6%.
- **Product Categories**: The Technologies category generates the most revenue, followed by Furniture and Office Suppliers. However, Table products within the Furniture group show negative profits and high return rates, indicating potential quality issues.

---

## 📂 Dataset Description & Data Structure  

### 📌 Data Source  
- Source: [🧷link to the dataset](https://drive.google.com/drive/folders/1oGbuHPBQECXKUcbhjuYOgk-ZH55Uau-g?usp=drive_link)
- Size: 51,291 rows 
- Format: .csv

### 📊 Data Structure & Relationships  

#### 1️⃣ Tables Used:  

There're: 
- 2 fact table: `Orders` and `Returns`
- 1 dim table: `People 

#### 2️⃣ Table Schema & Data Snapshot  

<details>
<summary>Table 1: Orders </summary>

| Column Name       | Data Type       | Description                                                                 |
|-------------------|-----------------|-----------------------------------------------------------------------------|
| Order ID          | int             | A unique identifier for each order.                                         |
| Order Date        | datetime        | The date when the order was placed.                                         |
| Ship Date         | datetime        | The date when the order was shipped.                                        |
| Ship Mode         | nvarchar(50)    | The method or mode of shipping used for the order.                          |
| Customer          | nvarchar(50)    | The name or identifier of the customer who placed the order.                |
| Customer Segment  | nvarchar(50)    | The segment or category to which the customer belongs.                      |
| City              | nvarchar(50)    | The city where the customer is located.                                     |
| State             | nvarchar(50)    | The state where the customer is located.                                    |
| Country           | nvarchar(50)    | The country where the customer is located.                                  |
| Postal Code       | nvarchar(20)    | The postal code of the customer's location.                                 |
| Market            | nvarchar(50)    | The market or region where the order was placed.                            |
| Region            | nvarchar(50)    | The specific region within the market where the order was placed.           |
| Product ID        | int             | A unique identifier for each product in the order.                          |
| Category          | nvarchar(50)    | The category to which the product belongs.                                  |
| Sub-Category      | nvarchar(50)    | The sub-category to which the product belongs.                              |
| Product Name      | nvarchar(100)   | The name of the product.                                                    |
| Sales             | money           | The total sales amount for the order.                                       |
| Quantity          | int             | The quantity of products ordered.                                           |
| Profit            | money           | The profit earned from the order.                                           |

</details>

<details>
<summary>Table 2: Returns</summary>

| Column Name  | Data Type | Description                        |
|--------------|-----------|------------------------------------|
| Returned     | bit       | Indicates if the order was returned. |
| Order ID     | int       | A unique identifier for each order. |

</details>

<details>
<summary>Table 3: People</summary> 

| Column Name       | Data Type        | Description                                                |
|-------------------|------------------|------------------------------------------------------------|
| Person            | nvarchar(255)    | The name of the person.                                    |
| Region            | nvarchar(255)    | The region where the person is located.                    |

</details>

#### 3️⃣ Data Relationships:  

![Screenshot 2025-02-12 134017](https://github.com/user-attachments/assets/eed00ddb-5d9d-4fe3-baaf-afb4c9666683)

---

## 🧠 Design Thinking Process  

1️⃣ Empathize  

➡️ Applied 5W1H to define the problem

![image](https://github.com/user-attachments/assets/f860d163-7ace-46c2-b8d7-f10ea5b6ff6d)

<!---
| 5W1H | Answer |
|-|-
| Who will use this dashboard? <br> -> Choose only one Stakeholder | R&D Dept., Sales Dept. <br> -> **Sales Manager** | 
| What problem this dashboard will tackle? <br> -> Describe the problem in one sentence | To understand which products have good or bad revenue/sales performance, compare similar products, show the impact of each region on revenue, and identify the customer groups that influence sales. <br> -> **have a right decision on expansion stratergy base on data** |
| When and where will Stakeholders view this Dashboard? | This dashboard can be view weekly or monthly in the meeting. |
| Why the Stakeholders need this dashboard? | 1. To know how products have progressed in sales over the past period <br> 2. Identify products with potential for further development <br> 3. Determine which products should be improved or discontinued <br> 4. Gain an overall understanding of the business situation <br> 5. Have a basis for making decisions
| How have the Stakeholders been achieving their goals so far? | Investigate and research the impact of each product on revenue and profit, by region or by different times of the year.
---> 

➡️ Empathy Map for Stakeholders 

![image](https://github.com/user-attachments/assets/d7c36e89-885b-4748-b6fa-87ed032aed30)

<!---
| Stakeholder Emotion| Detailed Description |
|-|-|
| Thinking and feeling |1. The sales manager believes that business performance is very good and that the company is operating smoothly. <br> 2. They believe there is potential for market development and expansion.
| Seeing |Sales manager sees potential for further development.
| Saying and doing |Saying: "We need more data-driven insights for the market expansion strategy" <br> Action: Explore better tools and processes for data analysis
| Pains |The manager sees a growth trend but is unsure if this trend reflects the entire market or all products. Is the growth due to a specific product, or is it because a particular market has increasing demand?
| Gains |What the stakeholder wants: <br> -> To use data to analyze overall performance and the details of each product. <br> -> To avoid bias in evaluations.
---> 

2️⃣ Define point of view  

➡️ Find the North star metric

![image](https://github.com/user-attachments/assets/32acd6fb-36cb-4a12-be2f-e1df2ee420eb)

<!---
| Questions | North star metric 1 | North star metric 2 
|-|-|- 
|What VALUE you want to measure?	|Revenue and Margin Profit | The products were actually sold without return |
|WHEN the value DELIVERY SUCCESS?	|When will the product bring profit to company? | When and Why the products was returned? |
|Northstar Metric Name	|% margin profit | % return rate |
|WHY do you choose this metric?	|For high-profit products, we can launch promotional programs in new markets while maintaining reasonable profit margins initially.| High profitability is irrelevant if a product has a high return rate.|
---> 

➡️ Dimension Data Group 

![image](https://github.com/user-attachments/assets/a2701ec3-d3ca-47b0-872f-a09abe62f612)

<!---
| Group 1 | Group 2 | Group 3 | Group 3 |
|-|-|-|-
|Product |Market, Regions |Sales Person analysis | Return rates 
--->

![image](https://github.com/user-attachments/assets/f8458ad6-6777-4a4d-b25b-d945c2b58fcc)

<!---
| The Views | Description | Why |
|-|-|-
| Revenue, Profit and Growth rate by Years, Months | Business performance over the years, growth rate, revenue share by customers, market | How the company works over years 
| Product revenue, Return rates analysis | Mainly analyze sub-category, revenue, sales volume, and profit, return rate - which products are returned, and how is the proportion | gain valuable insights into your business's performance across different types of the products, allowing to make informed decisions to drive growth and profitability
| Region & Sales person analysis | How do different markets consume products, and what are the corresponding profits and return rates? | To understand the characteristics of each market, markets segmentation and performance of the sales persons of each market <br> This helps us gain insights into the new market where we plan to release the product and determine if it shares any similarities with the existing markets 
---> 

3️⃣ Ideate  

![image](https://github.com/user-attachments/assets/b58d7dd9-9d86-4e66-8f0d-f755507b2abf)

<!---
| Idea name | Layer 0 dimension: <br> Total metric | Layer 1 dimension: <br> Breakdown the metric by 1 dimension | Layer 0 dimension: <br> Breakdown the metric by 2 dimension | Is there anything missed 
|-|-|-|-|-
| Revenue | Revenue, Profit | Revenue, Profit by yearly, monthly <br> % Growth rate by yearly, monthly |
| Product analysis | Return rate | Product revenue <br> Product profit <br> Product return rate | Revenue contribution by product <br> Product revuenue and return rate |
| Market, Region analysis | Return rate | Market revunue <br> Market profit <br> Segment revenue, profit | Revenue contribution by market <br> Segment revenue and return rate <br> Market profit and return rate | Sales persons performance 
---> 

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

| _Calculation      | Description                              |
|-------------------|------------------------------------------|
| %margin_profit    | Percentage of margin profit              |
| %MoM_profit_rate  | Month-over-Month profit rate             |
| %MoM_revenue      | Month-over-Month revenue                 |
| %return_rates     | Percentage of return rates               |
| orders_count      | Number of orders                         |
| price_per_1item   | Price per one item                       |
| profit_per_1item  | Profit per one item                      |
| returns_count     | Number of returns                        |
| total_profit      | Total profit                             |
| total_quantity    | Total quantity of items                  |
| total_revenue     | Total revenue                            |

3️⃣ Power BI Visualization  (applicable for PBI Projects)

📊 Dashboard 1: Overview   

![image](https://github.com/user-attachments/assets/453a3570-e431-4132-a99c-df54d1a86eda)

📊 Dashboard 2: Market Analysis 

![image](https://github.com/user-attachments/assets/011c7851-f12f-4103-92c9-fde752388046)

📊 Dashboard 3: Product Analysis

![image](https://github.com/user-attachments/assets/1d6c5224-8496-48b2-b1b0-cf0047cd25f6)

---

## 📊 Key Insights & Visualizations  

### 🔍 Dashboard Preview  

#### 1️⃣ Overall trend    

![image](https://github.com/user-attachments/assets/d9428b22-ca1c-441f-aa66-77e7c4babc08)

📌 Analysis 1:  
- Observation:
  - Consistent Revenue Growth - Revenue shows a consistent upward trend, highlighting a positive growth trajectory.
  - Stable, Low Profit - Profit remains flat, suggesting challenges in managing costs or heavy reinvestment.
- Recommendation: _Suggest actions based on insights._
  - Focus on Cost Optimization - Identify and implement strategies to reduce operational costs and improve profit margins.
  - Seasonal Strategy - Leverage seasonal patterns for marketing and resource allocation to maximize peak periods and mitigate dips.

#### 2️⃣ Markets' and Product Categories' contribution  

![image](https://github.com/user-attachments/assets/ae703d05-6c0f-4daf-b267-b61b0a4257f9)

📌 Analysis 2:   
- Observation: 
  - The APAC market tops revenue and profit, indicating strong performance.
  - The Consumer segment shows the highest revenue and profit among all segments.
  - Technology products are the top contributer. 
- Recommendation: _Suggest actions based on insights._  
  - Prioritize market expansion and tailored strategies in the APAC region.
  - Invest in consumer-targeted products and marketing efforts.
#### 3️⃣ Regions

![image](https://github.com/user-attachments/assets/a98c9235-6478-4d19-a3c9-ddbefa674bd0)
![image](https://github.com/user-attachments/assets/400afd23-3acf-4c3a-b877-8a283ce780a7)

📌 Analysis 3:  
- Observation: 
  - The Central Region leads in overall market revenue, with a below-average return rate of 4.8%. It also has a monthly growth rate of 4.6%, which is higher than the overall average, indicating an effective sales strategy.
- Recommendation:
  - Develop a new marketing strategy for this region to enhance and maintain customer loyalty. 

#### 4️⃣ Product 

![image](https://github.com/user-attachments/assets/8feb0468-45c4-4a29-a6e4-68cc2e707a41)

📌 Analysis 4:  
- Observation: 
  - Phones, Chairs, and Copiers lead in revenue and overall show good profit, whereas Tables exhibit a negative profit.
- Recommendation:
  - Enhance the quality and durability of tables to attract more customers, increase satisfaction, and reduce return rates.
 
#### 5️⃣ Top 5 Products 

![image](https://github.com/user-attachments/assets/60e8377b-6036-4c35-a3cd-390c3e7f280f)

📌 Analysis 5:  
- Observation: 
  - The top 5 products with the highest order counts indicate high customer demand and good quality.
  - The top 5 products with the highest return rates suggest issues with product quality or marketing, leading to misunderstandings about product usage.
- Recommendation:
  - Leverage high-demand products for market expansion with targeted marketing efforts.
  - Address quality issues and improve product descriptions to reduce high return rates. 

---

## 🔎 Final Conclusion & Recommendations  

- **Business Growth and Performance:** The business shows robust growth with a 4% Month-on-Month (MoM) growth rate, an average profit margin of 12%, and a successful order rate of approximately 95%.

- **Regional and Market Insights:** APAC is the largest revenue contributor, while Canada has the smallest revenue share but the highest profit margins at 26.6%.

- **Customer Segments and Product Performance:** The Consumer group leads in revenue contribution among customer segments, and the Technologies category generates the most revenue. However, Table products within the Furniture group show negative profits and a high return rate, indicating potential quality issues.

<!---
- The business demonstrates robust growth, with a Month-on-Month (MoM) **growth rate of about 4%**. The **average profit margin stands at 12%**, and the **successful order rate is approximately 95%**. <br> 
- APAC is currently the largest contributor to revenue, while Canada is the smallest. However, **the profit margins from the Canadian market** are significantly higher compared to other markets **(26.6%)**. <br> 
- Among customer segments, the Consumer group leads in revenue contribution, followed by the Cooperate and Home Office groups. Profit margins across these segments are fairly consistent, ranging from 11.8% to 12.6%. <br> 
- Products in the Technologies category lead in revenue generation, followed by Furniture and Office Suppliers, all contributing relatively evenly. However, Table products within the Furniture group show negative profits and a high return rate, suggesting potential quality issues.
--->

| Market | Insights | Recommendations 
|-|-|- 
| **APAC** | The APAC market leads in revenue contribution with a solid **profit margin of 12%**. The return rate stands at 5.5%, which is not excessively high. The top-selling products in this market include Chairs, Bookcases, Copiers, and Phones. | Ensuring consistent high-quality customer service is key. <br> Provide responsive support and resolve issues quickly to build trust and satisfaction. <br> Special promotions and discounts during holidays can attract and retain customers. <br> Build strong relationships through regular communication and feedback collection. Implement loyalty programs to reward repeat customers and encourage loyalty. Invest in marketing efforts to maintain brand recognition and visibility.
| **EU** | The market ranks 2nd in revenue contribution with a **solid profit margin of 12%**. However, it also has the highest **return rate at 6.2%** and a **low order success rate of under 94%**. Products like Appliances, Accessories, Copiers, and Fasteners have notably high return rates. The most frequently returned items are Copiers, Bookcases, Phones, Storage, and Appliances. | Implement strict quality control measures to ensure products meet the expected standards before they are shipped to customers. <br> Regularly gather and analyze feedback to identify common reasons for returns. <br> Provide detailed and accurate product descriptions, including specifications, dimensions, features, and high-quality images.
| **US** | The market ranks 3rd in revenue contribution, with a relatively **good profit margin of 12%**. However, it has a **return rate of 6%**, primarily in the Machines product category, which has a very low total order volume. Phones and Chairs are the top revenue contributors, significantly outpacing other product categories. Besides Tables, Bookcases and Supplies also have **negative profit margins**. | Regularly gather and analyze customer feedback to identify common reasons for returns and address them promptly. Provide excellent pre- and post-purchase customer support to address any issues promptly. <br> Ensure that all products, particularly those with high return rates, meet stringent quality standards to minimize defects and dissatisfaction. <br> Regularly review and optimize operational costs, including sourcing, manufacturing, and logistics, to improve profit margins without compromising quality. 
| **LATAM** | The market ranks 4th in revenue contribution, with a **modest profit margin of 10%** and a **return rate of 5.8%**. Top revenue and profit-contributing product categories include Bookcases, Chairs, Phones, and Copiers. However, **Tables have a negative profit margin and a high return rate of 10%**. | Focus on promoting and expanding the product categories that contribute the most to revenue and profit. Offer bundled deals on popular products to encourage higher sales volumes. <br> Invest in targeted digital marketing campaigns to reach a broader audience. <br> Train sales teams to upsell and cross-sell complementary products, increasing the average order value.
| **AFRICA** | The market ranks 5th, just above Canada, with a **modest profit margin of 10%**. The order **success rate is at 100%**, indicating a slow consumption rate for products. Customers in this market typically purchase essential items and use them for extended periods, rarely needing upgrades. The top consumed products are Storage, Machines, Phones, Appliances, Bookcases, and Copiers.  | Offer bundled deals on popular essential products. Introduce time-limited promotions and discounts to encourage customers to upgrade their essential products more frequently
| **CANADA** | Canadian market contributes the least to revenue but **boasts an exceptionally high profit margin of 26%** and a **100% order success rate**, indicating high customer satisfaction. This market tends to favor essential products such as Storage, Accessories, Phones, Appliances, Bookcases, and Copiers. | Launch tailored marketing campaigns to increase brand awareness and attract new customers. Implement referral programs where existing customers can refer friends and family in exchange for discounts or rewards. <br> Partner with other brands or local influencers to co-promote products and reach new customer segments. <br> Conduct regular market research to identify new opportunities and understand the evolving needs and preferences of your target audience.

















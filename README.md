# [Power BI] Stationery Retail Sales Data - Market Expansion Analysis 
## I. Introduction 
### Overview
This Power BI project aims to analyze the market and product performance to identify opportunities for expanding into new markets. By leveraging data visualization and analysis tools, we will examine key metrics such as market trends, customer demographics, product performance, and competitive landscape. The insights gained from this analysis will inform strategic decisions, enhance market positioning, and drive business growth. Ultimately, this project will enable us to identify new market opportunities, optimize product offerings, and expand our market presence effectively.

### Dataset 
[🧷link to the dataset](https://drive.google.com/drive/folders/1oGbuHPBQECXKUcbhjuYOgk-ZH55Uau-g?usp=drive_link)

## II. Insights and Recommendations 
### Insights
The company's sales revenue has demonstrated a significant upward trend, **growing from approximately 99 million in January 2011 to over 503 million in December 2014**, with an **average monthly growth rate of 10.2%**. This impressive growth indicates strong market demand and effective sales strategies. In analyzing product categories:

- **Furniture**: Although not the top-selling category, Furniture, particularly Chairs, shows notable potential for growth. This suggests an opportunity to capitalize on the increasing demand for home and office furniture.
- **Office Supplies**: This category, especially the Storage and Appliance groups, has high sales but also high return rates. This indicates a need to improve product quality and customer satisfaction to reduce returns and enhance profitability.
- **Technologies**: Phones and Copiers in this category exhibit strong sales and low return rates, making them highly profitable. This suggests focusing on these products can drive sustained growth and revenue.

### Recommendations 

- **APAC Region**: With the highest sales and lowest return rates, this region presents a prime opportunity for expansion. Focus on increasing market penetration and brand presence to capitalize on the existing demand.
- **EMEA Region**: Despite high return rates, this region offers significant revenue potential. Implementing strategies to improve product quality and customer experience can help tap into this market's full potential.
- **Africa and Canada**: Africa shows steady sales growth, while Canada has the lowest sales. Tailored strategies focusing on product appeal and customer satisfaction can drive growth in these regions. For example, in Africa, enhance marketing efforts and in Canada, introduce products that meet specific market needs.
- **Product Focus**: Emphasize products with high profitability and low return rates, like Phones and Copiers, to drive revenue. Additionally, improve customer experience for high-return items like Storage and Appliances to increase overall satisfaction and reduce returns.

## III. Design Thinking Applying 
### Step 1 - Empathize 
Applied 5W1H to define the problem

| 5W1H | Answer |
|-|-
| Who will use this dashboard? <br> -> Choose only one Stakeholder | R&D Dept., Sales Dept. <br> -> **Sales Manager** | 
| What problem this dashboard will tackle? <br> -> Describe the problem in one sentence | To understand which products have good or bad revenue/sales performance, compare similar products, show the impact of each region on revenue, and identify the customer groups that influence sales. <br> -> **have a right decision on expansion stratergy base on data** |
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

### Data modeling 
![Screenshot 2025-01-20 140051](https://github.com/user-attachments/assets/e647642b-03e2-4215-8e07-4754f74cabb1)

### View 1: Overview 
![Screenshot 2025-01-20 140104](https://github.com/user-attachments/assets/1afc2199-3149-49f9-81a1-aae40e6cd43f)
How to use: 

### View 2: Product Analysis
![Screenshot 2025-01-20 140152](https://github.com/user-attachments/assets/9548ce2a-d680-49b8-83a8-8a3ee28dc835)
How to use: 

### View 3: Market Analysis
![Screenshot 2025-01-20 140207](https://github.com/user-attachments/assets/27999c95-2586-4e54-a6a1-64fa2c2e09e1)
How to use: 








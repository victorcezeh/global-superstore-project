# Global Superstore Project

![Global Store](https://images.pexels.com/photos/1797428/pexels-photo-1797428.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1)


## Table of Contents

- [Brief](#Brief)
- [Objective](#Objective)
- [Dataset and spreadsheet explanation](#Dataset-and-spreadsheet-explanation)
  - [Order Sheet](#Order-Sheet)
  - [Returns Sheet](#Returns-Sheet)
  - [People Sheet](#People-Sheet)
- [Data cleaning and importation into MySQL Workbench](#Data-cleaning-and-importation-into-MySQL-Workbench)
- [Case study business questions and answers](#Case-study-business-questions-and-answers)
- [Tools Used](#Tools-Used)
- [Skillset Applied](#Skillset-Applied)
- [Project Structure](#Project-Structure)
- [Acknowledgement](#Acknowledgement)


## Brief
Global Superstore is a global online retailer based in New York, boasting a broad product catalogue and aiming to be a one-stop-shop for its customers globally. The superstore’s clientele, hailing from 147 different countries can browse through an endless offering with more than 10,000 products. This large selection comprises three main categories: `office` `supplies` (e.g. staples), `furniture` (e.g. chairs), and `technology` (e.g. smartphones). I have been contracted as a Data Analyst to help Global Superstore analyze and draw out meaningful insight from the Superstore dataset which would aid management in making informed decisions to improve performance and profitability.



## Objective

#### The objective of this project is to analyze the dataset and provide answers to the following business questions.

- Question 1
  - What are the 3 countries that generated the highest total profit for Global Superstore in 2014?
  - For each of these three countries, find the three products with the highest total profit. Specifically, what are the products’ names and the total profit for each product?

- Question 2
  - Identify the 3 subcategories with the highest average shipping cost in the United States.

- Question 3
  - Assess Nigeria’s profitability (i.e., total profit) for 2014. How does it compare to other African countries?
  - What factors might be responsible for Nigeria’s poor performance?

- Question 4
  - Identify the product subcategory that is the least profitable in Southeast Asia. Note: For this question, there is an assumption that Southeast Asia comprises Cambodia, Indonesia,       Malaysia, Myanmar(Burma), the Philippines, Singapore, Thailand, and Vietnam.
  - Is there a specific country in Southeast Asia where Global Superstore should stop offering the subcategory identified in the first part of this question?
 
- Question 5
  - Which city is the least profitable (in terms of average profit) in the United States? For this analysis, I discard the cities with less than 10 Orders.
  - Why is this city’s average profit so low?

- Question 6
  - Which product subcategory has the highest average profit in Australia?
 
- Question 7
  - Which customer returned items and what segment do they belong
  - Who are the most valuable customers and what do they purchase?
    
 

#### This project documentation contains screenshots of data visualization as a means to interpret and easily read results gotten from my analysis. It also contains SQL scripts that helped derive and drive my decison making process in this project.
 



## Dataset and spreadsheet explanation

The dataset for this project is presented in an unstandardized Excel spreadsheet format. It contains 3 different but related spreadsheets. These spreadsheets are:


- #### Order Sheet
- #### Returns Sheet &
- #### Peoples Sheet




I will explain the details of these sheets one after the other.




#### Order Sheet

This spreadsheet contains data of orders made by customers. The columns in this sheet consist of the following:

- `Row ID`: This represents a general identifier for the row within the spreadsheet.
  
- `Order ID`: This represents the unique identifier for each order purchased.
  
- `Order Date`: This represents a date tracker. It is data used to track when orders were placed.
  
- `Ship Date`: This refers to the date on which goods or products are shipped or sent out for delivery to the customers.
  
- `Ship Mode`: This refers to the method or mode of transportation used to deliver products from the seller or supplier to the customers.

- `Customer ID`: This represents a unique identifier assigned to each customer. This identifier is used to distinguish one customer from another.

- `Customer Name`: This refers to the name of the individual or entity that has placed an order.

- `Segment`: This refers to the category/division used to classify and organize orders based on certain criteria.

- `City`: This field contains data about the city associated with each order.

- `State`: This field contains data about the state associated with each order.

- `Country`: This field contains data about the country associated with each order.

- `Postal Code`: This refers to a series of letters, numbers, or both, that are used in a mailing address to facilitate the sorting and delivery of mail. In the context of an order                       spreadsheet, the Postal Code information allows businesses to perform detailed analyses related to geographic locations, such as assessing shipping costs, optimizing                     delivery routes, and understanding customer distribution. Additionally, it can be beneficial for compliance with shipping and mailing requirements. NB: Not all postal                    code data was available at the time of analysis.
  
- `Market`: This represents the geographic region associated with each order, such as the United States (US), Asia-Pacific (APAC), or Europe, Middle East, and Africa (EMEA).

- `Region`: This field represents a specific region or area associated with each order. Similar to the "Market" column, the "Region" column helps categorize orders based on broader                  geographic areas within which a business operates or wants to analyze performance.

- `Product ID`: This field serves as a unique identifier for each product. The Product ID is used to uniquely identify and distinguish different products within the dataset. Each                        product in this inventory or catalog would have its own unique Product ID.

- `Category`: This field categorizes each product into a broader group or classification. The "Category" column helps organize and analyze products based on common characteristics,                    features, or functions.

- `Sub-Category`: This field provides a more detailed classification of each product within a broader category. While the "Category" column groups products into high-level categories,                     the "Sub-Category" column adds another layer of granularity by further specifying the type or variant of each product.

- `Product Name`: This field refers to the specific names or labels of the products being sold.

- `Sales`: This field contains data of the total revenue generated from each order. The "Sales" column is calculated by multiplying the "Quantity" of each product by its corresponding              "Price."

- `Quantity`: This field represents the number of units or items of a particular product ordered in each transaction. The "Quantity" column indicates the quantity of each product                      associated with a specific order.

- `Discount`: This column captures the amount of price reduction applied to each product or order. The "Discount" column is used to record any discounts or promotional reductions in the               total price for specific products or the entire order.

- `Profit`: This column represents the financial gain or loss associated with each order or product.

- `Shipping Cost`: This column captures the cost associated with shipping each order. The "Shipping Cost" column includes the expenses incurred for delivering the products to the                           customers. This cost may cover transportation, packaging, handling, and any other logistics-related expenses.

- `Order Priority`: This field represents the priority level assigned to each order. The "Order Priority" column helps categorize orders based on their importance, urgency, or specific                      criteria determined by the business.



#### Returns Sheet

This spreadsheet tracks and manages product returns. The columns in this sheet consist of the following:

- `Returned`: This refers to items that customers have sent back to the seller or business as part of a product return process. When a customer is dissatisfied with a product, receives                a defective item, or simply changes their mind, they may initiate a return to the seller. The returned items are then tracked and managed in the return spreadsheet.

- `Order-ID`: This refers to a unique identifier assigned to a specific order when it was originally placed by a customer. The Order-ID is used to associate all relevant information and               details about that particular order, including the items purchased, customer details, and other transaction-related information.

- `Market`: This represents the geographic region associated with each order when it was originally placed by a customer, such as the United States (US), Asia-Pacific (APAC), or Europe,             Middle East, and Africa (EMEA).




#### People Sheet

This contains information about individuals (employees) and their associated regions. The columns in this sheet consist of the following:

- `People`: This column contains information about individual employees.
  
- `Region`: This refers to broader geographical location or area where the employee is located. This information is useful for organizational planning, management, and understanding the             distribution of employees across different locations.


## Data cleaning and importation into MySQL Workbench

In the course of trying to clean the data using Excel, I realised it was already a clean data when collected from the source. I checked for data duplicates and spelling errors and found nothing. I went ahead to standardize the Excel spreadsheet, seperate the `Orders`, `Returns` and `People` sheets and covert them into CSV formats for easy data importation into MySQL Workbench using Table Data Import Wizard on MySQL Workbench.


#### Orders Table on Excel

![Orders Table on Excel](https://github.com/victorcezeh/Global_Superstore_Project/assets/129629266/83c9a798-208b-4be9-8a4d-16a453280468)


#### Returns Table on Excel

![Returns Table on Excel](https://github.com/victorcezeh/Global_Superstore_Project/assets/129629266/9192d9d1-ae1f-4414-89d1-b628c8d523cc)


#### People Table on Excel

![People Table on Excel](https://github.com/victorcezeh/Global_Superstore_Project/assets/129629266/cc4a7380-ddcf-4699-8f26-bccb0b48b2cc)


#### Orders Table on MySQL Workbench after converting Excel format to CSV and importing into MySQL

![Orders Table on MySQL Workbench](https://github.com/victorcezeh/Global_Superstore_Project/assets/129629266/3b2d7291-290e-4615-8361-dbf7d2fb5528)


#### Returns Table on MySQL Workbench after converting Excel format to CSV and importing into MySQL

![Returns Table on MySQL Workbench](https://github.com/victorcezeh/Global_Superstore_Project/assets/129629266/2b072ce3-3aba-467a-bc89-db1b19a29c4f)


#### People Table on MySQL Workbench after converting Excel format to CSV and importing into MySQL

![People Table on MySQL Workbench](https://github.com/victorcezeh/Global_Superstore_Project/assets/129629266/ac05d757-97c0-4feb-b618-af75525c8881)




## Case study business questions and answers


- #### What are the 3 countries that generated the highest total profit for Global Superstore in 2014?

![ 3 countries that generated the highest total profit for Global Superstore in 2014](https://github.com/victorcezeh/Global_Superstore_Project/assets/129629266/d8ccada9-52e9-4f88-a46f-360108542372)

- #### In 2014, the 3 countries that generated the highest total profit for Global Superstore are:
1.	United States with $93,508
2.	India with $48,808
3.	China with $46,794


- #### For each of these three countries, find the three products with the highest total profit. Specifically, what are the products’ names and the total profit for each product?

![3 products, each country](https://github.com/victorcezeh/Global_Superstore_Project/assets/129629266/4e35e7b2-acfa-4749-8bb8-0cd8004affa1)

- #### The 3 products with the highest total profit, the products’ names and the total profit for each product are:
  
- #### The 3 products in United States:

1. Canon Image Class 2200 Advanced Copier with $14,560

2. Fellowes PB500 Electric Punch Plastic Comb Binding Machine with Manual Bind with $7,626

3. Hewlett Packard LaserJet 3310 Copier with $6,984

- #### The 3 products in India:
  
1. Apple Smart Phone, with Caller ID with $2,818

2. Sauder Classic Bookcase, Traditional $2,420

3. Hewlett Wireless Fax, Color with $1,465

- #### The 3 products in China:
  
1. Office Star Executive Leather Armchair, Black with $2,636

2. Sharp Wireless Fax, Digital with $2,368

3. Bush Classic Bookcase, Mobile with $2,267



- #### Identify the 3 subcategories with the highest average shipping cost in the United States.

```sql
-- Identify the 3 subcategories with the highest average shipping cost in the United States.
SELECT
  sub_category,
  country,
  (AVG (shipping_cost)) as average_shipping_cost_US
FROM vephlaproject.orders
WHERE country = 'United States'
GROUP BY sub_category
ORDER BY 3 DESC
LIMIT 3;

```

#### Output

The result of the query above was exported as a table in Excel format, standardized and visualized using Power BI.

![average shippping cost United States](https://github.com/victorcezeh/Global_Superstore_Project/assets/129629266/3ac1f379-9535-4b1f-a5c7-47fcf7433505)




![average shippping cost United States_Viz](https://github.com/victorcezeh/Global_Superstore_Project/assets/129629266/c8173c6b-bbee-4013-a2cd-69fc5145242f)




#### The 3 subcategories with the highest average shipping cost in the United States are:

1. Copiers with $165
2. Machines with $132
3. Tables with $70


- #### Assess Nigeria’s profitability (i.e., total profit) for 2014. How does it compare to other African countries?

```sql
-- Select African Region
SELECT
  country,
  profit
FROM vephlaproject.orders
WHERE Region = 'Africa';

```

#### Output

The result of the query above was exported as a table in Excel format, standardized and visualized using Power BI.

![Nigeria’s Profitability)](https://github.com/victorcezeh/Global_Superstore_Project/assets/129629266/04e7f362-0ae6-4cb8-a079-16a4c85fe626)


![Nigeria’s Profitability Viz](https://github.com/victorcezeh/Global_Superstore_Project/assets/129629266/915edde4-ce97-44e7-94fb-888fb1c547f8)



#### Nigeria’s profitability/total profit for 2014 and how it compares to other African countries.

In 2014, Nigeria made a loss of -$9,753. Nigeria lost the most money in the African region in that same year just after Zimbabwe who made a loss of -$1,404. On the other hand, South Africa, Morocco, Egypt and Republic of Congo made the most profit with $7,242, $6,274, $4,774 and $4,228 respectively in 2014.


#### What factors might be responsible for Nigeria’s poor performance?


```sql
-- Sum up Nigeria Shipping Cost 
SELECT
  SUM(shipping_cost) as shipping_cost,
  country,
  region
FROM vephlaproject.orders
WHERE country = 'Nigeria';

-- Find average discount in Nigeria
SELECT
  AVG(discount) as average_discount,
  country,
  region
FROM vephlaproject.orders
WHERE country = 'Nigeria';

```

The result of the query above was exported as a table in Excel format, standardized and visualized using Power BI.

#### Output

![Shipping Cost)](https://github.com/victorcezeh/Global_Superstore_Project/assets/129629266/70da84ff-e576-4a06-b99c-513fe33c6a08)


![Average Discount)](https://github.com/victorcezeh/Global_Superstore_Project/assets/129629266/aa5ced43-da84-4df7-97fa-5c21753c8ded)


![Shipping Cost & Average Discount Viz)](https://github.com/victorcezeh/Global_Superstore_Project/assets/129629266/e3bf2aa8-17c9-48da-9108-f3de0b2fd417)



Factors that might be responsible for Nigeria’s poor performance could be its shipping cost and average discount.

1. Shipping Cost: $6,183.11
2. Average Discount: $0.70

Nigeria’s shipping costs is way too high and this could be the possible reason Nigeria is losing so much money rather than making profits. Also, the average discount is relatively high compared to other countries.


- #### Identify the product subcategory that is the least profitable in Southeast Asia.

```sql
-- Identify the product subcategory that is the least profitable in Southeast Asia.
SELECT
  sub_category,
  profit,
  country
FROM vephlaproject.orders
WHERE country IN ('cambodia', 'Indonesia', 'malaysia',  'Myanmar (Burma)', 'Philippines', 'Singapore', 'Thailand', 'Vietnam')
ORDER BY 2 ASC;

```

The result of the query above was exported as a table in Excel format, standardized and visualized using Power BI.

#### Output

![least profitable in Southeast Asia](https://github.com/victorcezeh/Global_Superstore_Project/assets/129629266/cbfd8316-63fc-4abb-8279-aeca6361e857)


![least profitable in Southeast Asia Viz](https://github.com/victorcezeh/Global_Superstore_Project/assets/129629266/a25ae686-e014-4adc-8d5c-a6d0a5940eca)


The product subcategory that is the least profitable in Southeast Asia is Tables with a profit loss of -$20,163


####  Is there a specific country in Southeast Asia where Global Superstore should stop offering the subcategory identified from the result above?

```sql
-- Sum up profit loss of tables in Southeast Asia
SELECT
  sub_category,
  SUM(profit) ,
  country
FROM vephlaproject.orders
WHERE country IN ('cambodia', 'Indonesia', 'malaysia',  'Myanmar (Burma)', 'Philippines', 'Singapore', 'Thailand', 'Vietnam')
AND sub_category = 'Tables';

```

#### Output

![Too much losses in Indonesia](https://github.com/victorcezeh/Global_Superstore_Project/assets/129629266/15ff3e66-2c53-4a40-91b7-c2aebafaa1e3)


A country in Southeast Asia where Global Superstore should stop offering the subcategory Tables is Indonesia. They geneerated most of the losses and it will be good to understand why they have generated so much loss from this subcategory before we keep offering them.


#### Which city is the least profitable (in terms of average profit) in the United States? For this analysis, I discarded the cities with less than 10 orders.

```sql
-- Select all cities, average profit and quantity count in the US
SELECT
  city,
  AVG(Profit) AS avg_profit,
  COUNT(quantity) AS quantity_count
FROM vephlaproject.orders
WHERE country = 'United States'
GROUP BY city
ORDER BY 1;

-- Find Minimum average profit from result above
SELECT
  city,
  MIN(Avg_profit) as min_average_profit,
  quantity_count
FROM vephlaproject.uscities
WHERE quantity_count >= 10
GROUP BY avg_profit
ORDER BY 2 ASC;

```

The result of the query above was exported as a table in Excel format, standardized and visualized using Power BI.

#### Output


![Average Profit City](https://github.com/victorcezeh/Global_Superstore_Project/assets/129629266/0ecc4994-00f8-41a0-ba42-53c65d99edfc)



![Minimum Average City](https://github.com/victorcezeh/Global_Superstore_Project/assets/129629266/3b0b25d6-6a8a-4e7f-8822-d476e61719e4)



![Least Profitable City Viz)](https://github.com/victorcezeh/Global_Superstore_Project/assets/129629266/e317a7c4-68f7-4e86-8492-6eed62559fe8)



The city with is the least profitable (in terms of average profit) in the United States is Lancaster City with an average of -$169



#### Why is this city’s average profit so low?

```sql
-- Select Lancaster
SELECT
  order_date,
  category,
  city,
  MIN(profit) AS min_profit
FROM vephlaproject.orders
WHERE city = 'Lancaster'
GROUP BY profit
ORDER BY 4;

```

The result of the query above was exported as a table in Excel format, standardized and visualized using Power BI.

#### Output

![Lancaster](https://github.com/victorcezeh/Global_Superstore_Project/assets/129629266/109779f2-30b4-45da-80ab-b2f40d318b02)


![Lancaster Viz](https://github.com/victorcezeh/Global_Superstore_Project/assets/129629266/d27ea721-88cb-494f-bb73-3cb2d7db3200)


Lancaster City’s average profit is low because they make so much loss in profit when they purchase technology products. They had a loss of -$6,880


#### Which product subcategory has the highest average profit in Australia?

```sql
-- Which product subcategory has the highest average profit in Australia
SELECT
  Sub_category,
  AVG(profit) AS australia_avg
FROM vephlaproject.orders
WHERE country = 'Australia'
GROUP BY sub_category
ORDER BY 2 DESC;

```

The result of the query above was exported as a table in Excel format, standardized and visualized using Power BI.

#### Output

![Highest average profit in Australia](https://github.com/victorcezeh/Global_Superstore_Project/assets/129629266/2c5ade0c-b640-4787-aa0e-1abdaccd10ce)


![Highest average profit in Australia Viz](https://github.com/victorcezeh/Global_Superstore_Project/assets/129629266/0468a177-9284-4628-9266-89021b59ff6b)


The product subcategory with the highest average profit in Australia is Appliances with an average profit of $139. This is followed by Copiers with an avrage profit of $105 and Phones follow with and average of $98.


#### Which customer returned items and what segment do they belong?

![Returned Items](https://github.com/victorcezeh/Global_Superstore_Project/assets/129629266/c2184f1b-5699-4c41-a8d2-b7f8b371a04d)

The total number of customers who returned items is 619. They are segmented into three distinct categories: Consumer, Corporate, and Home Office.


#### Who are the most valuable customers and what do they purchase?

#### Top 10 custermers by profit

```sql
-- 10 Most Valuable Customers & What They Purchase.
SELECT
  customer_name,
  product_name, MAX(profit) as max_profit
FROM vephlaproject.orders
GROUP BY customer_name
ORDER BY MAX(profit) DESC
LIMIT 10;

```

The result of the query above was exported as a table in Excel format, standardized and visualized using Power BI.

#### Output

![Top 10 Valuable Customers](https://github.com/victorcezeh/Global_Superstore_Project/assets/129629266/f1fccdb2-9464-4b6d-aa45-eb1014ce6f1a)


![Top 10 Valuable Customers Viz](https://github.com/victorcezeh/Global_Superstore_Project/assets/129629266/8e02b4a7-31d2-45e6-b6fb-d042a72ca1e4)

The total profit generated from customers amounts to $1.47M across 1.59K customers. The top 10 valuable customers based on total profit generated and products purchased are:


1. Tamara Chand with $8,400 and purchased a Canon imageCLASS 2200 Advanced Copier.
2. Raymond Buch with $6,720 and purchased an Ikea Library with Doors, Traditional.
3. Hunter Lopez with $5,040 and purchased a Brother Fax Machine, Digital.
4. Adrian Barton with $4,946 and purchased a GBC Ibimaster 500 Manual ProClick Binding System.
5. Sanjit Chand with $4,630 and purchased an Ibico EPK-21 Electric Binding System.
6. Patrick Jones with $3,979 and purchased a Hoover Stove, Red.
7. Tom Ashbrook with $3,920 and purchased a Polycom CX600 IP Phone VoIP phone.
8. Christopher Martinez with $3,177 and purchased a Fellowes PB500 Electric Punch Plastic Comb Binding Machine with Manual Bind.
9. Carol Adams with $2,939 and purchased a Samsung Smart Phone, VoIP.
10. Cynthia Arntzen with $2,818 and purchased an Apple Smart Phone, with Caller ID.


From the overall profit generated, these are the to 10 customers who had the most significant impact based on total revenue generated.




## Tools Used

- Microsoft Excel
- [MySQL Workbench](https://dev.mysql.com/downloads/workbench/) (version 8.0)
- [Microsoft Power BI Desktop](https://www.microsoft.com/en-us/download/details.aspx?id=58494)


## Skillset Applied

- Microsoft Excel
- Data Importation
- MySQL
- Data Visualization using
- Microsoft Power BI
- Knowledge of generating actionable insights
- Documentation



## Project Structure

`Global Superstore Power BI.pbix`: This file contains the data visualization of this project and as seen on the documentation as well.

`Global Superstore Report.pdf`: This file contains report from the analysis.

`Global Superstore SQL Queries.sql`: This file contains the queries used for this project and as seen on the documentation as well.

`GlobalSuperstore Data.xls`: This file contains the dataset in a spreadsheet(Excel).

`README.md`: Project documentation.


## Acknowledgement

A big thank you to [Vephla University](https://vephlainstitute.com/) for equipping me with the necessary skillset to take on this project.

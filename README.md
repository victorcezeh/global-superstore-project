# Global Superstore Project

![Global Store](https://images.pexels.com/photos/1797428/pexels-photo-1797428.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1)


## Brief
Global Superstore is a global online retailer based in New York, boasting a broad product catalogue and aiming to be a one-stop-shop for its customers globally. The superstore’s clientele, hailing from 147 different countries can browse through an endless offering with more than 10,000 products. This large selection comprises three main categories: `office` `supplies` (e.g. staples), `furniture` (e.g. chairs), and `technology` (e.g. smartphones). I have been contracted as a Data Analyst to help Global Superstore analyze and draw out meaningful insight from the Superstore dataset which would aid management in making informed decisions to improve performance and profitability.

## Table of Contents

- [Getting Started](#Getting-Started)
  - [Tools Used](#Tools-Used)
  - [Clone Repo](#Clone-Repo)
  - [Usage](#Usage)
- [Project Structure](#Project-Structure)
- [Contributing](#Contributing)


## Objective

#### The objective of this project is to analyze the dataset and provide answers to the following business questions.

- Question 1
  - What are the 3 countries that generated the highest total profit for Global Superstore in 2014?
  - For each of these three countries, find the three products with the highest total profit. Specifically, what are the products’ names and the total profit for each product?

- Question 2
  - Identify the 3 subcategories with the highest average shipping cost in the United States.

- Question 3
  - Assess Nigeria’s profitability (i.e., total profit) for 2014. How does it compare to other African countries?
  - What factors might be responsible for Nigeria’s poor performance? You might want to investigate shipping costs and the average discount as potential root causes.

- Question 4
  - Identify the product subcategory that is the least profitable in Southeast Asia. Note: For this question, there is an assumption that Southeast Asia comprises Cambodia, Indonesia,       Malaysia, Myanmar(Burma), the Philippines, Singapore, Thailand, and Vietnam.
  - Is there a specific country in Southeast Asia where Global Superstore should stop offering the subcategory identified in the first part of this question?
 
- Question 5
  - Which city is the least profitable (in terms of average profit) in the United States? For this analysis, discard the cities with less than 10 Orders.
  - Why is this city’s average profit so low?

- Question 6
  - Which product subcategory has the highest average profit in Australia?
 
- Question 7
  - Which customer returned items and what segment do they belong
  - Who are the most valuable customers and what do they purchase?
 



## Dataset and spreadsheet explanation

The dataset for this project is presented in an unstandardized Excel spreadsheet format. It contains 3 different but related spreadsheets. These spreadsheets are:

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


## Data cleaning and Ingestion into MySQL Workbench

In the course of trying to clean the data using Excel, I realised it was already a clean data when collected from the source. I checked for data duplicates and spelling errors and found nothing. I went ahead to standardize the Excel spreadsheet, seperate the `Orders`, `Returns` and `People` sheets and covert them into CSV formats for easy data ingestion into MySQL Workbench using Table Data Import Wizard on MySQL Workbench.


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
SELECT sub_category, country, (AVG (shipping_cost)) as average_shipping_cost_US
FROM vephlaproject.orders
WHERE country = 'United States'
GROUP BY sub_category
ORDER BY 3 DESC
LIMIT 3;
```

#### Output

![average shippping cost United States](https://github.com/victorcezeh/Global_Superstore_Project/assets/129629266/3ac1f379-9535-4b1f-a5c7-47fcf7433505)




![average shippping cost United States_Viz](https://github.com/victorcezeh/Global_Superstore_Project/assets/129629266/c8173c6b-bbee-4013-a2cd-69fc5145242f)




#### The 3 subcategories with the highest average shipping cost in the United States are:

1. Copiers with $165
2. Machines with $132
3. Tables with $70









## Tools Used

- [MySQL Workbench](https://dev.mysql.com/downloads/workbench/) (version 8.0)
- [Power BI Desktop](https://www.microsoft.com/en-us/download/details.aspx?id=58494)


## Skillset Applied

- Data cleaning
- Data ingestion
- SQL
- Data modeling
- Data visualization using PowerBI
- Knowledge of generating actionable insights


## Expense
### Attributes
`id`: Unique identifier generated as a UUID string.

`title`: String representing the title of the expense.

`amount`: Float representing the amount of the expense.

`created_at`: Timestamp indicating when the expense was created (UTC).

`updated_at`: Timestamp indicating the last time the expense was updated (UTC).



### Methods
`update_expense(title, amount)`: Updates the expense details.

`to_dict()`: Returns a dictionary representation of the expense.



## ExpenseDataBase
### Attributes
`expenses`: List storing Expense instances.



### Methods
`add_expense(expense)`: Adds an expense to the collection.

`remove_expense(expense_id)`: Removes an expense from the collection.

`get_expense_by_id(expense_id)`: Retrieves an expense by ID.

`get_expense_by_title(expense_title)`: Retrieves expenses by title.

`to_dict()`: Returns a list of dictionaries representing expenses.




## Clone Repo

Copy link below and paste on yout Git to clone the repository.

   ```bash
   git clone https://github.com/victorcezeh/Object_Oriented_Programming_Project.git
   cd Object_Oriented_Programming_Project
   ```


## Usage

Run the Expense Tracker with the code below.

```bash
python main.py
```


## Project Structure

`Object_Oriented_Programming.py`: This code containes the Expense and ExpenseDataBase Class Implementations.

`README.md`: Project documentation.

`main.py`: The main script to test run the Expense Tracker.



## Contributing

If you'd like to contribute to the project, kindly contact ezeh_victor@yahoo.com

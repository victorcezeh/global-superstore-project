# Global Superstore Project

## Brief
Global Superstore is a global online retailer based in New York, boasting a broad product catalogue and aiming to be a one-stop-shop for its customers globally. The superstore’s clientele, hailing from 147 different countries can browse through an endless offering with more than 10,000 products. This large selection comprises three main categories: `office` `supplies` (e.g., staples), `furniture` (e.g., chairs), and `technology` (e.g., smartphones). I have been contracted as a Data Analyst to help Global Superstore analyze and draw out meaningful insight from the Superstore dataset which would aid management in making informed decisions to improve performance and profitability.

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
  - What are the three countries that generated the highest total profit for Global Superstore in 2014?
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





## Tools Used

- [MySQL Workbench](https://dev.mysql.com/downloads/workbench/) (version 8.0)


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

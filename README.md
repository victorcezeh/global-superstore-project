# Global Superstore Capstone Project

# Brief

## Global Superstore is a global online retailer based in New York, boasting a broad product catalogue and aiming to be a one-stop-shop for its customers globally. The superstore’s clientele, hailing from 147 different countries can browse through an endless offering with more than 10,000 products. This large selection comprises three main categories: `office` `supplies` (e.g., staples), `furniture` (e.g., chairs), and `technology` (e.g., smartphones). You are contracted as a Data Analyst to help Global Superstore analyze and draw out meaningful insight from the Superstore dataset which would aid management in making informed decisions to improve performance and profitability.

## Table of Contents

- [Getting Started](#Getting-Started)
  - [Tools Used](#Tools-Used)
  - [Clone Repo](#Clone-Repo)
  - [Usage](#Usage)
- [Project Structure](#Project-Structure)
- [Contributing](#Contributing)


## Objective

The objective of this project is to analyze the dataset and provide answers to the questions listed below.


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

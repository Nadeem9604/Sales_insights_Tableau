# Sales_insights_Tableau

# Sales Insights Data Analysis Project
SQL database dump is in db_dump.sql file above. Download db_dump.sql file to your local computer and import it.

First i did Data Analysis Using SQL for cleaning and checking the data some of the tasks i performed is mentioned below

1- Show all customer records

   SELECT * FROM customers;

2- Show total number of customers

   SELECT count(*) FROM customers;

3- Show transactions for Chennai market (market code for chennai is Mark001

   SELECT * FROM transactions where market_code='Mark001';

4- Show distrinct product codes that were sold in chennai

   SELECT distinct product_code FROM transactions where market_code='Mark001';

5- Show transactions where currency is US dollars

   SELECT * from transactions where currency="USD"

6- Show transactions in 2020 join by date table

   SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;

7- Show total revenue in year 2020,

   SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.currency="INR\r" or transactions.currency="USD\r";

8- Show total revenue in year 2020, January Month,

   SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and and date.month_name="January" and (transactions.currency="INR\r" or transactions.currency="USD\r");

9- Show total revenue in year 2020 in Chennai

   SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.market_code="Mark001";

# Making Tableau worksheets and dashboard
After the data cleaning and anlysing i created Worksheets and a Dashboard in Tableau Desktop
There are some problem statements which asked by steakholders or sales managers so i have to answer those questions by worksheets and dashboard

1- What is the Sales Revenue b Markets ?

2- What is the Sales Quantity by Markets ? 

3- What is the Revenue by Year ? 

4- Who are the Top 5 Customers ?

5- What are the top 5 Products ?

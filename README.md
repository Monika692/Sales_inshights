# Sales_inshights
THE SQL QUERIES FOLLOWED HERE ARE:
Show all customer records

1.SELECT * FROM customers;

2.Show total number of customers

3.SELECT count(*) FROM customers;

4.Show transactions for Chennai market (market code for chennai is Mark001

5.SELECT * FROM transactions where market_code='Mark001';

6.Show distrinct product codes that were sold in chennai

7.SELECT distinct product_code FROM transactions where market_code='Mark001';

8.Show transactions where currency is US dollars

9.SELECT * from transactions where currency="USD"

10.Show transactions in 2020 join by date table

11.SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;

12.Show total revenue in year 2020,

13.SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.currency="INR\r" or transactions.currency="USD\r";

14.Show total revenue in year 2020, January Month,

15.SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and and date.month_name="January" and (transactions.currency="INR\r" or transactions.currency="USD\r");

16.Show total revenue in year 2020 in Chennai

17.SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.market_code="Mark001";

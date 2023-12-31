# ATLIQ Hardware Sales Insight Data Analysis Using SQL and Power BI
___
![](Intro_Photo.jpg)

## Intoduction
---
Atliq Hardware is a prominent supplier of computer hardware and peripherals to various esteemed clients, including Surge Stores, Nomad Stores, Excel Stores, and Electricalsara Stores across India. The company's headquarters are based in Delhi, and it operates regional offices spanning different regions of the country. However, the Sales Director of Atliq Hardware is currently facing a series of challenges in light of the rapidly evolving market.

One of the main difficulties the Sales Director is encountering is effectively tracking sales in this dynamic and growing market. The ever-changing landscape poses obstacles in gaining accurate insights into the business performance. Additionally, the Sales Director relies on the regional managers for North, South, and Central India for updates and information. Unfortunately, the data provided by these managers is conveyed verbally during phone conversations, often painting an overly optimistic picture of the sales situation.

This discrepancy between the rosy picture presented and the observable decline in overall sales has left the Sales Director feeling frustrated. Despite requesting specific numbers, the regional managers tend to provide information in numerous excel files, making it challenging for the Sales Director to gain a comprehensive understanding of the situation.

In an effort to make data-driven decisions and boost the company's sales, the Sales Director is seeking a more efficient and transparent solution. Specifically, he desires an interactive dashboard that can present data in a clear, easy-to-understand, and digestible manner. This dashboard would enable him to grasp the complete picture of the company's performance promptly.

By having access to a user-friendly dashboard with real-time data, the Sales Director can make informed decisions that will propel the company's growth in this highly competitive market.

## Problem Statement
---
-  Detailed breakdown of the revenue generated in each of the cities where we have a presence.
-  Comprehensive breakdown of the company's revenue over the past few years and months to understand any trends or patterns. 
-  The top 5 customers are in terms of both revenue generated and the quantity of products sold.
-  The list of the top 5 best-performing products based on revenue.
-  The net profit and profit margin figures for each market segment.

## Skills
---
- SQL
- Power BI

## Project Planning and AIMS GIRD
---
1. Purpose -  To unlock sales insights that are not visible before for sales team for decision support & automate them to reduced manual time spent in data gathering.
2. Stakeholders -
   
        • Sales Director
   
        • I.T. Team
   
        • Customer Service Team
   
        • Data & Analytics Team
   
4. End Result -  An automated dashboard providing quick & latest sales insights in order to support data driven decision making.
5. Success Criteria -
   
        • Dashboards uncovering sales order insights with latest data available.
   
        • Sales team able to take better decision & prove 10% cost savings of total spend.
   
        • Sales analysts stop data gathering manually in order to save 20% of their business time & reinvest it in value added activity.


## Data Analysis using SQL
---

• Show all customer records
           
           SELECT * FROM sales.customers ;

• Show total number of customers
           
           SELECT count(*) FROM sales.customers ;

• Show transactions for Chennai market (market code for Chennai is Mark001)
           
           SELECT * FROM sales.transactions where market_code = 'Mark001';

• Show distrinct product codes that were sold in chennai.
           
           SELECT distinct product_code FROM sales.transactions where market_code = 'Mark001' ;

• Show transactions where currency is US dollars.
           
           SELECT * from sales.transactions where currency = "USD" ;

• Show transactions in 2020 join by date table.
           
           SELECT sales.transactions.*, sales.date.* FROM sales.transactions 
           INNER JOIN sales.date ON sales.transactions.order_date = sales.date.date 
           where sales.date.year = 2020 ;

• Show total revenue in year 2020.
           
           SELECT SUM(sales.transactions.sales_amount) FROM sales.transactions 
           INNER JOIN sales.date ON sales.transactions.order_date = sales.date.date 
           where sales.date.year=2020 
           and transactions.currency="INR\r" or transactions.currency="USD\r" ;

• Show total revenue in year 2020, January Month.
    
           SELECT SUM(sales.transactions.sales_amount) FROM sales.transactions 
           INNER JOIN sales.date ON sales.transactions.order_date = sales.date.date 
           where sales.date.year = 2020 
           and sales.date.month_name="January" 
           and (transactions.currency="INR\r" or transactions.currency="USD\r");

## Power BI Dashboard
---

![](1.png)

---
![](2.png)

---
![](3.png)

---
![](4.png)

---
![](5.png)

---


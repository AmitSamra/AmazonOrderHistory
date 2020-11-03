![amazon_logo](https://github.com/AmitSamra/AmazonOrderHistory/blob/master/img/amazon_logo.png)
![python_logo](img/python_logo.png)
![pandas_logo](img/pandas_logo.png)
![matplotlib_logo](img/matplotlib_logo.png)
![sqlalchemy_logo](img/sqlalchemy_logo.png)

Amazon.com is the largest online retailer in the world. One of the best things about Amazon is the ability to download order reports in CSV format. In this project, I provide insight into my Amazon order history spanning 2008 to 2019, inclusive. I use pandas, matplotlib and SQLAlchemy to clean, analyze and persist data.

This repository includes a [JupyterNotebook](https://github.com/AmitSamra/AmazonOrderHistory/blob/master/AmazonOrderHistory.ipynb), which contains all of the code used to generate the following report. 

# Table of Contents

1. [Data Processing](https://github.com/AmitSamra/AmazonOrderHistory#1-data-processing)
2. [Data Analysis](https://github.com/AmitSamra/AmazonOrderHistory#2-data-analysis)
3. [SQL](https://github.com/AmitSamra/AmazonOrderHistory#3-sql)

# 1. Data Processing

The following is a the raw dataframe generated by reading [amazon_purchases.csv](img/amazon_purchases.csv) into Python Pandas. Note how columns are formatted incorrectly and many fields are missing. 

![Raw Dataframe](img/raw_dataframe.png)

Data cleaning is an important part of the ETL process. The following shows the final dataframe. Note how the formatting and rows containing NaN have been replaced or removed.

![Final Dataframe](img/final_dataframe.png)

[Home](https://github.com/AmitSamra/AmazonOrderHistory#table-of-contents)

# 2. Data Analysis

Let's begin with a striking number: $30,000. That's how much I spent on Amazon over the last 12 years. 

![Total Spending](img/total_spent.png)

It took 781 transactions to achieve this number. 2019 marked a sharp increase in my transactions, surpassing the peak I hit in 2011. 

![TransactionsByYear](img/TransactionsByYear.png)

My average transaction size was almost $40.

![AveragePerTransPerYear](img/AveragePerTransPerYear.png)

The following shows my daily purchase totals. Most of my transactions seem to be below $50 with occasional big-ticket purchases. 

![DailyPurchaseAmount](img/DailyPurchaseAmount.png)

This graph shows what seems to be an outlier. I spent over $7,000 in 2011. 

![PurchasesByYear](img/PurchasesByYear.png)

It seems that I spent the most amount in March, July and August and not during Christmas. 

![PurchasesByMonth](img/PurchasesByMonth.png)

Is there any particular day that I purchased more frequently? Yes, Monday. I seem to haved ordered more in the beginning of the week, likely due to the chances of things being delivered quickly on a weekday. 

![PurchasesByDay](img/PurchasesByDay.png)

Most of my purchases on Amazon were for Computers and Electronics equipment. 

![PurchasesByCategory](img/PurchasesByCategory.png)

The two categories accounted for nearly 50% of my Amazon purchases. 

![PurchasesByCategoryShare](img/PurchasesByCategoryShare.png)

Almost 60% of my transactions were with Amazon as the seller. 

![TransactionsBySeller](img/TransactionsBySeller.png)

But Amazon accounted for 75% of my purchase spend. Perhaps it's the generous returns policy for goods sold directly by Amazon. 

![PurchasesBySeller](img/PurchasesBySeller.png)

Most orders were shipped using USPS folowed by Amazon's in-house delivery service. 

![ShippingMethod](img/ShippingMethod.png)

However, orders with the highest value were shipped with either FedEx or UPS. 

![ShippingMethodPrice](img/ShippingMethodPrice.png)

[Home](https://github.com/AmitSamra/AmazonOrderHistory#table-of-contents)

# 3. SQL

One of the best things about Python is that we can actually source our data directly from SQL. The following shows a dataframe that I both created and sourced by using SQLAlchemy. 

![SQL_dataframe](img/SQL_dataframe.png)

SQLAlchemy can be used to directly query data from a SQL database. The queries can then be utilized inside Python. 

![SQL_PurchasesByYear](img/SQL_PurchasesByYear.png)

This concludes my presentation. Thank you! 

[Home](https://github.com/AmitSamra/AmazonOrderHistory#table-of-contents)
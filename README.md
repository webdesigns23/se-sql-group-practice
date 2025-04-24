# Practice for Grouping Data with SQL

## Set Up

* Fork and Clone the GitHub Repo
* Install dependencies and enter the virtual environment:
    * `pipenv install`
    * `pipenv shell`

Next, let's set up our code in `main.py`. Import libraries and connect to the database.

```python
import pandas as pd
import sqlite3

conn = sqlite3.connect('data.sqlite')
pd.read_sql("""
SELECT *
  FROM products;
""", conn)
```

## Practice Queries

1. Select the product line
*   Count the number of each product line
*   Give the count the alias "count"
*   Sort descending by count

2. Select the product line
- Determine the average by Price by product line
- Give the average the alias "avgPrice"
- Sort descending by avgPrice

3. Select the product line
- Find the minimum of the MSRP as minMSRP
- Find the maximum of the MSRP as maxMSRP

4. Repeat (3), but only select the rows where the MSRP is $50 or more.

5. Repeat (2), but only select the product lines with an average price greater than $50.  

6. Select the product line
- Find the average buy price as 'buyPrice' and the average MSRP as 'avgMSRP'
- Only select MSRP greater than equal to $50
- Only select avgPrice greater than equal to $50
- Group by by product line and order by the ascending average price


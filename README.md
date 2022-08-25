# SQL NOTES

### DISTINCT AND COUNT

```
SELECT DISTINCT Country FROM Customers;
This is similar to .filter() as this selects the data with out repetition

SELECT Country FROM Customers;
This returns all with repetiio and duplicates

SELECT COUNT(Country) FROM Customers;
This returns counts of all including the data with duplicates

SELECT DISTINCT COUNT(Country) FROM Customers;
This returns counts of all EXCLUDING the data with duplicates

```

### WHERE

```

SELECT * FROM Customers WHERE CustomerID=10;
This first returns the whole data because of * and then the WHERE is a conditional statment which returns based on the condition CustomerID=10

SELECT DISTINCT CustomerID=10  FROM Customers; will retuen just the ID without the value because we did not include the initial statment asking it to return the full data.

BETWEEN return Between a certain range
LIKE   Search for a pattern and is for patial matching
=	is exact Equal Matching

SELECT * FROM Customers
WHERE City='Berlin' OR City='München'
This returns Berlin and München

```

### ORDER BY

```
SELECT * FROM Customers
ORDER BY Country ASC/DESC;

SELECT * FROM Customers
ORDER BY Country ASC, CustomerName DESC;

```

### INSERT INTO, DELETE and UPDATE

```
INSERT INTO Customers (CustomerName, ContactName, Address, City, PostalCode, Country)
VALUES ('Cardinal','Tom B. Erichsen','Skagen 21','Stavanger','4006','Norway');

This inserts Data into the row

UPDATE Customers
SET ContactName='Alfred Schmidt', City='Frankfurt'
WHERE CustomerID=1;

DELETE FROM Customers
WHERE CustomerName='Alfreds Futterkiste';
This delets where Customer Name is 'Alfreds Futterkiste'

DELETE FROM Customers
This delets All

```

### NULL EMPTY DATA

```
SELECT column_names
FROM table_name
WHERE column_name IS NOT NULL;


This returns values that are not null(empty)

```

### SELECT TOP AND BOTTOM (WITH DESC)

```
SELECT TOP 3 * FROM Customers
WHERE Country='Germany' AND City='Berlin';

This returns list of Country Germany and City Berlin


SELECT TOP 50 PERCENT * FROM Customers
ORDER BY Country DESC, CustomerName DESC;


SELECT  * FROM Products
WHERE Price = 18
ORDER BY ProductName DESC LIMIT 2

```

### MIN(Price) and MAX(Price)

```
SELECT MIN(Price) AS SmallestPrice
FROM Products;

returns the smallest price

SELECT MAX(Price) AS LargestPrice
FROM Products;

returns the largest price
```

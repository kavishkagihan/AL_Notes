      
# Analyses the main components of a database system

### Components of DBMS
- Hardware
- Software
- Data
- Procedures
- DAL (Database Access Language)

![](../../../assets/Images/Pasted%20image%2020230729184507.png)

### SQL

- SQL stands for Structured Query Language
- SQL lets you access and manipulate databases
- SQL became a standard of the American National Standards Institute (ANSI) in 1986
- SQL commands falls into 2 basic groups
	- **Data Definition Language ( DDL)**
	- **Data Manipulation Language ( DML)**

#### Data Definition Language (DDL)

- This is the SQL commands **used for defining and modifying** the data and its structure
- It is used to build and modify the structure of your tables


![](../../../assets/Images/Pasted%20image%2020230729185010.png)

#### Data Manipulation Language (DML)

- These are the commands used for **selecting, inserting, deleting and updating** data in a database.
- It is used to retrieve and manipulate data in a relational database
- DML **performs read-only queries** of data.

![](../../../assets/Images/Pasted%20image%2020230729185130.png)

### Writing SQL queries

![](../../../assets/Images/Pasted%20image%2020230729185824.png)
![](../../../assets/Images/Pasted%20image%2020230729185942.png)


#### Special Operators

- BETWEEN - Used to check whether an attribute value is within a range

![](../../../assets/Images/Pasted%20image%2020230729190039.png)

- IS NULL - Used to check whether an attribute value is null

![](../../../assets/Images/Pasted%20image%2020230729190215.png)

- LIKE - Used to check whether an attribute value matches a string pattern
	- `%` is a special character used to mean any characters (plural)
	- `_` is a special character used to mean any single character (singular)

![](../../../assets/Images/Pasted%20image%2020230729190246.png)
![](../../../assets/Images/Pasted%20image%2020230729190305.png)

- IN - Used to check whether an attribute value matches any value within a value list

![](../../../assets/Images/Pasted%20image%2020230729190329.png)

- EXISTS - Used to check if a sub query returns any rows
![](../../../assets/Images/Pasted%20image%2020230729190400.png)


```sql

1. SELECT * FROM STAFF;
2. SELECT Sno, FName, LName, salary from STAFF;
3. SELECT DISTINCT Pno FROM PROPERTY_FOR_RENT;
4. SELECT Sno, FName, LName, (Salary * 30) AS monthly_salary FROM STAFF;
5. SELECT * FROM STAFF WHERE Salary > 10000;
6. SELECT Street FROM BRANCH WHERE City = 'London' OR City = 'Glasgow';
7. SELECT * FROM STAFF WHERE DOB >= '1975-01-01' AND DOB <= '1995-12-31';
8. SELECT * FROM STAFF WHERE Position = 'Manager' OR Position = 'Deputy';
9. SELECT * FROM STAFF WHERE Address LIKE 'Glasgow';
10. SELECT * FROM VIEWING WHERE Pno = 'PG4' AND Comment IS NULL;

```


#### SQL aggregate functions


![](../../../assets/Images/Pasted%20image%2020230729190620.png)

##### **Examples**

![](../../../assets/Images/Pasted%20image%2020230729191042.png)

- SUM
```sql
SELECT SUM(Total) FROM Orders WHERE OrderDate BETWEEN '3/1/2014' AND '3/31/2014'
```


- AVG - 
```sql
SELECT AVG(Total) FROM Orders WHERE OrderDate BETWEEN '3/1/2014' AND '3/31/2014'
```

- COUNT 
```sql
SELECT COUNT(*) FROM Orders
SELECT COUNT(OrderId) FROM Orders
```


- GROUP BY
	- Used to group and kind of sort out the results we get.
	- I.e say you have a list of customers from different countries. You can use GROUP BY to identify how many customers are from a certain country, like this 
	```sql
	SELECT country, COUNT(customer_id) FROM customers GROUP BY country;
	```
	- We can even use 2 columns if needed, like say you have the customer's country and the city, so you can further group it like this	
	```sql
	SELECT country, COUNT(customer_id) FROM CUSTOMERS GROUP BY country, city;
	```

![](../../../assets/Images/Pasted%20image%2020230729193816.png)

- JOIN - to perform queries relating more than 1 table
	- common attributes is an important distinction in relational database
	- This general idea is
		 ```
		get rows from Table A 
		and rows from Table B 
		where the PK(Table A) = FK(Table B)
		```
	- refer - https://www.mysqltutorial.org/mysql-inner-join.aspx
	- this is the syntax
		```sql
		SELECT select_list FROM t1 INNER JOIN t2 ON join_condition1
		```
	- Example
		![](../../../assets/Images/Pasted%20image%2020230729201602.png)
		- the table `products` has the column `productLine` that references the column  `productline` of the table `productlines` . The column `productLine` in the table `products` is called the [foreign key](https://www.mysqltutorial.org/mysql-foreign-key/) column.
		- Suppose you want to get:
			- The `productCode` and `productName` from the `products` table.
			- The `textDescription` of product lines from the `productlines` table.
		- To do this, you need to select data from both tables by matching rows based on values in the `productline` column using the `INNER JOIN` clause as follows:
			```sql
			SELECT 
			    productCode, 
			    productName, 
			    textDescription
			FROM
			    products t1
			INNER JOIN productlines t2 
			    ON t1.productline = t2.productline;
			```
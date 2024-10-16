
# Describes the main components of the relational database model

### Characteristics of Tables

- A table contains data about a group of related entities
- Table: entity set, a two-dimensional structure composed of rows and columns
- Each table row (tuple) represents a single entity occurrence with the entity set - a Student
- Each table Column represents an attribute and each column has a distinct name - Student ID
- All values in a column must conform to the same data type/format
- Each table must have a key, one or more attributes that uniquely identifies each row

### DBMS Keys

```
A DBMS key is an attribute or set of an attribute which helps you to identify a row 
```

##### Primary Key

```
A key with a singel attribute that is used to identify a certain record uniquely is called  a primary key.
```

**Rules for defining Primary key**

- Two rows can't have the same primary key value
- Its a must for every row to have a primary key value.
- The primary key field cannot be null.
- The value in a primary key column can never be modified or updated **if any foreign key refers to that primary key**
- Each table must have a Primary Key

##### Composite key

```
A key which has multiple attributes to uniquely identify rows in a table is called a composite key
```

![](../../../assets/Images/Pasted%20image%2020230715192518.png)

##### Candidate key
```
A super key with no repeated attribute is called a candidate key.
```

> A candidate key is a possible primary key, as it doesn't repeat itself

- The Primary key should be selected from the candidate keys. Every table must have at least a single candidate key.

**Properties of a candidate key**

- It must contain unique values
- Candidate key may have multiple attributes
- Must not contain null values
- It should contain minimum fields to ensure uniqueness
- Uniquely identify each record in a table.

![](../../../assets/Images/Pasted%20image%2020230715192909.png)

##### Alternate Key

```
Keys that are left of candidates keys after chosing the primary key.
```

- Technically, it is a candidate key which is currently not the primary key.
- A table may have single or multiple choices for the primary key

![](../../../assets/Images/Pasted%20image%2020230715193304.png)

##### Foreign key (FK)

```
A foreign key is a column which is added to create a relationship with another table
```

- helps to maintain integrity of data
- allow navigation easy
- if using a foreign key, every model needs to be supported by a foreign key.
- Helps reduce redundancy. (Redundancy is unnecessary duplication of data)
- Foreign key is nullable.

![](../../../assets/Images/Pasted%20image%2020230715193816.png)

###### Difference between Primary key & foreign key

![](../../../assets/Images/Pasted%20image%2020230715194157.png)

![](../../../assets/Images/Pasted%20image%2020230715194751.png)

![](../../../assets/Images/Pasted%20image%2020230715194819.png)

- How a foreign key is set for a table

```sql
-- Create the Customers table
CREATE TABLE Customers (
    CustomerID INT PRIMARY KEY,
    CustomerName VARCHAR(50),
    CustomerAddress VARCHAR(100)
);

-- Create the Orders table
CREATE TABLE Orders (
    OrderID INT PRIMARY KEY,
    OrderDate DATE,
    CustomerID INT,
    FOREIGN KEY (CustomerID) REFERENCES Customers(CustomerID)
);
```
#### Domain

```
A domain is defined as the set of all unique values permitted for an attribute
```

- For example, a domain of date is the set of all possible valid dates, a domain of integer is all possible whole numbers

![](../../../assets/Images/Pasted%20image%2020230715195011.png)
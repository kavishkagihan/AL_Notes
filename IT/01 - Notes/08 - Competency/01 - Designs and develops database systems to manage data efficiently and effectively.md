
#  Designs and develops database systems to manage data efficiently and effectively

#### Structured Vs. unstructured data

**Structured Data**

- Structured data refers to any data that resides in a fixed field within a record or file.
- This includes defining what fields of data will be stored and how that data will be stored
- Ability to enter easily
- Managed using Structured Query Language (SQL)
- (numeric, currency, alphabetic, name, date, address

**Unstructured Data**

- Unstructured data is all those things that can't be so readily classified and fit into a neat box
-  (photos and graphic images, videos, streaming instrument data, webpages, PDF files)

| Structured Data                        | Unstructured Data                                |
| -------------------------------------- | ------------------------------------------------ |
| Fit into a pre-defined model           | Doesn't fit into a pre-defined model             |
| Easy to search                         | Difficult to seach                               |
| Usually text based                     | Could text based or binary based                 |
| Often stored in Relational databases   | Often stored in Non-relational databases (NoSQL) |
| Examples: Dates, Addresses, NIC, Names | Examples: PDF files, Images, Videos, Audio files |


![](../../../assets/Images/Pasted%20image%2020230715184127.png)

#### What is a Database?

```
Database is a specialized structure that allow computer-based systems to store, manage and retrieve data very quickly.
```

##### Problems with not using the database.
- Security
- Accuracy
- Redundancy
- Incomplete Data

![](../../../assets/Images/Pasted%20image%2020230715184523.png)

#### What is a DBMS?

```
DBMS is a collection of programs trhat manage database sturcture, control access to data, facilitate the sharing of data, anables efficient and effective data management.
```

![](../../../assets/Images/Pasted%20image%2020230715185753.png)

##### Benefits of a DBMS
- Provides consistent view of data and operations
- enables ad-hoc queries
- Reduces data inconsistencies and errors.
- Helps with data security 

#### Database models

- Flat file system
- Hierarchical model
- Network model
- Relational model
- Object Relational model


##### Flat File system

- Firstly introduced model
- All the data used is kept in the same plane.
- This model is not so scientific.
- (Excel, Calc)

![](../../../assets/Images/Pasted%20image%2020230715190244.png)

##### Hierarchical Model

- Hierarchical model has one parent entity with several children entity
- But at the top we should have only one entity called **root**
- The root can have several children entities.

![](../../../assets/Images/Pasted%20image%2020230715190350.png)

##### Network Model

- Entities are stored in a graphical representation
- Some entities are accessible through several paths.

![](../../../assets/Images/Pasted%20image%2020230715190448.png)

##### Object Relational Model

- widely used in computer applications to **hold audio, video and graphic files**
-  consist of data piece and the methods which are the DBMS instructions.

![](../../../assets/Images/Pasted%20image%2020230715190558.png)

##### Relational Model

-  **most popular** model and the **most extensively** used model
- data can be stored in the tables, these storing is called relations 

![](../../../assets/Images/Pasted%20image%2020230715190847.png)

**Comparison of database models**

![](../../../assets/Images/Pasted%20image%2020230715190912.png)

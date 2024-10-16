
# Normalizes database schema to improve performance


```
Normalization is a process to evaluate and correct the table structure
```
> This is another database design tool except ER diagrams

>Here what happens is that we are given a document with a mixed up records, and here with normalization we just clean it up according to a couple of stages and insert those data into a database

Drawing an ER diagram is a **top-bottom** approach
- Here we start from 0 and build everything from there
But normalization is a **bottom-top** approach 
- Here we take a finalized document and then build a database off of that 

The method we use from ER or normalization depends on the story line 
- What is the main purpose of using this method (including ER diagram)

```
To minimize data redundency
```

### Normalization Objectives

- To ensure tables have the following characteristics
	- Each table represents a single subject (One to student, one for teaching etc)
	- No data duplication
	- All the attributes in a table are uniquely identified by a primary key
	- To avoid anomalies (happens due to data redundancy) for data insertion, updating and deletion.
### Normalization Stages
Normalization goes through number of stages
- First normal form (1NF)
- Seconds normal form (2NF)
- Third normal form (3NF)

In each of these stages, there are certain things that happen to the document that's not normalized yet.

| Normal form | Actions                                 |
| ----------- | --------------------------------------- |
| 1NF         | Format the tables                       |
|             | Make sure there are no repeating groups |
|             | Define a primary key                    |
| 2NF         | No partial dependencies                 |
| 3NF         | No transitive dependencies              |
#### First Normal Form (1NF)

1. A table must not contain repeating groups
	- **Eliminate the repeating groups** by making sure each attribute contains an appropriate data value
2. Choose a primary key 
	- A “key” should identify **one record** not a group
3. Identify all dependencies

> Physically, they way we identify the document is in 1NF is by seeing whether if it has any repeating groups. If not, it is in 1NF, else not.
##### Eliminating the repeating groups

Think of an example like this.

![](../../../assets/Images/Pasted%20image%2020240622193844.png)

This table is in the 0NF form. Why? Even though the primary keys are defined here (as `EmpID` and `Department`) there are repeating groups as `Client1` and `Client2`. So we need to remove those first. For that we need to create `client` table

CLIENT(<u>ClinetID</u>, ClinetName,EmpID<sup>*</sup>)
EMP_DEP(<u>EmpID</u>,EmpName,<u>Department</u>,Location,Working_Hours)

>So like this now we have 2 tables, which are both in 1NF form, as there are **no repeating groups** and both tables h**ave a primary key defined**.



##### Functional Dependency

There are 2 main types of dependencies
1. Partial dependency
2. Transitive dependency

**Partial dependency**
- This happens only when there is a composite key is present
- In a composite key, there could be 2 or more key attributes. Partial dependency is **when other non-key attributes depend on any of those key attributes**.

![](../../../assets/Images/Pasted%20image%2020230902195946.png)

Here, in this diagram, `PROJ_NUM` and `EMP_NUM` are the 2 key attributes used to define the composite key. When take individually, 
- `PROJ_NAME` is dependent on `PROJ_NUM`
- `EMP_NAME`, `JOB_CLASS`, `CHG_HOUR` are dependent on `EMP_NUM`
This is partial dependency.

**Transitive dependency**
- This happens when **2 non-key attributes are related to each other.**
- Gets identified in the 2NF stage (even though, we can identify this in the 1NF as well)

![](../../../assets/Images/Pasted%20image%2020230902203258.png)

Here the `JOB_CLASS` and the `CHG_HOUR` attributes are related to the `EMP_NUM` key attribute. Those 2 are also related to each other, as the hourly charging rate depends on the job class. This is when transitive dependency happens.

If transitive dependency exists, we need to go from 2NF to 3NF stage 

#### Second Normal Form (2NF)

> Goal of 2NF is to remove partial dependencies

- What is the problem of 1NF?

```
There should be NO partial dependencies in a table
```

- In the 2NF, **partial dependencies are removed  and separate tables are made for the key attributes** of the partial dependencies. 
- And then, transitive dependencies are identified.

![](../../../assets/Images/Pasted%20image%2020230902204331.png)
> Note that here to relate the `EMPLOYEE` and `PROJECT` tables, **an additional table called `ASSIGNMENT` has been added.**

Here, once the tables are made according to the 2NF, we can see the transitive dependency in the `EMPLOYEE` table. 
#### Third Normal Form (3NF)

<head>
<style> p { color: red} </style>
</head>

Now that have identified the transitive dependencies, we need to make an **additional table for the transitive dependency** to remove them so that it becomes a 3NF

![](../../../assets/Images/Pasted%20image%2020230902204845.png)

>Since `JOB_CLASS` **depends on the employee**, and we need to **make a connection between the additional table we make and the `EMPLOYEE` table**, we are taking the `JOB_CLASS` as the primary key of the new table and make it the **foreign key** of the `EMPLOYEE` table 

After all is done, the initial document we had should include the table which connects the 2 main tables we made according to the partial dependencies. Plus 

![](../../../assets/Images/Pasted%20image%2020230902204512.png)

And also we should have a separate table for the transitive dependency

> So in summary, for every partial, transitive dependency we find **represents a relation** between table. Which means for every dependency, separate tables must be made


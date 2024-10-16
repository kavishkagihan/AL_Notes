
# Designs the conceptual schema of a database

- What is a Data model?
```
Simple representation (usually graphical) of more complex real world data structures
```

![](../../../assets/Images/Pasted%20image%2020230805184757.png)

- A data model organizes data for different users
- Data modeling is the first step in designing a DB
### Building Blocks of Data Models

- Entities
	- Things about which data is to be collected
	- e.g., employee, students, courses
- Attributes
	- Characteristics of the entity
	- e.g., ID, name, DOB, manufacturer number
- Relationships (cardinalities)
	- 1:1 (one to one)
	- 1:M (one to many)
	- M:N (many to many)
### Business Rules

```
Business rules determine the building blocks
```

- Above-mentioned building blocks are determined from the business rules.
- Any organization that stores data has business rules
	- Policies, procedures, or principles
	- For example, each full-time student must select at least 3 units each semester

### Importance of Business Rules
- Help verify the data model
	- Without knowing the business rules, we can't identify the entities, relationships and attributes
- Communication tool
	- helps to the relationship between the user and the designer to understand the nature of the database model.

![](../../../assets/Images/Pasted%20image%2020230805190230.png)

### Evolution of Data Models
- Early age
	- Hierarchical and Network models
- Modern age
	- Relational model
	- Entity Relationships (ER) model
- New age
	- Object-Oriented, Object/Relational, XML, Big Data and NoSQL

#### Relational Model
- Developed by E.F. Codd
- Conceptually simple
- Powerful modelling capabilities
- But considered impractical in 1970due to lack of computing power
- Modern computers can handle relational databases with no problem

| Merits                    | Limitations                |
| ------------------------- | -------------------------- |
| Structural Independence   | Substantial hardware        |
| Conceptual Simplicity     | System Overhead            |
| Implementation Simplicity | Can facilitate poor design |

#### Entity Relationship (ER) Model

![](../../../assets/Images/Pasted%20image%2020230805191329.png)

#### ER Model
- A graphical data model
- Introduced by Chen in 1976
- Defines database structures in terms of the **entities** and their **relationships**
#### ER-Relational

- An ER model maps to relational tables
- Each **entity set** maps to a **relational table** `Entity set --> table`
- Each **entity instance** maps to a **table entry (row)** `Entity occurence --> row`

| Merits                                | Limits                                          |
| ------------------------------------- | ----------------------------------------------- |
| Exceptional conceptual simplicity     | Representation of constraints and relationships |
| Effective communication tool          | No data manipulation language                   |
| Complements the relational data model |                                                 |

#### Four Tests for an Entity Type

You have to check if these 4 rules are fulfilled when you are choosing whether if it's an entity or not.
- **It should be of importance to the system being studied**
- **Should be able to have of a number of attributes that belong to the entity type.**
- **There should be several occurrences of the entity type**
- **Each occurrence should be uniquely identifiable** (should be possible to define a primary key)

##### Entity
```
A uniquely identifiable object or concept that is of significance to the system and about which information is to be held.
```

- Entity types, Entity sets → Tables
- Entity instances, Entity Occurrences → Rows

> When naming entities in ER diagrams, we need to use the singular form
> - Book
> - Author
> - Student


![](../../../assets/Images/Pasted%20image%2020230805195426.png)

###### Entity type

- Two classes of entity types
	- Weak entity
		- an entity whose existence depends on other entities
		- Can be identified uniquely only by considering the primary key of another strong entity
	- Strong/Regular Entity
		- an entity that is not weak (independent)
![](../../../assets/Images/Pasted%20image%2020230805195623.png)
##### Attributes
```
A property for an entity
```
- e.g holds all data elements associated with entities

![](../../../assets/Images/Pasted%20image%2020230805195742.png)
###### Attribute types
- Single / Composite
	- single
		-  Can have a single value from the associated domain
		- like the student id
	- composite
		- Can have more than one value from the associated domain
		- like the name, `First name` and `last name`
- Key
- Base / Derived
	- base - raw value we input to the database, cannot be deduced (date of birth)
	- derived - value we derive from process (age --> `current date - date of birth`)

![](../../../assets/Images/Pasted%20image%2020230805201155.png)
##### Relationships

```
A meaningful association among entity types
```

- Relationships of the same type are grouped or typed into a relationship type
- Entities are linked together by relationships
- Exists if one or more attributes are **common** to two entities

![](../../../assets/Images/Pasted%20image%2020230805202758.png)
##### Degree

```
The number of entities associated with the relationship
```

- Unary relationships
	- Only one entity is involved
		- Employee of a company is married to another employee of the same company
- Binary relationships
	- 2 entities are involved
	- the most common type in the real world
- Ternary relationship
	- when n number of entities are involved

##### ER Notation Relationships

![](../../../assets/Images/Pasted%20image%2020230805203224.png)
##### Structural Constraints - Cardinality

- A relationship may allow multiple occurrences of subject/object.
- Possible Cardinalities
	- One to One 1:1
	- One to Many 1: m
	- Many to Many m: n

- one to one

![](../../../assets/Images/Pasted%20image%2020230805203949.png)

- one to many
![](../../../assets/Images/Pasted%20image%2020230805204041.png)

- many to many
![](../../../assets/Images/Pasted%20image%2020230805204122.png)

> Note - relational databases are unable to handle m: n relationships. Therefore, if they occur they must be resolved by two 1: n relationships

##### Structural Constraints - Participation/Optionality Constraints

```
Participation constraints determine whether the existence of an entity depends upon its being related to another entity through the relationship
```

There are 2 types of participation constraints
- **Total** - A mandatory relationship is where one occurrence of an entity type must be associated with an occurrence of the other entity type (mentioned by a double line) (all occurrences of table A has to be connected to a row of table B)
- **Partial** - A relationship is said to be optional between 2 entities if an occurrence of one may exist without associated occurrences of the other (mentioned by a single line)

REF: https://www.youtube.com/watch?v=W7SVMKIwOzs
![](../../../assets/Images/Pasted%20image%2020240427140337.png)
> According to this example, an employee must at least work for 1 Department. However, there can be departments where no employees are in work. (This could be the case for newly formed departments)

###### Example

![](../../../assets/Images/Pasted%20image%2020230812185552.png)
- Entities should be inside rectangles (Students, Instructor)
- Attributes should be in ovals (name, code)
- Key attribute (primary key) should be underlined
- Relations should be marked according to the cardinality (1:1, 1:m, n:m)

![](../../../assets/Images/Pasted%20image%2020230812191808.png)

##### Extended ER Diagram -EERD

EER is a high-level data model that incorporates the extensions to the original ER model. There are a couple of ways of doing this but for our syllabus, we only talk about **Specialization** and **Generalization**
###### **Specialization**

```
Specialization is a process of identifying subsets of an entity that share some different characteristic
```

For example, we have an entity called vehicles. This vehicle entity could have values like car, bike which have special attributes.
I.e car could have a special characteristic called engine type and the bike could have a special characteristic called tyres. To represent these in an ER diagram, this technique is used.
###### Generalization

This is kinda the opposite of the specialization. Here we take 2 or more sub entities, like Pigeon, Sparrow and Dove which can be generalized into **birds** 

![](../../../assets/Images/Pasted%20image%2020230819185918.png)

# Designs the logical schema of a database

There are different kinds of database sachems
1. Conceptual schema - The plane and the structure we have in our head (ER diagrams)
2. Logical(Relational) schema - The tables we make using the structure
3. Physical schema - Final tables filled with data 

### Transform ER Diagram into Relational schema

The given ER diagram should be written in the following form

![](../../../assets/Images/Pasted%20image%2020230819191948.png)

```
ENTITY_NAME(PRIMARY_KEY (underlined), OTHER_ATRIBUTES)
```

- **Multivalued attributes**

I.e if we have 2 telephone numbers for the same person, we have to **go for another additional table** to represent them, and use the primary key of the  initial table as the foreign key for the additional table. 

![](../../../assets/Images/Pasted%20image%2020230819192847.png)

The `BANCH` table is the main table and the `BRANCH_TEL_NO` is the additional table we added to add the telephone numbers. Here to present the foreign key, an `*` is used.

- **Composite attributes**
These attributes are stored in the same table as 2 columns.
For example the name -> (First name, Last name). These both are saved in the same table.

```
STAFF(Staff_ID,f_name,l_name)
```
> Only multi valued attributes are made into a seperate table.

- **Derived attributes.**

These values **aren't represented in the table**. When needed, they are derived at the time to retrieval. I.e if in the ER diagram we have name, **age** and date of birth as fields, when making the table we only include the name and date of birth as we can derive the age based on that.

```
STUDENT(name, date_of_birth)
```

##### Relationships
- **One to many relationship**

Here, the primary key of the 1 side is set as the foreign key of the many side.

![](../../../assets/Images/Pasted%20image%2020230819194956.png)

`SUPPLIER` is the 1 side and the `PURCHASE_ORDER` is the many side. `supplier_no` which is the primary key from the 1 side is related to the foreign key of the many sides

- Many to many

Here we have to use 3 tables to depict this relation.

![](../../../assets/Images/Pasted%20image%2020230902185433.png)

In the example shown , `prod_code` and `supplier_no` are foreign keys in the new SUPPLIER_PRODUCT relation. The primary key of the new relation must also include both these foreign keys, unless a surrogate/artificial key is produced

Here, the primary keys of the SUPPLIER table and the PRODUCT key are used as the **composite key** for the new SUPPLIER_PRODUCT table.

- **One to one**

Here the primary key of each table can be the foreign key of the other table according to your preference. No order here.

![](../../../assets/Images/Pasted%20image%2020230902190117.png)

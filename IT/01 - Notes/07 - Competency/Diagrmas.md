
- There are diagrams drawn in different levels, like mentioned in [[04 - Examines the Structured System Analysis and Design Methodology (SSADM)#Diagram map]] Therefore, first we are going to take a look at `Business Activity Model` diagrams.

### Business Activity Model Diagrams

![](../../../assets/Images%201/Pasted%20image%2020230513185643.png)

#### Important points
- An event should be triggered to start an event
- When drawing the diagrams, actors with direct interactions with the database are included, other actors and their activities aren't included in the diagram.  


![](../../../assets/Images%201/Pasted%20image%2020230513190324.png)

### Example

![](../../../assets/Images%201/Pasted%20image%2020230513190948.png)

- Actors and their activities

| Actors | Activities |
| ---- | ---- |
| Customer | makes a book enquiry |
|  | makes the payment |
|  | collects the book |
| Sales Assistant | goes through book details |
|  | Checks for the availability of the book in stock |
|  | refers to hold-on requests |
|  | checks if the book status is available |
|  | makes a reply to enquiry |
|  | takes customers personal details |
|  | places a hold-on request |
| Cashier | refers to the hold-on request |
|  | finds the relevant hold-on request |
|  | accepts the payment if found a relevant request |
|  | issues a payment receipt |
|  | finalizes the sale |
|  | allows the customer to take the book |
|  | takes a copy of the payment receipt |
|  | compiles a sales report using the payment receipt |
|  | sends the sales receipt to the owner |
|  | updates the book details in the Inventory |
|  | adds the book details to the inventory file |
| Owner | supplies books to Bookland |
|  | Sends details of books to Cashier |

From these activities that these actors do, only the activities that affects the database system is needed to be taken in to consideration when designing the system. 
 - Cashier making a hold-on request
 - Cashier referring to the book inventory
Because considering other actions would be pointless as they don't affect the system.
-  Customer reserving a book (even though this indirectly interacts with the database this is not taken, only direct links are taken in to consideration)
- Owner sending the book details to the Cashier

![](../../../assets/Images%201/Pasted%20image%2020230513195923.png)

>Actions in the encirecled part are the only actions which have a direct link with the database. So those are the only actions which should be included in the finalized system.

Like said in 7.4 there are 2 types of functions as functional and non-functional
- **Functional requirements** - main task that we want our system to do (A teller machine giving us info about money)
- **Non-functional requirement**. - other requirements that support the main functions/tasks (The teller machine having a touch screen)

These both types can also be divided as Essential requirements and Nice-to-have requirements.

![](../../../assets/Images%201/Pasted%20image%2020230513202655.png)


![](../../../assets/Images%201/Pasted%20image%2020230527201525.png)
![](../../../assets/Images%201/Pasted%20image%2020230527201545.png)
![](../../../assets/Images%201/Pasted%20image%2020230527201554.png)

---
### Context Diagram (Level 0 DFD)
- This is the first most level DFD diagram with the highest level of abstraction
- This **shows how the system interacts with the external entities**
- Provides an over-view of the whole system in a single process.

![](../../../assets/Images%201/Pasted%20image%2020230527201816.png)

- Also, we can use `dotted lines` to specify and relation between 2 external entities
![](../../../assets/Images/Pasted%20image%2020230607134421.png)

![](../../../assets/Images%201/Pasted%20image%2020230527202529.png)

This is a table we create for the easy understanding of what should be included in the context diagram. This table represents,
- Who the external entities are
- Who the Source and the Recipient are
- Data which passes by the sender to the source

Once you have the table made, then you can go and draw the diagram as below.

![](../../../assets/Images%201/Pasted%20image%2020230527202638.png)

---
### Document Flow Diagram
- [[04 - Examines the Structured System Analysis and Design Methodology (SSADM)#Document flow diagram|Part 4]]

![](../../../assets/Images/Pasted%20image%2020230607130456.png)

- Document Flow Diagram for the 2017 AL past paper question example

| Sender          | Document         | Recipient       |
| --------------- | ---------------- | --------------- |
| Customer        | Call             | Sales Assistant |
| Customer        | Book enquiry     | Sales Assistant |
| Customer        | Personal details | Sales Assistant |
| Sales Assistant | Enquiry Reply    | Customer        |
| Customer        | Payment          | Cashier         |
| Cashier         | Sales report     | Owner           |
| Owner           | Book details     | Cashier         |

![](../../../assets/Images/Pasted%20image%2020230607133848.png)


Here we dont include the call as its the triggering event and its only shown in the Business Activity Model Diagram

---
### Level 1 DFD

![](../../../assets/Images%201/Pasted%20image%2020230527201605.png)
![](../../../assets/Images%201/Pasted%20image%2020230527201612.png)

![](../../../assets/Images/Pasted%20image%2020230607145519.png)

---
### Level 2 DFD

In this level, the same diagram is expanded more. The process block which include the processes done by each and every entity is expanded and rewritten with its relation with the external entities. Some changes happen in the way the block is drawn.
1. Processes of the entity is written in the header of the block
2. The body will contain separate blocks containing the processes written inside

Other things are pretty much the same, all the other relations are shown from arrows.
 
![](../../../assets/Images/Pasted%20image%2020230611163734.png)


![](../../../assets/Images/Pasted%20image%2020230611170210.png)
#### Elementary Process 

If a process is no longer decomposable, it is called an elementary process. We use the following symbol to denote that in the Level 2 DFDs

![](../../../assets/Images/Pasted%20image%2020230611170501.png)

Data is required to decide whether a process is decomposable or not, so if not said, it should be kept as a normal process which can be decomposed.

We can describe the elementary process using a table as follows
1. It is written in plain English as a pseudo code.
2. This should contain enough details to write the program specification.

![](../../../assets/Images/Pasted%20image%2020230611170617.png)

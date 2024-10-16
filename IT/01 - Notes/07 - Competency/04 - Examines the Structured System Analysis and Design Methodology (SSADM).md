
# Examines the Structured System Analysis and Design Methodology (SSADM)

![](../../../assets/Images%201/Pasted%20image%2020230429185034.png)

There are many structured methods of SAD. 
- SADT
- Structured Design
- Yourdon Structured Method

#### Why do we need a standard method for SAD?
```
Different organizations used these different methods to analysis the system and design the system. Hence the Documentations were different. As a result new developer couldn't understand the pictures and symbols that used in the system. Hence UK government wanted to have one standard method for government development and government asks particular company to develop one standard method.
	- SSADM - UK standard!                 
```

#### What is SSADM?

```
Structured System Analysis and Design Method (SSADM) is a standard for system analysis and application design.
```

##### **Properties of SSADM**
- Used for systems with stable and known requirements which doesn't change often
- It was developed in early 1980s in the U.K
- Development stage is not a very important stage.
- Requires to complete one stage before starting the next
- Have to do feasibility study, requirement analysis and design again and again (suitable for waterfall model)
- As a result SSADM can apply for the system that system requirements are relatively stable and clear. (i.e Library System)

All the Information Systems has two aspects such as **data** and **process**

#### Object-oriented methodology (Object-oriented System Analysis and Design -OOSAD)

```
OOSAD used to design a system as a collection of objects that work interactively
```

In mid-90’s company call **Rational** recruited above 3 people to develop one method. Then Rational released that as **UML** (`Unified Modeling Language`) and Rational Rose is a tool for that.
- **Grady Booch** proposed `Booch Method for OOSAD.`
- **James Rambo** proposed` Object Modeling Techniques` 
- **Ivan Jakobsan** proposed` OOSE (Object Oriented Software Engineering)`

![](../../../assets/Images%201/Pasted%20image%2020230429190037.png)

##### **Properties of OOSADM**
- Best for systems with requirements that changes often
- Uses visual modeling to improve communication

#### What is Software Development Life Cycle (SDLC)?

```
SDLC is a process used by the software industry to design, develop and test high quality software
```


![](../../../assets/Images%201/Pasted%20image%2020230429190801.png)

#### Feasibility Study

This is done to study whether the project is feasible or not. This phase can be divided into 4 parts.
- Business Feasibility
- Financial Feasibility - checking whether I have the money to build a project
- Technical Feasibility - checking whether I have the technical knowledge to build a project
- Political and Organizational Feasibility

Can identify the problems at the beginning by doing feasibility study.

#### Requirements Analysis
We have to identify that what are the requirements should be satisfied for the system to be developed

There are 2 main types of requirements.
- **Functional requirements** - main task that we want our system to do (A teller machine giving us info about money)
- **Non-functional requirement**. - other requirements that support the main functions/tasks (The teller machine having a touch screen)

#### Requirements Specification
- Once you identify requirements, and then specify them in detail. It is call **requirement specification**
- This is a legal document which should be written in formal English (with shall and all that)

#### Logical System Specification
- In the sense we design the system to be developed **without considering the technical constraints**
- Logical design is **independent of technology**

#### Physical Design
- Once you have the logical design, then we can transform it into a physical design.
- The physical design is **dependent on the technology**.

### Framework

SSADM has a framework/skeleton. We have to do all the analysis and design things within this frame.

In this framework, 5 modules in SSADM are broken into 7 stages.

![](../../../assets/Images%201/Pasted%20image%2020230429200031.png)

- **Stage 0 (Feasibility study)** 
	- Check whether the project is feasible or not
- **Stage 1 (Investigation of current environment)**
	- Uncover/identify requirements /problems of the current system (manual/computerize)
- **Stage 2 (BSOs - Business System Options)**
	- There are alternative solutions to satisfy those requirements. All solutions satisfy mandatory requirements. **Client has to select one solution** out of those alternative solutions and Analyst can explain the advantages & disadvantages.
- **Stage 3 (Definition of Requirements)**
	- Defining the requirements for the selected solution
- **Stage 4 (TSOS)**
	- Evaluate the technical system options. Find out what are the alternative technical options to transform to the physical design
- **Stage 5 (Logical Design)**
	- Design the future system logically without considering the technical constraints.
- **Stage 6 (Physical Design)**
	- Transform the logical design into the physical design according to the selected technical option.
##### Diagram map
![](../../../assets/Images%201/Pasted%20image%2020230429201503.png)


##### Document flow diagram
Here, there is another diagram called `Document flow digram` between the Context Diagram and the Level 1 DFD.
- This show what documents(physical/soft copy) being passed between the system
- This acts as a bright between the context diagram and the level 1 DFD

![](../../../assets/Images/Pasted%20image%2020230607130112.png)


### Drawing Business Activity Models (BAM)

![[Diagrmas|Diagrmas]]


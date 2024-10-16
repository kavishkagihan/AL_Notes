
# Explores different information system development models and methods

- What is software engineering?

```
Software engineering is a branch of computer science, defined as a process of analyzing user requirements and then designing, building, and testing software application which will satisfy those requirements.
```

- What are the 2 main functions of a software engineer?

```
1. Development of new applications
2. Maintainance
```

- Good Software Engineering Practices Create

```
Successful projects
Business value
Lower stress levels for developers
Happy customers
```

There are 3 main Stakeholders in a software project.
1. **User** (Most important stakeholder) -  Users are the ones who use the system after it has been developed to perform their day to day tasks.
2. **Project Sponsor** - this category of the stakeholders is responsible for the financial aspect of the project and ensuring that the project is completed.
3. **Developer** - this category is usually made up of systems analysts and programmers. The system analysts are responsible for collecting the user requirements and writing system requirements.

### Systems Development Life Cycle (SDLC)

```
The system development life cycle refers to the processing of Strategy Planning, Feasibility Study, System Analysis, System Design, Implementation and Maintenance an information system.
```

#### Steps in the SDLC
1. Strategy planning
2. Feasibility study
3. System analysis
4. System design
5. Implementation
6. Manitainance

**The main objective of system development life cycle**
- to produce high quality information systems that meet or exceed the expectations of the users within the agreed budget and time frame. 

SDLC uses a number of development models to achieve this objective.
1. Waterfall modal
2. Spiral model
3. Agile model
4. Prototyping model
5. Rapid Application Development (RAD) model

#### Waterfall Model

- sequential design model
- next stage starts only after the completion of the previous stage
- first stage is usually drawn on the top and the subsequent stages below and to the left bottom

![](../../../assets/Images%201/Pasted%20image%2020230422190829.png)

- Feasibility Study
	- determines whether the solution considered to accomplish the requirements is practical and workable in the software. Information such as resource availability, cost estimation for software development, benefits of the software to the organization after it is developed and cost to be incurred on its maintenance are considered during the feasibility study.
- Requirement Gathering and analysis
	- All possible requirements of the system to be developed are captured in this phase and documented in a requirement specification document.
- System Design
	- the requirement specifications from first phase are studied in this phase and the system design is prepared. This system design helps in **specifying hardware and system requirements** and helps in defining the overall system architecture.
- Implementation
	- with inputs from the system design, the system is first developed in small programs called units, which are integrated in the next phase. Each unit is developed and tested for its functionality, which is referred to as Unit Testing.
- Integration and Testing
	- All the units developed in the implementation phase are integrated into a system after testing of each unit. Post integration the entire system is tested for any faults and failures.
- Deployment of system
	- Once the functional and non-functional testing is done; the product is deployed in the customer environment or released into the market.
- Maintenance
	- There are some issues which come up in the client environment. To fix those issues, patches are released. Also to enhance the product some better versions are released. Maintenance is done to deliver these changes in the customer environment.

>The biggest challenge of the waterfall model is **adoption to change**. It is **not easy to incorporate new user requirements.**

###### Advantages of Waterfall Model
- Simple, easy to use
- Easy to manage
- Clear documentation
- Better to use when there are fixed requirements.

######  Disadvantages of Waterfall Model
- Difficult to adapt to change
- High amount of risk
- Not good for complex projects
- No working products till the end of SDLC

#### Spiral Model

- combination of a waterfall model and iterative model
- Each phase **begins with a design goal** and **ends with the client reviewing the progress**.
- first mentioned by **Barry Boehm**
- starts with a small set of requirements
- goes through each development phase for those set of requirements

![](../../../assets/Images%201/Pasted%20image%2020230422194540.png)

###### Advantages of Spiral Model
- High amount risk analysis
- Additional functionalities can be added later

######  Disadvantages of Spiral Model
- Can be a costly model
- Risk analysis requires high specific expertise

###### When to use Spiral Methodology?
- In large projects
- when releases are frequent
- when risk and costs evaluation is important
- for medium to high risk projects
- when requirements are unclear or complex
- when changes may require at any time
#### Agile Model

- The Agile model breaks the development process into small parts called iterations or sprints.
- A sprint in agile terms is a well-defined task to be accomplished within a given time
- All stakeholders must meet in person to get the feedback on the sprint before they can move on to the next sprint if any.

![](../../../assets/Images%201/Pasted%20image%2020230422195126.png)

###### Advantages of Agile Model
- Customer satisfaction with rapid delivery
- Continuous attention to technical excellence and good design
- Rapid and flexible responses to change.
- Easy and **fast** addition of requirements and releases.

######  Disadvantages of Agile Model
- Lack of emphasis and documentation
- The projects can easily get take off track as the customer is not clear with what the final outcome they want
- Difficult to assess the effort required at the beginning for some large project.

#### Prototyping Model

- semi-functional simulation model of the actual system to be developed
- make use of prototypes.
- both developers and users to get feedback early
- makes it easy for users to specify their requirements
- makes it easy for developers understanding the requirements of the users 
- 2 main types
	- Evolutionary prototyping - started with clear requirements
	- Throw-away prototyping - started with partial requirements, purpose is to make the requirements clear


#### Rapid Application Development (RAD) Model

![](../../../assets/Images%201/Pasted%20image%2020230422200413.png)

- an adoption of the waterfall model
- targets at **developing software in a short span of time**
- follow the **iterative**
- emphasises on delivering projects in small pieces
- larger projects are divided into a series of smaller projects
- main features of RAD model are that **it focuses on the reuse of templates, tools, processes, and code.**

###### When to use RAD Methodology?
- when a project needs to be produced in a short time span
- when the requirements are known
- when the user will be involved all through the life cycle
- when technical risk is less
- when a budget is high enough to afford designers for modelling 

![](../../../assets/Images%201/Pasted%20image%2020230422201141.png)

###### Advantages of RAD Model
- Minimal planning
- Fast prototyping 
- Developing instead of planning
- Encourage customer feedback
- Quick initial review

######  Disadvantages of RAD Model
- Need a big budget to afford expertise in different fields
- High dependency on modelling skills


| Model       | Advantages                                                               | Disadvantages                                             |
| ----------- | ------------------------------------------------------------------------ | --------------------------------------------------------- |
| Waterfall   | Easy to use                                                              | Difficult to adapt to change                              |
|             | Better to use with known requirements                                    | High amount of risk                                       |
|             | Clear documentation                                                      | No working products till the end of SDLC                  |
| Spiral      | High amount risk analysis                                                | Risk analysis requires high specific expertise            |
|             | Additional functionalities can be added easily                           | Can be a costly model                                     |
| Agile       | Customer satisfaction with rapid delivery                                | Lack of emphasis and documentation                        |
|             | Easy, fast addition of requirements and releases.                        | Difficult to asses the effort required at the beginning   |
| Prototyping | makes it easy for users to specify their requirements                    | Takes a longer time to finish                             |
|             | makes it easy for developers understanding the requirements of the users | User requirements may change often                        |
| RAD         | Minimal planning and fast prototyping                                    | High dependency on modeling skills                        |
|             | Encourage customer feedback                                              | Need a big budget to afford expertise in different fields |
|             | Developing the software in a short period of time                        |                                                           |

#### Incremental vs Iterative

![](../../../assets/Images%201/Pasted%20image%2020230422201716.png)


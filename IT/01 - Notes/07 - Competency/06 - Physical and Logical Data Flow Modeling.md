# Physical and Logical Data Flow Modeling

There are 2 main types of Data Flow Models
1. Physical DFM - The current system
2. Logical DFM - The proposed system to be made

![](../../../assets/Images/Pasted%20image%2020230611172004.png)

>DFD diagrams can be draw to both of these DFMs

#### Testing

There are 2 types of main testing methods
1. White box
2. Black box

| White Box                               | Black Box                                                                    |
| --------------------------------------- | ---------------------------------------------------------------------------- |
| Source code of the application is given | Source code is kept hidden                                                   |
| Done in early stages of testing         | Uses to test whether the required functionalities are working as they should |
| Applied for relatively small unit       | Test cases are taken from the program specification                          |

Also, the testing phase can be divided into 4 parts
1. Unit testing
2. Integration testing
3. System testing 
4. Acceptance testing

![](../../../assets/Images/Pasted%20image%2020230611173808.png)

1. **Unit Testing**
	- testing of individual units of the system
	- done by **programmers**
	- **white box testing** is used
2. **Integration Testing**
	- continues to test the units when they are integrated together
	- done by **Integration testers**
	- either **white box or black box** can be used
3. **System Testing**
	- testing the whole system's functionality
	- done by programmers (not the ones who made the system)
	- **black box** testing is used
4. **Acceptance Testing**
	- testing whether the system is acceptable by the users
	- done by programmers or users who developed the system
	- **black box** testing is used


#### Deployment

There are 4 types of deployments
1. Parallel deployment
2. Direct deployment
3. Phased deployment
4. Pilot deployment

![](../../../assets/Images/Pasted%20image%2020230611174522.png)

1. **Parallel Deployment**
	- duplication of effort can be seen (ie data must be entered in both systems)
	- time-consuming
	- most bulletproof method
2. **Direct Deployment**
	- smallest method of deployment
	- implementation is faster
	- least expensive deployment
	- can be hard on users as they have to learn a whole new system from scratch
	- if 2 systems are incompatible, this deployment should be used
3. **Pilot Deployment**
	- Can get valuable feedback on the system while using the other system
	- Easy on users
	- implementation risk is high (what if the system fails, the whole location gets shut down)
4. **Phased Deployment**
	- No implementation risk as the whole system isn't being replaced
	- Information learned from the previous stages can be used to make the other better.
	- Can be confusing for users to have some using the older system and some using the new system
	- This can lead to quality issues.


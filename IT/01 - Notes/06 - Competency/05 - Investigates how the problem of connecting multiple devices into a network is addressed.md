# Investigates how the problem of connecting multiple devices into a network is addressed

- What is a Network Architecture

```
Network architecture describes how a network is arranged and how resources are coordinated and shared
```

### Topologies

```
A network can be arranged or configured in several different ways. This arrangement is called the network’s topology
```

#### Bus Topology

Each device is connected to a common cable called a bus or backbone, and all communications travel along this bus. ( A **Coaxial** cable is used as the backbone)

![](../../../assets/Images%201/Pasted%20image%2020230128132540.png)

**Advantages**
- Easy to setup
- Cost is very less
- Best suited for small networks

**Disadvantages**

- Highly dependent on the central bus
- Cable length is limited, therefore limited number of nodes can be connected.
- Not easy to isolated system faults.
- **Each device in the network sees all the data that's been transferred,**

#### Ring Topology

Each device is connected to two other devices, forming a ring. When a message is sent, it is passed around the ring until it reaches the intended destination.

![](../../../assets/Images%201/Pasted%20image%2020230128132844.png)

**Advantages**
- A central server is not required
- Since unidirectional traffic, high speed
- Less costly than a star topology.

**Disadvantages**
- Failure of a single node in the network can cause the entire network to fail
- Data transmission is slower
- Highly dependent on the wire connecting the network nodes

#### Star Topology

Each node is connected to a central node directly.

![](../../../assets/Images%201/Pasted%20image%2020230128133338.png)

**Advantages**
- Simple to operate
- Can achieve device isolation
- Easy to identify system faults
- Analysis of network traffic is easy
- Adding or removing nodes is easy

**Disadvantages**
- Failure in the central node results in complete breakdown in the system
- Setup costs a lot
#### Mesh Topology

Each node have more than one connection to the other nodes. There is an equation we can use to find the number of connections we get with the number of nodes

```
n = number of nodes

n(n - 1) / 2 = number of connections
```

![](../../../assets/Images%201/Pasted%20image%2020230128133924.png)

**Advantages**
- Possible to transmit data from one node to many other nodes at the same time
- Failure in a single node doesn't affect any other nodes
- Can handle heavy traffic
- Easy to identify faults.

**Disadvantages**
- High complexity
- Cost is high
- Connections that server no purpose, maybe exist for no reason.

| Topology | Advantages                               | Disadvantages                                                           |
| --------- | ---------------------------------------- | ----------------------------------------------------------------------- |
| Bus       | Best suited for small networks           | Each device in the network sees all the data that's been transferred,   |
|           | Easy setup, Low cost                     | Not easy to isolated system faults.                                     |
| Ring      | Since unidirectional traffic, high speed | Data transmission is slower                                             |
|           | Less costly than a star topology.        | Highly dependent on the wire connecting the network nodes               |
| Star      | Simple, Device isolation                 | Setup costs a lot                                                       |
|           | Easy to identify system faults           | Failure in the central node results in complete breakdown in the system |
| Mesh      | Can handle heavy traffic                 | High cost, complexity                                                   |
|           | Easy to identify faults                  | Connections that server no purpose, maybe exist for no reason.          |

### Switch and Hub

![](../../../assets/Images%201/Pasted%20image%2020230128134755.png)

![](/assets/Images/Pasted%20image%2020230901192026.png)

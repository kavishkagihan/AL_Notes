# Explores the role of Media Access Control (MAC) protocol

### Local Area Network

```
Networks with nodes that are in close physical proximity within the same building are called local area networks
```

LAN networks are mainly used to share resources such as printers like costly devices.

The main benefits of a LAN are:
- Flexibility
- Economical advantages

>**A gateway is used to link one LAN to another.**

#### Identifying devices in the network

When a router(DHCP server in specific) is not present, MAC address is used to identify the devices in a LAN.
#### Protocol

```
Set of certain rules which has to be followed by every connected device.
```

#### Multiple Access Protocol

```
Multiple access protocols are a set of protocols operating in the Medium Access Control sublayer (MAC sublayer) of the Open Systems Interconnection (OSI) model. 
```

**These protocols allow a number of nodes or users to access a shared network channel**

The main purpose of this protocol is to prevent collisions when 2 or more devices communicate at once

There are 3 Multiple Access Protocols
1. Random access protocols
2. Controlled access protocol 
3. Channelization

![](../../../assets/Images%201/Pasted%20image%2020230130103421.png)

##### ALOHA, Slotted ALOHA

- This is a random access protocol, meaning that **it can send data at any time**.
- Developed by **Normon Abramson**
- This was firstly introduced to **wireless networks**

In this, multiple stations can transmit data at the same time and can hence lead to **collision and data being garbled.**

![](../../../assets/Images%201/Pasted%20image%2020230130104036.png)

To prevent collisions like this 2 different methods are used.
1. Pure ALOHA
2. Slotted ALOHA

###### Pure ALOHA

![](../../../assets/Images%201/Pasted%20image%2020230130104621.png)


- When Station 1 send data to the common medium, at that time other stations are not sending (transmitting) anything. Therefore, Frame 1.1 is survived. Frame 3.2 also survived, and other frames are colliding with each other.
- When two or more stations transmit simultaneously, there is collision and the frames are destroyed.
- In pure ALOHA, whenever any station transmits a frame, it **expects the acknowledgement from the receiver**.
- If acknowledgement is not received within a specified time, the station assumes that the frame (or acknowledgement) has been destroyed

> If such this happens, the sender waits for a **random time** (back off time) and re-sends data. Since the waiting time is random, another collision probability is decreased. 

> Even though they aren't transmitted in the same time, if the first bit of a new frame overlaps with just the last bit of a frame almost finished, **both frames will be totally destroyed** and both will **have to be retransmitted**.

![](../../../assets/Images%201/Pasted%20image%2020230130105135.png)

###### Slotted ALOHA

This was invented to improve the efficiency of pure ALOHA. 

> Unlike in pure ALOHA, in here you can't transmit anytime you have data. Time is divided into discrete slots. Data is transmitted only at the **beginning of the slot**. If you miss a time slot, you will have to wait till the next time slot comes.

ote
![](../../../assets/Images%201/Pasted%20image%2020230130105821.png)

But still **collisions can occur  if 2 devices send data at the beginning of same time slot.** But the probability for collisions are greatly reduced compared to pure ALOHA.

![](../../../assets/Images%201/Pasted%20image%2020230130110110.png)

Here station 2 and 3 have transmitted frame 2.1 and 3.1 in the same time slot, resulting  in collision.

##### Ethernet

- This was introduced to **wired networks**
- This is introduced according to the IEEE 802.3 standards
- Advantages and reasons to use Ethernet:
	- Flexibility
	- Low cost
	- Easy to understand
- Ethernet standards
	- operates in Physical layer and Data link layer
- There are 2 sublayer in Ethernet
	- LLC (Local Link Control)
	- MAC

![](../../../assets/Images%201/Pasted%20image%2020230130111118.png)
![](../../../assets/Images%201/Pasted%20image%2020230130111433.png)

##### Media Access Control (MAC) Address
- Ethernet Address is another name given to MAC address.
- MAC address is an 48 bit  address

![](../../../assets/Images%201/Pasted%20image%2020230130111903.png)

###### Types of Messages

Three different methods of sending messages over computer networks
1. Unicast
2. Multicast
3. Broadcast

![](../../../assets/Images%201/Pasted%20image%2020230130112024.png)

##### CSMA/CD (Carrier Sense Multiple Access with Collision Detection).

```
This is a technology used to prevent collisions in Ethernet/wired networks.
```

> It utilizes **coaxial cables and early versions of twisted pair cables.**

###### How CSMA/CD works
- A computer **first listens** to the network media. If the media is idle, the computer sends its data (**Carrier Sense**).
- But if two computers send data at the same time, a collision will happen. Priorities are **not** assigned to particular stations (**Multiple access**)

![](../../../assets/Images%201/Pasted%20image%2020230130113043.png)

- When collision happens, computers will **wait random amount of time and retry to send the data.** (**Collision detection**)

![](../../../assets/Images%201/Pasted%20image%2020230130113139.png)


![](../../../assets/Images%201/Pasted%20image%2020230130114137.png)

![](../../../assets/Images%201/Pasted%20image%2020230130114239.png)
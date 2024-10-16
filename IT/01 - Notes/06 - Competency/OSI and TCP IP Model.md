# OSI Model

OSI model - _The Open Systems Interconnection model_


![](../../../assets/Images%201/Pasted%20image%2020221021152240.png)

This model was a conceptual model that wasn't actually built. The model that we use in the present day is the TCP/IP model. 

# TCP/IP Model

TCP/IP model is a model that was built by combining some  layers in the OSI Model itself. The 7 layers in the OSI model is combined as below.

![](../../../assets/Images%201/Pasted%20image%2020221021152538.png)

- Physical and the  Data Link layers are combined to make the **Network Access layer.**
- The Application, Presentation and Session layers are combined to make the **Application layer.**
- And the Network layer in the OSI model is known as **Internet Layer** in the TCP/IP model.

## Protocol Data Unit

The reason why these are grouped in this order is because of the **Protocol Data Unit** of these layers. Simply said, when data passes through these layers, they are being called with different names.

![](../../../assets/Images%201/Pasted%20image%2020221021153236.png)

- In the OSI model throughout the Application, Presentation and the Session layer the raw data is flown. Nothing yet has happened to the data. Therefore, in the TCP/IP model all these 3 layers are grouped into one layer 
- But when it comes to the Transport layer, these data are broken in to pieces called **Segments**
- And in the Network Layer they are called Packets, in the Data Link layer they are called Frames and at last Bits in the Physical Layer

## Devices 

![](../../../assets/Images%201/Pasted%20image%2020221021154115.png)

- A couple of different things to mention here, if you look at the NIC and the WAP, it's in both Physical and Data Link layer thants because it's a **Network Access Layer** device (according to the TCP/IP Model)
- Multilayer switch = Router + Switch. 

## Protocols

![](../../../assets/Images%201/Pasted%20image%2020221021154606.png)

- MAC - Media Access Control
- ARP - Address Resolution Protocol
- Ethernet 802.3 - Wired Ethernet
- Ethernet 802.11 - Wireless Ethernet
- SONET - Fiber Connections 

## Functions of the Layers

### Application Layer

- **Application Layer**
	- Applications that the end-user uses, I.e Web Browsers
- **Presentation Layer**
	- Data is formatted, converted, encrypted, compressed and sent to the user. This is where MIME types come in 
- **Session Layer** 
	- Opening, closing and managing session between application processes - 

### Transport Layer
- Services the upper layers with **ports** so that it can facilitate end-to-end communications. 
- For this protocols like TCP (Transmission Control Protocol) which is reliable and UDP (User Data gram Protocol) which is not reliable are used.
- Connection oriented with 3 way handshake (for TCP)
- Flow control
- Error correction - up to a certain extent

### Internet Layer / Network layer

- Providing host addressing with IP addresses
- Routing and Forwarding is performed (Switching packets out of the correct interface)
- Maintaining the QoS (Quality of Service) - When watching a video, more bandwidth is needed rather compared to sending an email

### Network Access layer

- **Data Link Layer**
	- There are 2 sub-layers as LLC (Logical Link Control) and MAC (Media Access Control)
	- Provides Error checking (If there is a corrupted frame, it will drop the frame)
- **Physical Layer**
	- Encoding the data into binary (1,0) with electrical pulses or link rays


# Encapsulation and Decapsulation

![](../../../assets/Images%201/Pasted%20image%2020221021161934.png)

When going from top to bottom, each layer adds a header to the data
- In the Transport layer, the data is broken into Segments are the **Transport header** is added - header includes information like source port and destination port 
- Then the **Network header** is added in the Network Layer -  header includes information like source and destination IP address)
- And then the **Frame header** is added in the Network Access layer (specifically in Data link layer) - header includes information like source and destination MAC addresses. Also, a **Frame trailer** is added with a hash related to the packet to make sure that no corruption was occurred. 
- At last, frames are converted in to Bits as 1s and 0s
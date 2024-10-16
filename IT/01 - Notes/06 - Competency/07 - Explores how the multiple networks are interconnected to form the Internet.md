# Explores how the multiple networks are interconnected to form the Internet


1. What is a Gateway
```
A gateway is a router equipped with all the information which leads to route packets to the destination host.
```

2. What is an IP address?

```
IP addresses are unique addresses assigned to each device on the network to identify the location of the device
```

3. What are the 2 types of IP addresses?

```
IP Version 4 (IPv4) is 32 bits long and can address up to 4 billion devices.
IP Version 6 (IPv6) is 128 bits long and is plenty enough to address a huge number of networkable devices.
```

##### Dotted decimal notation

- This notation is used for human convenience
- Each bit is represented from 0-255
`192.160.32.5`


### IPv6 

- Has 128 bits per 1 address

### IPv4 classes, Ranges and subnets
- There are typically 5 classes in IPv4 addresses

![](/assets/Images%201/Pasted%20image%2020230206101424.png)

**Similarities between the subnet and the IP address**
- They both have 4 octet.
- Both are 32bit addresses

**Difference between the subnet and the IP address**
- When you convert an IP to binary, 0s and 1s are mixed up together. But in subnet mask, 0s start after finishing with 1s

Talking about the rangers and subnets, different classes have different ranges and masks. There are some points that you need to know to understand the above table better.
- The first octet of the IP address always depicts the Class.
	- `0-127` -> Class A
	- `128-191` -> Class B
	- `192-223` -> Class C
- When calculating the range, the 1st 
	- 1 bit of Class A
	- 2 bits of Class B
	- 3 bits of Class C
	- 4 bits of Class D
	- 5 bits of Class E **never changes**. This is used to represent the network class throughout the range of the IPs.
- Like said above, 
	- first octet of Class A
	- first 2 octets of Class B
	- first 3 octets of Class C are used to **represent the network part in the IP address**. The other octets are reserved to **represent the host part**s.
- To calculate the **number of networks we can create** in different classes, you have to get the 2nd power of the bits in the  network octet.
	- Class A -> The first octet is used to represent the class, meaning that 8 bits are used. So theoretically the number of networks we can create should be `2 ** 8`, But, here the **first bit is unchanged throughout the range**, so actually the changeable networks bits are 7. Therefore, the real number of networks that can be created is `2 ** 7 = 128` (same goes for other classes)
- To calculate the **number of host in these networks**, you have to get the 2nd power of number of bits you have left for the hosts.
	- Class A -> Only the first octet is reserved to represent the IP class so the rest 3 octets are to represent the host (`8 * 3 = 24`). Therefore, ( `2 ** 24 = 16, 777, 216`) there are `16, 777, 216`  IPs. But 2 IPs are reserved for the network IP address and the broadcast IP address. So the number of usable host IPs are `2 ** 24 - 2 = 16, 777, 214` (Same goes for other classes)
	- We can calculate the network IP using the IP and the Mask like this. You convert them to binary and do AND operation to them. ![](../../../assets/Images%201/Pasted%20image%2020230206110714.png)
	- Here once this is done, if the host part of the IP is all 0s, it's the network IP, if the host part is all 1s it's the broadcast IP  
	  ![](../../../assets/Images%201/Pasted%20image%2020230206111253.png)

### Assignment of IP addresses
The institute that handles this assignment of IPs is called `IANA (Internet Assinged Number Authority)`

![](../../../assets/Images%201/Pasted%20image%2020230206105118.png)

#### Sub-netting

```
The process of dividing a single subnet to 2 or more networks is called sub-netting. 
```

**Purpose of sub-netting**
- To help relieve network congestion
- Improve network performance
- Enhance security
- To overcome the problem of depletion of network address of a 32-bit addressing scheme

![](../../../assets/Images%201/Pasted%20image%2020230206105804.png)

> The usage of the subnet mask is to find out the number of host bits and network bits

Lets take an example where you are asked to subnet `192.248.154.0/24` to 6 networks, each having minimum 30 hosts. Steps are as below.
1. First you have to get the host changeable bits that are needed to represent the number of hosts we need to each network (30 in this case)
	- `/24` -> `255.255.255.0` means that we have last 8 bits as the host bits. To represent 30 hosts we need at least 5 bits `2 ** 5 = 32`, this means that the hosts bits of the new 6 subnets we create is 5.  
	- And the rest 3 bits (`8 - 5 = 3`) are reserved as network bits to the new subnet
2. Now that we know that, then we need to create the actual subnets. For that, we use the method we use to create the truth table.  (We create a truth table with 3 inputs, since we only need 6 subnets, we only get the first 6 entries) Then those bits are used as the network bits for net subnet.
	
	| id  | host bit |
	| --- | -------- |
	| 1   | 000      |
	| 2   | 001      |
	| 3   | 010      |
	| 4   | 011      |
	| 5   | 100      |
	| 6   | 101      |
	| 7   | 110      |
	| 8   | 111      |


3. Using these we can create our 6 networks as follows.

	| Orig. Network + New subnet network bits | Host bits | Decimal representation (New subnet network bit + Host bit) |
	| --------------------------------------- | --------- | ---------------------------------------------------------- |
	| 192.248.154.000                         | 00000     | -> 000 00000 = 0                                           |
	| 192.248.154.001                         | 00000     | -> 001 00000 = 32                                          |
	| 192.248.154.010                         | 00000     | -> 010 00000 = 64                                          |
	| 192.248.154.011                         | 00000     | -> 011 00000 = 96                                          |
	| 192.248.154.100                         | 00000     | -> 100 00000 = 128                                         |
	| 192.248.154.101                         | 00000     | -> 101 00000 = 160                                         |
	- Then we need to convert these binary values to decimal in order to get the real subnets
	![](../../../assets/Images%201/Pasted%20image%2020230206124832.png)
	- Likewise, we need to convert all these 6 to decimal. Once that's done, we can get the IP net subnets as below
	```
	192.248.154.0
	192.248.154.32
	192.248.154.64
	192.248.154.96
	192.248.154.128
	192.248.154.160
	```
4. Finally using this we can get the network ID and the broadcast ID including total usable host IPs

| Network         | N/A and B/A | Actual Network  | N/A and B/A     | Usable Host IP Range |
| --------------- | ----------- | --------------- | --------------- | -------------------- |
| 192.248.154.000 | 00000       | 192.248.154.0   | 192.248.154.0   | 192.248.154.1        |
|                 | 11111       |                 | 192.248.154.31  | 192.248.154.30       |
|                 |             |                 |                 |                      |
| 192.248.154.001 | 00000       | 192.248.154.32  | 192.248.154.32  | 192.248.154.31       |
|                 | 11111       |                 | 192.248.154.63  | 192.248.154.62       |
|                 |             |                 |                 |                      |
| 192.248.154.010 | 00000       | 192.248.154.64  | 192.248.154.64  | 192.248.154.63       |
|                 | 11111       |                 | 192.248.154.95  | 192.248.154.94       |
|                 |             |                 |                 |                      |
| 192.248.154.011 | 00000       | 192.248.154.96  | 192.248.154.96  | 192.248.154.97       |
|                 | 11111       |                 | 192.248.154.127 | 192.248.154.126      |
|                 |             |                 |                 |                      |
| 192.248.154.100 | 00000       | 192.248.154.128 | 192.248.154.128 | 192.248.154.129      |
|                 | 11111       |                 | 192.248.154.159 | 192.248.154.158      |
|                 |             |                 |                 |                      |
| 192.248.154.101 | 00000       | 192.248.154.160 | 192.248.154.160 | 192.248.154.161      |
|                 | 11111       |                 | 192.248.154.191 | 192.248.154.190      |

5. As the last step we have to find the subnet mask of our new network.
	- Since the networks bits that were newly added to the subnet is 3, we add that to out earlier subnet mask which is 24 resulting 27. Therefore, `192.248.154.0/27,192.248.154.32/27` likewise `/27` is the new subnet mask for our 6 subnets. 

- In example cases you might be given the subnet mask of a subnetted  network and a corresponding IP of that network and asked to calculate the network and the broadcast IP of that network. This is how thats done. Let's take an example case of a network with IP `182.12.150.195` and a subnet mask of `255.255.192.0`. Now we need to find the network IP and the broadcast IP.
	- **Network IP**
	![](https://youtu.be/83Z2ICDChzM)
		- We need to compare the octets of the IP and the subnet mask separately according to a certain criteria.
		- Those criteria are, 
			- If we have `255` in the subnet relevant to the octet of the IP, then that relevant octet of the network IP is the same as the IPs one.
			![](/assets/Images/Pasted%20image%2020230906125845.png)
			- If we have `0` in the subnet of a relevant octet, we just ignore whatever it is in the IP, and write `0` in the corresponding octet of the network IP.
			 ![](/assets/Images/Pasted%20image%2020230906130055.png)
			 - If we have any other number(n) except 0 or 255, we subtract that number from `256` (`256 - n = r`)and then multiple the remainder so that it becomes the highest possible value that doesn't exceed the number in the relevant octet of the IP address
			 ![](/assets/Images/Pasted%20image%2020230906130502.png)
		- According to our example, here is how thats done
		 ![](/assets/Images/Pasted%20image%2020230906131155.png)
	- Broadcast IP
	![](https://www.youtube.com/watch?v=1pZNjRZLNqI)
		- Here similar criteria are followed. 
			- If we have `255` in the subnet relevant to the octet of the IP, then that relevant octet of the broadcast IP is the same as the IPs one.
			![](/assets/Images/Pasted%20image%2020230906131847.png)
			-  If we have `0` in the subnet of a relevant octet, we just ignore whatever it is in the IP, and write `255` in the corresponding octet of the network IP.
			![](/assets/Images/Pasted%20image%2020230906131748.png)
			- If we have any other number(n) except 0 or 255, we subtract that number from `256` (`256 - n = r`)and then multiple the remainder until it becomes the closest highest number to the relevant octet of the IP and subtract 1 from it.
			![](/assets/Images/Pasted%20image%2020230906132522.png)
		- According to our example here is how we find the broadcast IP
		![](/assets/Images/Pasted%20image%2020230906132901.png)
			
			

#### Class C IP table - The sunny way 
![](https://www.youtube.com/watch?v=ecCuyq-Wprc)

![](../../../assets/Images%201/Pasted%20image%2020230213094118.png)

#### Class B IP table

![](https://www.youtube.com/watch?v=gxLKiCOus2I)


![](../../../assets/Images/Pasted%20image%2020231013152549.png)

#### Classless Inter Domain Routing (CIDR)

Instead of full class A, B or C networks, organizations can be allocated any number of addresses using this scheme. **This scheme can help reducing the growth of the router tables.**

#### Private IPs

Three sets of address ranges are used for private use.
- 10.0.0.0 – 10.255.255.255 (10.0.0.0/8) – 16M addresses
- 172.16.0.0 – 172.31.255.255 (172.16.0.0/12) - 1M addresses 
- 192.168.0.0 – 192.168.255.255 (192.168.0.0/16) – 64k addresses




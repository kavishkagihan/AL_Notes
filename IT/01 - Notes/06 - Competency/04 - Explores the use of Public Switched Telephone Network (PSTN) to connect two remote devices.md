
# Explores the use of Public Switched Telephone Network (PSTN) to connect two remote devices

- What is public switch telephone network? (PSTN)

```
The PSTN (Publicly Switched Telephone Network) is the worldwide collection of interconnected public telephone network that carries your voice calls (Analog Telephone calls) when you call from a landline or cell phone.
```

PSTN is also referred as landline/ Plain Old Telephone Service (POTS), **PSTN is a circuit switch network.**

- Circuit switching

![](../../../assets/Images%201/Pasted%20image%2020230128124524.png)

>When transferring data with circuit switching, **a dedicated route of nodes has to be used**. Since every node in the circuit switching costs money, its very **expensive**. Therefore, these days instead of this, packet switching is used. 

- Packet switching
![](../../../assets/Images%201/Pasted%20image%2020230128125016.png)

>With packet switching, **a dedicated route is not taken**, but **all the nodes are shared.** Therefore, it's **less expensive** than Circuit switching.

Originally, PSTN was only an **analog system**, but it is now almost entirely digital. Only the very oldest and most backward parts still use analog.

In terms of physical media, PSTN is a mix of **copper wires**, **fiber optics** and **wireless**.

| Circuit Switching               | Packet Switching             |
| ------------------------------- | ---------------------------- |
| Uses a dedicated route of nodes | Uses a shared route of nodes |
| Expensive                       | Less expensive               |


### PSTN – Dial Up Connections

These Dial Up connections require a **modem** and a **phone line** to dial into a service provider’s node, in order to get the connection

#### **Modulation and Demodulation**

- Modulation is converting digital signals to analog signals so that it can be transferred in a network to the destination
- Demodulation is converting the analog signal back to its digital form so that it can be processed.

> Modulation -> Digital to Analog
> Demodulation -> Analog to Digital


![](../../../assets/Images%201/Pasted%20image%2020230128130509.png)

##### Different modulation schemes

- Pulse Code Modulation (PCM) is one method in which the samples of an analog signal are taken
- Analog voice data must be translated into a series of binary digits before they can be transmitted. With PCM, the amplitude of the sound wave is sampled at regular intervals and translated into a binary number
- The difference between the original analog signal and translated digital signal is called **quantizing error**


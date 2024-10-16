# Signal transmission media

### Types of transmission media

There are 2 types of transmission media.
1. Guided / Wried / Bound
2. Unguided / Wireless / Unbound

![](../../../assets/Images%201/Pasted%20image%2020230107124459.png)

#### Wired or Guided Media or Bound Transmission Media

Examples for guided media
1. Twisted pair
2. Coaxial
3. Fiber optic

Common features for all guided media
1. High speed
2. Secure
3. Used for shorter distances

##### Twisted-pair cable
	
- consists of pairs of copper wire that are twisted together.
- used in **telephone lines** and **Ethernet cables.**
- There are 2 types of TP
	- Shielded Twisted Pair (STP) Cable
	-  Unshielded Twisted Pair (UTP) Cable

| Schema                                | STP       | UTP                       |
| ------------------------------------- | --------- | ------------------------- |
| Performance in higher data rates      | High      | Low                       |
| Speed                                 | Fast      | Slow                      |
| Installation and manufacturing        | Difficult | Easy                      |
| Transmission distance (comparatively) | Long      | Short (due to attenution) |
| Size                                  | Bulky     | Smaller                   |

##### Coaxial cable
- a high-frequency transmission cable
- replaces the multiple wires of telephone lines with a single solid-copper core.
- has over 80 times the transmission capacity of twisted pair
- used in **Cable TVs** and **analog television networks** and **CCTVs**

Advantages
- High Bandwidth
- Easy to install
- Better noise immunity
- Inexpensive

Disadvantages
-  Single cable failure can disrupt the entire network

##### Fiber-optics cable 

- transmits data as pulses of light through tiny tubes
- recently speeds of 1 petabit per second
- it is lighter, faster, and more reliable at transmitting data (compared to coaxial)

Advantages
- Increased capacity and bandwidth
- Light weight
- Immunity to electromagnetic interference
- Less signal attenuation

Disadvantages
- High cost
- Breakable
- Difficult to install and maintain

| Schema                       | Twisted pair              | Coaxial                | Fibre optics      |
| ---------------------------- | ------------------------- | ---------------------- | ----------------- |
| Speed                        | Slower                    | Faster than TP (80x)   | Fastest           |
| Bandwidth                    | 0-100 MHZ                 | 100-600 MHZ            | 0-1 GHZ           |
| Installation and maintenance | Easy                      | Easy                   | Hard              |
| Supported distance           | short distance            | long distance          | longest distances |
| Signal attenuation           | high  (UTP)               | low                    | lowest            |
| Durability                   | durable than fibre optics | durable than TP        | Not very durable  |
| Cost                         | Cheapest                  | More expensive than TP | Most expensive    |
| Electromagnetic Interference | Lower                     | Higher                 | Lowest            |

#####  Bandwidths of guided transmission media

![](../../../assets/Images%201/Pasted%20image%2020230107130645.png)


#### Wireless or Unguided Media or Unbound Transmission Media

Wireless connections do not use solid materials in  sending and receiving signals. There are three types of unguided media such as,
1. Radio wave 
	- **AM and FM radios**, **cordless phones**, **Wi-Fi** and **Satellites** use Radio waves for transmission.
2. Microwave (goes longest)
	- These are majorly used for **mobile phone** communication and **television** distribution.
3. Infrared waves
	- Used in **TV remotes, wireless mouse, keyboard, printer**, etc

**Common features for all unguided media**
- Signal is broadcasted through air
- Less Secure 
- Used for larger distances

### How latency, bandwidth, noise, attenuation, and distortion affect signal transmission

#### Latency / RTT (Round Trip Time)

```
Latency is a networking term to describe the total time it takes a data packet to travel from one node to another.
```

#### Bandwidth

```
The data carrying capacity of a channel or medium.
``` 

- Bandwidth is also the amount of data that can be transmitted in a fixed amount of time. 
- For digital devices, the bandwidth is usually expressed in **bits per second** (bps) or bytes per second
- For analog devices bandwidth is expressed in **cycles per second**, or Hertz (Hz)

digital - bits per second
analog - cycles per second

#### Noise

```
Noise refers to any external and unwanted information that interferes with a transmission signal.
```

 - noise can be created by radio waves, power lines, lightning and bad connections.
 - noise results in data loosen transmission strength and lacks efficiency 

#### Attenuation

```
It refers to loss of energy as signal propagates outwards.
```
- The amount of energy lost depends on frequency
- This can be fixed by amplification of the signal

![](../../../assets/Images%201/Pasted%20image%2020230107132211.png)

#### Distortion
```
Distortion is alteration (distort) of properties of a transferred signal caused by the capacitance and inductance of the communication medium
```

![](../../../assets/Images%201/Pasted%20image%2020230107132306.png)


### Simple topology: point-to-point connection

- Point-to-point topology is the simplest of all the network topologies.
- direct link between the computer
- Faster and more reliable.
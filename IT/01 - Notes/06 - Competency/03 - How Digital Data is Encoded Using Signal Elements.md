# How Digital Data is Encoded Using Signal Elements

1. What is encoding?

```
Encoding is the process of converting a sequence of symbols, characters, alphabets or the data into a specific format for sending the data securely
```

#### Encoding Techniques
- Analog data to Analog signals - Techniques such as Frequency Modulation, Amplitude Modulation and Phase Modulation of analog signals come under this category
- Analog data to Digital signals – Pulse Code Modulation (PCM) does the digitization process also called as digital modulation. 
- Digital data to Digital signals - Non-return to Zero Level (NRZ-L), Nonreturn to Zero Invented (NRZ-I), Manchester Encoding are few techniques.

 2. What is signal modulation?

```
Modulation is the technique used to send the signal to a long distance by attaching it to a higher frequency signal and modifying the basic characteristics such as frequency, amplitude and phase.
```

3. Why do we need modulation?

```
Our message signals are not strong enough to travel a long distance. Once it reaches a certain level it starts to attenuate. To avoid that we take the help of such high frequency signal which is called as a carrier signal to transmit our message signal.
```

- carrier signal - Strong
- message signal - Weak

> Here the basic characteristics of the message signal never changes, Only the **characteristics of the higher frequency signal changes.**


![](../../../assets/Images%201/Pasted%20image%2020230121123333.png)

>- Message signal / Message / Modulating signal - Signal which is about to be modulated.
>- Carrier signal - High frequency signal used to modulate the message signal
>- Modulated signal - Signal that comes after modulating the message signal with the carrier signal.

### Types of Modulation

![](../../../assets/Images%201/Pasted%20image%2020230121124246.png)

#### Analog Modulation

Like mentioned above there are 3 types of analog modulation
1. Amplitude modulation
2. Frequency modulation
3. Phase modulation

##### Amplitude modulation

This is the technique of modulation, where the amplitude of the carrier signal changes.

![](../../../assets/Images%201/Pasted%20image%2020230121124735.png)

> As you can see, the amplitude of the carrier signal is altered according to the amplitude of the message signal

**Advantages**
- Most simple method of modulation

**Disadvantages**
- Preceptable for noise

**Applications**
- AM radio broadcast

##### Frequency modulation

This is the technique of modulation, where the frequency of the carrier signal changes.

![](../../../assets/Images%201/Pasted%20image%2020230121125149.png)

> As you can see, the frequency of the carrier signal is altered according to the frequency of the message signal. All the other basic characteristics stays the same.

**Advantages**
- No noice is added

**Disadvantages**
- Complicated

**Applications**
- FM radio broadcast

##### Phase modulation

This is the technique of modulation, where the phase of the carrier signal changes.

![](../../../assets/Images%201/Pasted%20image%2020230121125428.png)

> As you can see, the phase of the carrier signal is altered according to the amplitude of the message signal

The main difference we see once the message signal is modulated is that the side of the angle of the carrier wave changes according to the message wave. Meaming that the phase only changes when the binary signal value changes from 0 to 1 or 1 to 0

![](../../../assets/Images%201/Pasted%20image%2020230123132135.png)

When the value of the signal wave becomes 0, the wave stops going up and stars going down.

**Advantages**
- Doesn't carry any noise

**Disadvantages**
- Demodulation is bit complicated than AM and FM

**Applications**
- Satellite communication.

#### Digital Modulation

In digital modulation there are 3 types used.
1. Amplitude shift key (ASK)
2. Frequency shift key (FSK)
3. Phase shift key (PSK)

> In this, the carrier signal stays analog but the message signal is digital.

##### Amplitude Shift Key

Here the amplitude of the carrier signal (analog) changes according to the message  signal (digital).

![](../../../assets/Images%201/Pasted%20image%2020230121130810.png)

> In the modulated wave the changes to the amplitude only happens when the digital signal value of the wave is 0, in other worrds below the cetral line of the wave

![](../../../assets/Images%201/Pasted%20image%2020230123133258.png)

![](../../../assets/Images%201/Pasted%20image%2020230123133343.png)

**Applications**
- Used in infrared remote controllers
- Used in fiber optical transmitters and receivers

##### Frequency Shift Key

Here the frequency of the carrier signal (analog) changes according to the message  signal (digital).


![](../../../assets/Images%201/Pasted%20image%2020230121130942.png)

**Application**
- Modems use FSK in telemetry systems

![](../../../assets/Images%201/Pasted%20image%2020230123133413.png)

##### Phase Shift Key

Here the phase of the carrier signal (analog) changes according to the message  signal (digital).


![](/assets/Images%201/Pasted%20image%2020230121131213.png)

Here as well, the change of the side of the wave is depicted by a half wave formation in the modulated wave.

![](/assets/Images%201/Pasted%20image%2020230123132207.png)

![](/assets/Images%201/Pasted%20image%2020230123133657.png|500)
**Applications**
- Used in ADSL broadband modem.
- Used in satellite communication.

**Summary of both these modulation schemes**

| Technique | Advantages                       | Disadvantages                   | Applications            |
| --------- | -------------------------------- | ------------------------------- | ----------------------- |
| AM        | Most simple method of modulation | Preceptable for noice           | In AM radios            |
| FM        | Doesn't carry noice              | Complicated                     | In FM radios            |
| PM        | Doesn't carry noice              | Complicated than both AM and FM | Satellite Communication |

| Technique | Application                                                                           |
| ------ | ------------------------------------------------------------------------------------- |
| ASK    | Used in infrared remote controllers, Used in fiber optical transmitters and receivers |
| FSK    | Used in telemetry system modems                                                       |
| PSK    | Used in ADSL broadband modems , Used in satellite communication                       |

![](/assets/Images/Pasted%20image%2020230901182653.png)

![](https://www.youtube.com/watch?v=qGwUOvErR8Q)
### Converting Digital data to Digital signals

There are 3 encoding methods when converting digital data to digital signals.
1. Non-return to Zero Level (NRZ-L)
2. Non-return to Zero Inverted (NRZ-I)
3. Manchester Encoding

##### Non-return to Zero Level

This - is an encoding scheme in which two different voltages for 0 and 1 bits are used to represent data and remain constant during a bit interval.

![](/assets/Images%201/Pasted%20image%2020230121133305.png)


##### Non-return to Zero Inverted

This method is based to transition of physical level.
- if it's a 1, a physical transition happens
- if it's a 0, nothing happens.

![](/assets/Images%201/Pasted%20image%2020230121133628.png)

##### Manchester Encoding

For this encoding, there are 2 different representation methods for 1 and 0 (according to the IEEE 802.3)
1. 1 is represented by a signal wave going from down to up
1. 0 is represented by a signal wave going from up to down

![](/assets/Images%201/Pasted%20image%2020230121134211.png)

![](/assets/Images%201/Pasted%20image%2020230121134541.png)

There is another way called Thomas method which is the reverse of this
- 1 is represented by going up to down
- 0 is represented by going to down to up
But this is out of the syllabus

### Synchronization

```
Synchronization is used to ensure that the data streams are received and transmitted correctly between two devices
```

Usually, a clock signal is transmitted in sequence with a data stream to maintain proper signal timing.

### Handling Errors

>The purpose of error control is to ensure that the information received by the receiver is exactly the information transmitted by the sender


```
The term error control is defined as the process of identification or correction of error occurred in the transmitted data.
```

##### Parity

The most common method of detecting the errors is the use of parity

> The bit is chosen to be a '0' or a '1', in order to keep the total number of '1' s '1' bits in the character odd or even respectively. To compute the parity bit, the number of bits in the character is added first, using modulo-2 addition, the result may be a '0' or a ‘1’. If the parity is chosen as odd, then the additional bit added must make the result into a '1' if the parity chosen is even, then the additional bit must make the result into a '0'. Following is an example for the parity generation. 
> 
> 
> At the receiving end, after the reception of the character, the parity bit is removed from the received character. The remaining bits are added using the modulo-2 addition and the result is checked with the received parity bit. If these two values differ, then the received character contains an error. Hence, the use of parity bit is to detect single bit errors.


Simply said, if its odd parity,
- the total number of 1's in the data bits (including the parity bit) should be an odd number
- i.e take `100010` as the character bits, here the total number of 1's are 2. Since 2 isn't odd the parity bit is going to be 1, now take `11001` as the character bits. Here the total number of 1's are 3 which is an odd number, therefore the parity bit is going to be 0
if its even parity,
- the total number of 1's in the data bits (including the parity bit) should be an even number.
- i.e take `101100`, here the number of 1's are 3 which is not even, therefore the parity bit going to be 1.
- Now take `10001101`, here the number of 1's are 4 which is even, therefore the parity bit is going to be 0.

 ![](/assets/Images%201/Pasted%20image%2020230121140215.png|800)

![](/assets/Images%201/Pasted%20image%2020230121140906.png)
![](/assets/Images%201/Pasted%20image%2020230121140941.png)


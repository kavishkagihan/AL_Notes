# Explores new trends and future directions in computing

### Intelligent and emotional machines

Examples for human interest about intelligent and emotion machines,
- 80's tele-series "Knight Rider" had machines that exhibit intelligence and emotion
-  Modern fictions such as ”2001: A Space Odyssey” by Sir Arthur C Clarke
### Artificial Intelligence

- What is Artificial intelligence?
```
Artificial Intelligence (AI) is usually defined as the science of making computers do things that require intelligence when done by humans.
```
> Some important AI Techniques are: Neural Network, Genetic Algorithm, and Expert Systems


- What is Machine intelligence?

```
Computer which follows problem solving processes as humans do.
```
> Intelligent systems display machine-level intelligence, reasoning, often learning, and self-adapting

#### Branches of Artificial Intelligence

![](../../../assets/Images/Pasted%20image%2020240420185638.png)

##### Neural Network

```
Neural Network are computational models inspired by an animal’s central nervous systems (in particular, the brain) which is capable of machine learning as well as pattern recognition.
```

- Here the behavior, of different animals are studied and used to help develop AI
- Artificial neural networks are generally presented as systems of interconnected **"neurons"** which can compute values from inputs

**Applications of Neural Network**
- Fingerprint Recognition
- Pattern Identification
- Speech Recognition
- Character Recognition
- Signature Verification Application

> Apart from these, neural networks can **analyze real datasets, and make predictions** based on that. More datasets and experience, it has the better chance of the prediction being correct.

##### Genetic Algorithms

```
Genetic Algorithms (GAs) are adaptive heuristic search algorithm premised on the evolutionary ideas of natural selection and genetic
```

> This follows the principles first laid down by Charles Darwin of **survival of the fittest.**

Hence, this is usually **used to find the best solution out of many**

In GA, combining two good solutions to create better solutions in the next generation.
- Father and mother contribute good features to create better children.
- From multiples ways of getting something done, finding the best way to do it with most efficiency.

![](../../../assets/Images/Pasted%20image%2020240420193048.png)
> The place where the genes are separated from the chromosome is called the crossover point
![](../../../assets/Images/Pasted%20image%2020240514151820.png)
 This process of crossing over is done till a chromosome (child) is made that is the fittest and the strongest according to pre-defined set of rules 

---
##### Example 1

![](../../../assets/Images/Pasted%20image%2020240514153404.png)
> A - A gene
> B - A chromosome (Made of 2 or more genes) 
> C - Population (Mode of set of chromosomes)

> In this example, there are 6 genes per chromosome, which means that this population has `2**6 = 64` number of possible solutions

> Here, the process of choosing the strongest and fittest individuals (chromosomes) which need to be crossovered is called selection 

```
Parents
100111 - P1
111101 - P2

Children after crossing over

100101 - C1
111111 - C2
```

___
##### Example 2


Find the number with the larges square root using 4 out of 32.

Vocabulary - `{0,1}`
Fitness function - `x**2`


```
1. Get random 4 out of 32

32 is 2**5, which means one chromosome should have 5 genes

A - 00000
B - 00001
C - 00010
D - 00100

2. Calculate the fitness value
A - 00000 - 0 -> 0**2 = 0
B - 00001 - 1 -> 1**2 = 1
C - 00010 - 2 -> 2**2 = 4
D - 00100 - 4 -> 4**2 = 16

We need to represent these as a precentage of all the fitnesses of all chromosome
Total fitness = 0 + 1 + 4 + 16 = 21

Percentage fitness
A = (0/21) * 100  = 0% -> f1
B = (1/21) * 100 = 4% -> f2
C = (4/21) * 100 = 19% -> f3
D = (16/21) * 100 = 76% -> f4

3. Selection using roulette wheel method 

We need to mark these perentages in a circle like this
```
![](../../../assets/Images/Pasted%20image%2020240514162223.png)
```
Then we select the parents by putting the parble

PB - 00001
PC - 00010

4. Cross over the parents

C1 - 00010
C2 - 00001

5. Then we calculate the fitness function for these 2 children

C1 - 00010 - 2 -> 2**2 = 4 19% -> fc1
C2 - 00001 - 1 -> 1**2 = 1 4% -> fc2

6. Then we add these children to the roulette wheel and arrange them in the decending order of there fitness


D = (16/21) * 100 = 76% -> f4
C = (4/21) * 100 = 19% -> f3
C1 - 00010 - 2 -> 2**2 = 4 19% -> fc1
B = (1/21) * 100 = 4% -> f2
C2 - 00001 - 1 -> 1**2 = 1 4% -> fc2

7. Then again we do the roulette barble and select 2 to crossover.
This is does untill only the strongest ones are left 
```
---
##### Expert Systems

This is the same system that's in the Systems lesson [Expert Systems](02%20-%20Compares%20and%20contrasts%20different%20types%20of%20man-made%20systems%20in%20terms%20of%20their%20objectives%20and%20functionality#Expert%20Systems)

#### Artificial Intelligence Software vs. Conventional Software

| AI Software                                                                        | Conventional Software                                                                     |
| ---------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- |
| Ability to give the computer only the problem, not the steps necessary to solve it | follow a logical series of steps to reach a conclusion based on pre-provided instructions |

#### Artificial Intelligence (Pros)
- Ability to simulate human behavior and cognitive processes.
- Capture and preserve human expertise (Watch, learn and adapt)
- Fast Response.
- The ability to understand large amounts of data quickly.

#### Artificial Intelligence (Cons)
- No common sense
- Can't easily deal with mixed knowledge
- May have high development costs
- Raise legal and ethical concerns



![](../../../assets/Images/Pasted%20image%2020240420195043.png)

### Man-Machine Coexistence

The word coexistence can be broken into two parts, `co-` and `-exists`.The prefix co- means together, and -exist means to be or to live.

- Man-Machine coexistence
```
Man-Machine coexistence is giving assistance to humans in workplaces without disturbing humans
```
Examples: `Asimo` Robot(Humanoid Robots)

- Machine-Machine coexistence
```
Machine-Machine coexixtence is the ability of machines to work with multiple other machines
```

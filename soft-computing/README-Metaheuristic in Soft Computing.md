## Metaheuristic in Soft Computing: 
### Solving Uncapacitated Single Hub Allocation Problem

Soft computing is the use of approximate calculations to provide imprecise but usable solutions to complex computational problems. The approach enables solutions for problems that may be either unsolvable or just too time-consuming to solve with current hardware (TechTarget, 2018).

Metaheuristic is one example of Soft computing technique, are approximation methods growing widespread for its capability in solving complex optimization problem by using concepts derived from artificial intelligences, natural, and biological phenomenon (Osman & Kelly, 1996).

In this folder, we demonstrate the application of metaheuristic in study case of Hub Location Problem (HLP), one of most popular study case in the field of Operation Research / Management Science (OR/MS). 
HLP strongly associated with Supply Chain Management sector. It addresses scenarios where we have a set of nodes representing specific locations, regions, or cities with demands or flows to be satisfied. We need to determine which node or nodes should serve as hubs for the other nodes in order to minimize the overall network cost.

More precisely, we will delve into **Uncapacitated Single Allocation Hub Location Problem**:

**Single**: Meaning that each of non-hub node could be paired only with one corresponding Hub

**Uncapacitated**: There is no demand/flow capacity for each hub in the allocation process

Picture below present the example of typical **Uncapacitated Single Allocation Hub Location Problem** visual representation. In this example, nodes 4,7, and 10 are the hubs for the other nodes

![HLP](https://github.com/Lazuardis/UniversityOfEdinburgh/assets/110012138/ecdf7c9e-4c8a-492b-b5f0-2cbd67e00e4a)

 <br />

### Datasets

The datasets involve 5 different dataset that comprise of different number of node as well as demand/flow matrix and cost matrix. And for each dataset, we will experiment with different parameter of total number of hub. The summary as follows:


![Datasets](https://github.com/Lazuardis/UniversityOfEdinburgh/assets/110012138/758569d2-2820-4bf5-bf2e-1f781402ab81)



### The application of Metaheuristic

#### 1. Genetic Algorithm

Genetic Algorithm (GA) is inspired by the nature of evolution, process of natural selection based upon the concept of survival of the fittest (Murray-Smith, 2012). It is one popular population-based method that imitates the process of parents reproducing offspring. The algorithm is being performed through step by step genetic operators like chromosome crossover, mutation, selection, fitness evaluation and replacement.

In this study case we are adopting some techniques from Topcuoglu et al. (2003) that involves designated solution representation, initial solution generation, crossover and mutation techniques, and replacement.          

Below present the step by step algorithm of performing Genetic Algortihm

![Genetic Algorithm](https://github.com/Lazuardis/UniversityOfEdinburgh/assets/110012138/55261724-b9ce-4b5f-856c-4c091dc47ed3)


#### 2. Tabu Search

Tabu Search (TS) adopts artificial intelligence feature in a way it builds a memory that prohibits the search process revisiting solutions (Hanafi, 2001). The intuitive behind this is to give allowance for exploring different areas of candidate solutions thus avoiding local optimal rather than being stuck when the all the possible neighbour appear worse. 

TS evaluates all candidate solutions in a neighbourhood. And the way the algorithm explores the neighbourhood depends on the neighbourhood structure. In this study case, we use some of the neighbourhood structures defined by Azizi and Salhi (2021). We also adopt tabu tenure as tuning parameter which value will define for how many iterations a solution is forbidden to visit until it is allowed again (Hemert, 2008). 

Below present the step by step algorithm of performing Tabu Search

![Tabu Search](https://github.com/Lazuardis/UniversityOfEdinburgh/assets/110012138/d65ab95e-0ddf-40bb-8ec4-1203bc7cc8a6)


#### 3. Hybrid Genetic Algorithm and Tabu Search

Hybrid algorithm (HA) combines strength of algorithms and generate more powerful optimization technique. The practice of hybrid of TS and GA implementation has been done in various domain fields with the main concept be incorporating tabu search for each individual solution in a population or generation after crossover/mutation process, exploring the best local neighbour for each of them and select the best one before moving on to replacement phase of genetic algorithm (Mottaki et al., 2022), (Li & Gao, 2016).

In our study case, a distinctive modification of hybrid TS and GA is demonstrated as instead performing local search for each of individual, it is done only for the best individual with best fitness value here. The reason being is to avoid lengthy computational time per iteration.

Below present the step by step algorithm of performing Hybrid TS-GA

![Hybrid GA - TS](https://github.com/Lazuardis/UniversityOfEdinburgh/assets/110012138/d9c28244-cace-4494-9113-530cd5fd4f0a)


### Solution Representation

Solution array will be used to represent solution of network setting that generates network cost, with numerical values indicating which nodes serve as hubs and which are allocated to each hub. For example, in figure 1, the first number represents node 0, which acts as a hub with a value of 0. The second node, node 1, is allocated to hub 4 with a value of 4. The three unique integer values of 0, 2, and 4 indicate the three hubs for the remaining nodes. The use of Python programming language is the reason for node 0 being denoted as the first index.

<img width="162" alt="solution array" src="https://github.com/Lazuardis/UniversityOfEdinburgh/assets/110012138/8ad14e5a-7fd5-4a29-9067-8aa2548ac27e">


### Input Parameter: Termination Time

This study has its intention to compare all three algorithm mentioned above. In order to make the comparison somehow equal, fair, apple to apple by each other,  the termination criterion during program execution is based on time constraints. This approach allows us to determine which algorithm yields the best solution within a predefined runtime. This is better compared to use number of iteration as the terminating condition, as various algorithm might have different time lapse, which could be far significantly different between each other due to algorithm structure complexity.


### Findings and Conclusion 

The local search capability of the Tabu Search algorithm demonstrates superior performance for smaller datasets, such as CAB25 and TR55, but is faced with significant computational responsibility when applied to larger datasets. On the other hand, the Genetic Algorithm has shown to perform better in handling larger datasets such as TR81 and RGP100, due to its ability to incorporate a population-based exploration of better solutions, which is effective and does not necessarily require the same level of time as a local search approach.

The developed Hybrid Algorithm (HA) demonstrates promising results in handling both small and large datasets. However, the algorithm's potential is hindered by its current configuration, which only examines local search on the best individual based on fitness value, therefore, limiting its capacity to reach optimal performance.


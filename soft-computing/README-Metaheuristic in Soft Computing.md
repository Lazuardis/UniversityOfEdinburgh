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


![Genetic Algorithm](https://github.com/Lazuardis/UniversityOfEdinburgh/assets/110012138/55261724-b9ce-4b5f-856c-4c091dc47ed3)


#### 2. Tabu Search

![Tabu Search](https://github.com/Lazuardis/UniversityOfEdinburgh/assets/110012138/d65ab95e-0ddf-40bb-8ec4-1203bc7cc8a6)


#### 3. Hybrid Genetic Algorithm and Tabu Search

![Hybrid GA - TS](https://github.com/Lazuardis/UniversityOfEdinburgh/assets/110012138/d9c28244-cace-4494-9113-530cd5fd4f0a)


### Solution Representation

### Findings and Conclusion 

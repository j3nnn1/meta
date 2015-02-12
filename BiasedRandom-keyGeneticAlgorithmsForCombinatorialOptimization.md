
rkga => randon key genetic algorithms
=====================================

JOSÉ FERNANDO GONÇALVES AND MAURICIO G. C. RESENDE
--------------------------------------------------


* had a great intro intro:
    E = {1..n} 
    F subconjunto de 2 exp E
    S* solucion optima del conjunto F

* Combinatorial Optimization, apply to Routing, scheduling, inventory control, production planning, location problems.
* GRASP, simulated anneling, tabu search, variable neighborhood search, scatter search, path-relinking, iterated local search, ant colony optimization, genetic algorithms
* explain elements that shape to Metaheuristic
    1 - ground set
    2 - solution set
    3 - optimal solution
* A example traveller salesman Problem, 

* A framework for build heuristic, that include components:
    * the problem-independent component
    * the architecture
    * the problem specif-part
* Defined that the sofware can be sequential or parallel
* Defined  a new term : "Algorithm Designer"

BRKAG
=====
* AG, survival of the fittest, supervivencia del mas apto.
* solution = individue 
* each individue has a chromosome that represent a solution
* a chromosome is a string of genes.
* each gen take a values called allele
* each chromosome had a fitness level (nivel de adaptacion) wich is correlated with the objetive function.
* an population, with N generations
* mutation, crossover, produce offspring(descendientes)
* Individuals are selected at random but those with betterness are preferred over those that are less fit
* first introduced in 1994
 In BRKAG,  chromosomes are represented as a string or vector, de random real numbers between [0,1]
- the decoder, takes as input any chromosome and asociate with it a solution.
- in 1994 the decoder ordena el vector de "random keys", y usa el indice estos elementos ordenados para representar una secuencia. 
- the decoder is a main component for BRKAG
- Decoder computed the fitness of each individual 
- p vectors of random keys, => initial population
- later this population is split into 
    - pe (p elite)
    - p - pe (no elite) where pe < p - pe
- An RKGA uses an elitist strategy, after the fitness is computed the population is split.
    - the elite population is copied to the next generation
- At each generation a small number of p m mutants are introduced into the population
- how represent a random key vector.???
- process of mating => like crossover



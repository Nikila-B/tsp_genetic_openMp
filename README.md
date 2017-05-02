# tsp_genetic_openMp
I have implemented TSP using Genetic algorithm, and used OpenMp for parallelising the code.

INTRODUCTION
THE serialtsp.CPP FILE HAS THE SERIAL CODE IMPLEAMENTATION AND THE paralleltsp.CPP HAS THE PARALLEL CODE USING OPENMP. THE METHODOLOGIES USED FOR CROSSOVER AND CALCULATING FITNESS FUNCTION ARE MENTIONED BELOW. THE MAJOR ISSUE WITH THE CODE ID THAT THE SERIAL CODE PERFORMS BETTER THAN THE PARALLEL CODE. ALSO THERE IS A RESTRICTION OF NUMBER OF INDIVIDUALS IN A POPULATION, WHICH CAN BE CHANGED BY CHANGING THE SIZE OF THE 2D ARRAYS.

ABOUT TSP
The Travelling Salesman Problem (often called TSP) is a classic algorithmic problem in the field of computer science. It is focused on optimization. In this context, better solution often means a solution that is cheaper. TSP is a mathematical problem. It is most easily expressed as a graph  describing the locations of a set of nodes. The Travelling Salesman Problem describes a salesman who must travel between N cities.   The order in which he does so is something he does not care about, as   long as he visits each one during his trip, and finishes where he was at  first. The travelling salesman problem is regarded as difficult to solve. If there is a way to break this problem into smaller component problems, the components will be at least as complex as the original one. This is what computer scientists call NP-hard problems.


ABOUT GENETIC ALGORITHMS
A genetic algorithm (GA) is a method for solving both constrained and unconstrained optimization problems based on a natural selection process that mimics biological evolution. The algorithm repeatedly modifies a population of individual solutions. In a genetic algorithm, a population of candidate solutions (called individuals, creatures, or phenotypes) to an optimization problem is evolved toward better solutions. Each candidate solution has a set of properties (its chromosomes or genotype) which can be mutated and altered; traditionally, solutions are  represented in binary as strings of 0s and 1s, but other encodings are   also possible. 
A typical genetic algorithm requires:

•	a genetic representation of the solution domain,
•	a fitness function to evaluate the solution domain.


OVERVIEW OF THE CODE
• We have taken a training set and calculated the fitness of the population.
• The fit population is taken forward and crossover is performed.
• After performing crossover, the new population is added to the old population.
• At the end, mutation is applied to remove duplicate entries in one individual.

CROSSOVER METHOD USED
I HAVE USED ONE POINT CROSSOVER. THE FIRST TWO ATTRIBUTES OF THE CHILD ARE FROM FIRST PARENT AND OTHER ATTRIBUTES FROM SECOND PARENT. I HAVE TAKEN THE FIRST TEN AND THE LAST TEN INDIVIDUALS FROM THE CURRENT POPULAATION, FOR PERFORMING CROSSOVER.

FITENESS THRESHOLD
THE VALUE OF FITNESS THRSHOLD IS CALCULATED BASED ON THE MAXIMUN OCCURINNG COST OF TRAVEL. IF TWO COSTS OCCUR SAME TIME ANYONE OF THEM IS CHOOSEN.

LIMITATIONS/ISSUES PROBLEM
THE SERIAL CODE TAKES LESS TIME AS COMPARED TO THE PARALLEL CODE.



# simulated_annealing_tsp
Simulated Annealing is an optimization algorithm that iteratively compares a new solution to a current solution. If the new one is better, it replaces the current. If the new one is worse, it may still be accepted based on a probability that is determined by a temperature value that "cools" or decreases with each iteration. 

Simulated Annealing has been successfully applied for many real world problems, but it can be difficult to implement because its performance is very sensitive to the parameters set by the user. The two main parameters are the initial temperature and the cooling schedule. This notebook explores tuning both of those parameters and compares the results of my algorithm to stochastic hill-climber and simple random search algorithms for 5 Traveling Salesman Problems (TSP) problems.

Finding the initial temperature parameter can be particularly challenging. To do this, I implemented an [algorithm proposed by Walid Ben-Ameur](https://www.mendeley.com/catalogue/8a3521ca-3e4d-362e-86d6-0d2aad69f398/) (see steps on page 374) in Python. Some experimentation might be needed to find the parameter S that is used in that algorithm. I provided a couple functions that may make finding S a little easier.

In the Traveling Salesman Problem, the salesman must visit all cities within the itinerary once and return to the original city where the journey began. It should be easy to find the shortest route for this right? This problem is in fact very difficult to solve as your number of cities grows, which is why local search heuristics are often needed to approximate an optimal answer. Each of my TSP problems are from the [TSPLIB website](http://comopt.ifi.uni-heidelberg.de/software/TSPLIB95/) hosted by Heidelberg University.

Useful links for understanding these topics:

More on the TSP: https://en.wikipedia.org/wiki/Travelling_salesman_problem

Simulated Annealing: https://machinelearningmastery.com/simulated-annealing-from-scratch-in-python/

Simulated Annealing & TSP: https://towardsdatascience.com/how-to-solve-travelling-salesman-problem-with-simulated-annealing-c248447a8bcd 

# Course-Scheduling-and-Resource-Optimization-System
The system aims to allocate rooms, professors, and time slots while considering constraints like room availability, professor schedules, and student preferences. The goal is a conflict-free schedule maximizing resource utilization.  The chosen approach is the A* Search Algorithm, adapted for scheduling. 

# A* search algorithm

* A* searches possible schedules, evaluating each based on constraint violations. The cost function f(n) = g(n) + h(n) is used, where g(n) represents satisfied constraints and h(n) estimates remaining unsatisfied constraints.

* Purpose: A* is used for pathfinding and graph traversal to find the shortest path from a start node to a goal node.

* Combines Algorithms: It merges the principles of Dijkstra's algorithm and Greedy Best-First Search.

* Cost Functions:

g(n): Represents the cost from the start node to the current node nnn.

h(n): Heuristic function that estimates the cost from the current node nnn to the goal node.

Total Cost: The total estimated cost f(n)=g(n)+h(n)f(n) = g(n) + h(n)f(n)=g(n)+h(n) guides the search process.

* Node Exploration: A* prioritizes nodes based on the lowest f(n)f(n)f(n), balancing the actual cost to reach the node and the estimated cost to reach the goal.

* Optimality: A* guarantees an optimal solution if the heuristic h(n)h(n)h(n) is admissible (never overestimates the true cost).

* Applications: Widely used in AI, robotics, and game development for efficient navigation and resource management.

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

## In this application, A* Search Algorithm Components are:
1. g(self): Returns the number of satisfied constraints by counting courses with assigned rooms and time slots.
2. h(self): Returns the number of unsatisfied constraints by counting courses without a room or time slot.
3. f(self): Combines g(self) and h(self) to rank schedules. A* prioritizes schedules with the lowest f value.
4. lt(self, other): Compares two Schedule objects based on their f() values for priority queue ordering.

The a_star_search function uses a priority queue (open list) and a closed list to explore schedules efficiently. The time complexity depends on the number of courses (C), rooms (R), and time slots (T).
![](https://github.com/user-attachments/assets/96048c87-90bc-4205-8dfe-f1011f5ba957)

## Novelty 

A Search Algorithm for Scheduling: Innovative use of A* search to optimize course schedules by evaluating the cost of constraint violations (room, professor availability, and time slot conflicts). 

Custom Heuristic (f = g + h): Unique heuristic design to prioritize schedules with fewer unsatisfied constraints, ensuring efficient and conflict-free resource allocation. 

Dynamic Neighbor Generation: Flexibly generates neighboring schedules by dynamically assigning available rooms and time slots, ensuring more efficient exploration of solutions.

Constraint Satisfaction as a Core Metric: The system directly measures how well constraints are satisfied (room availability, professor assignment, time slots) and continuously improves the solution through the A* algorithm.

Conflict Detection and Resolution: By using a validity check that detects conflicts (e.g., multiple courses in the same room at the same time), the system ensures a conflict-free schedule in a dynamic and automated manner.

Scalability for Complex Constraints: The approach can easily scale to handle more complex constraints, such as student preferences or course prerequisites, by modifying the heuristic function to accommodate additional rules.

Real-time Adaptation: The system's ability to generate new neighbor states and explore different configurations makes it adaptable to last-minute changes in room availability or professor schedules without restarting the process.

### Usage

```bash
python3 code.py
```

### Dependencies
* Python 3.x
* Standard libraries

### Future Enhancements
* Add GUI using Tkinter or Flask
* Add hard/soft constraint differentiation

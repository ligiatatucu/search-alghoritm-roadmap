# Search Algorithm Roadmap

This project demonstrates how to calculate the distance between Porto Unico and Curitiba using a heuristic-based approach—specifically, the Greedy Algorithm. Heuristics are practical strategies for solving problems that may not guarantee a perfect solution but provide sufficiently good results within time or resource constraints.

In this case, the Greedy Algorithm is used to make locally optimal choices at each step with the hope of finding the global optimum path.

🧠 Heuristic Strategy Overview
The algorithm is implemented in two main parts:

Graph Construction – Defining Vertex, Adjacent, and Graph classes to model the map.

Greedy Pathfinding – Creating and using an OrderedArray to determine the next best path based on heuristic distance.

📦 Code Structure and Explanation
🔹 Class: Vertex
Represents a node in the graph.

Constructor Parameters:

label: A unique identifier for the vertex (e.g., city name).

visited: A boolean flag (default False) to mark whether the node has been visited.

distance_objective: A heuristic estimate (e.g., straight-line distance) to the target vertex.

adjacent: A list holding adjacent nodes connected to this vertex.

Methods:

add_adjacent(self, adjacent): Adds an adjacent vertex (an Adjacent instance) to the adjacency list.

print_method(self): Prints the label and cost of each adjacent vertex, helpful for debugging or visualizing the graph.

🔹 Class: Adjacent
Represents an edge or connection from one vertex to another.

Purpose:

Encapsulates both the target vertex and the cost to reach it.

Provides a clean and structured way to manage relationships between nodes, including weights (distances).

Attributes:

vertex: A reference to the target Vertex object.

cost: The cost or distance of the connection from the current vertex to the adjacent one.

This separation of Vertex and Adjacent classes allows for a modular and extendable graph structure, which is ideal when implementing pathfinding algorithms.

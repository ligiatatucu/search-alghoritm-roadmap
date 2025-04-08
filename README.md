# 🔍 search-alghoritm-roadmap

This project demonstrates a **Greedy Algorithm** approach to calculating the distance between *Porto Unico* and *Curitiba* using a **heuristic search strategy**. 

Heuristic algorithms are problem-solving techniques that use practical methods to produce solutions that are not guaranteed to be perfect but are often good enough within time or resource constraints.

---

## 🧠 What’s Implemented?

This example uses the **Greedy Best-First Search** technique, which always selects the next node based on the lowest estimated cost to the goal (heuristic). The problem is broken down into two main parts:

1. **Graph Construction** – Creating `Vertex`, `Adjacent`, and `Graph` classes.
2. **Greedy Search Logic** – Using an `OrderedArray` to keep track of the most promising path.

---

## 📦 Project Structure

### 🔹 Class: `Vertex`

Represents a node in the graph.

**Attributes:**
- `label`: A unique identifier for the vertex (e.g., city name).
- `visited`: Boolean flag indicating if the node was visited.
- `distance_objective`: Heuristic distance to the goal (e.g., straight-line distance).
- `adjacent`: A list of connections to other vertices.

**Methods:**
- `add_adjacent(self, adjacent)`: Adds a connection to another node.
- `print_method(self)`: Prints adjacent nodes and their respective costs.

---

### 🔹 Class: `Adjacent`

Represents a directional connection between two vertices.

**Attributes:**
- `vertex`: The destination vertex.
- `cost`: Cost or distance to the destination.

---

### 🔹 Class: `Graph`

Manages the entire network and pathfinding process.

**Attributes:**
- `current_vertex`: The current vertex being explored.
- `end_vertex`: The goal vertex.
- `ordered_array`: Stores vertices to be visited in order of priority.

**Methods:**
- `add_vertex(self, vertex)`: Adds a vertex to the graph.
- `set_start(self, label)`: Sets the starting point.
- `set_end(self, label)`: Sets the destination point.
- `search(self)`: Core logic of the greedy algorithm, tracing a path toward the goal.

---

### 🔹 Class: `OrderedArray`

Custom priority queue to store vertices by their heuristic values.

**Attributes:**
- `array`: List of vertices in sorted order.
- `limit`: Max number of vertices the array can hold.

**Methods:**
- `insert(self, vertex)`: Inserts a vertex in sorted order (lowest heuristic first).
- `get_first(self)`: Removes and returns the vertex with the lowest heuristic value.
- `print_method(self)`: Prints the content of the array for debug purposes.

---

## 🚀 How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/ligiatatucu/search-alghoritm-roadmap.git

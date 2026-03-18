# Shortest Path — Dijkstra's Algorithm (C++)

A C++ program that builds a weighted social network graph from a CSV file and uses **Dijkstra's algorithm** to find the shortest path between any two people, outputting the full path and total cost.

---

## Features

- Loads a weighted social network from a CSV adjacency matrix at runtime
- Builds a weighted graph using adjacency lists via `std::map`
- Dijkstra's algorithm implemented with a priority queue for efficiency
- Outputs the full shortest path between two nodes and the total path cost
- Handles cases where no path exists between two people
- Input loop allowing repeated searches until the user quits

---

## Concepts Demonstrated

- Dijkstra's shortest path algorithm
- Weighted graph representation using adjacency lists
- Priority queue for selecting the lowest-cost candidate node
- Path reconstruction using parent tracking
- STL `map`, `priority_queue`, `stack`, and `vector`

---

## How to Run

### Online (easiest)
Paste `Lab_12.cpp` into [onlinegdb.com](https://onlinegdb.com), set language to C++, and upload `fb_weighted.csv` as the input file.

### Local (requires g++)
```bash
g++ -o dijkstra Lab_12.cpp
./dijkstra
```

Place `fb_weighted.csv` in the same directory before running.

---

## Usage

```
Enter the starting name (X to quit): Alice
Enter the ending name (X to quit): Charlie

The best path between these two people is:
 Alice
 Bob
 Charlie
The cost of this path is: 7
```

Enter `X` at any prompt to quit.

---

## Notes

- Edge weights are read directly from the CSV — a value of 0 means no connection
- Best path and best parent are tracked per node to allow full path reconstruction
- The priority queue processes lowest-cost candidates first (min-heap behavior)
- Requires `fb_weighted.csv` in the same directory to run

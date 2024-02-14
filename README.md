# Graphs C++

A small collection of graph algorithms implemented in C++. Currently available:

- [Depth-first search](./src/dfs.cpp)
- [Breadth-first search](./src/bfs.cpp)
- [Dijkstra](./src/dijkstra.cpp)
- [Bellman-Ford](./src/bellman_ford.cpp)
- [Ford-Fulkerson](./src/ford_fulkerson.cpp)

## How to run

Clone the repo and compile sources:

```
git clone https://github.com/e-polevikov/graphs-cpp
cd graphs-cpp
make
```

Then run a binary as shown below.

```
cat resources/weighted_graph.txt | ./bin/main.out
```

Dijkstra is the default algorithm to run. It find all shortest paths in the specified graphs and prints them to stdout.

```
Graph:
0: (1, 10) (3, 2) (4, 3) 
1: (0, 10) (2, 5) 
2: (1, 5) (3, 1) (7, 3) 
3: (2, 1) (0, 2) (5, 18) 
4: (0, 3) 
5: (6, 6) (3, 18) 
6: (5, 6) (7, 7) 
7: (6, 7) (2, 3) 
Shortest paths: 
4 -> 0 (3)
4 -> 0 -> 3 -> 2 -> 1 (11)
4 -> 0 -> 3 -> 2 (6)
4 -> 0 -> 3 (5)
4 -> 0 -> 3 -> 2 -> 7 -> 6 -> 5 (22)
4 -> 0 -> 3 -> 2 -> 7 -> 6 (16)
4 -> 0 -> 3 -> 2 -> 7 (9)
```
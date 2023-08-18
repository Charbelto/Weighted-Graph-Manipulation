# Overview
This code implements a graph data structure and algorithms operating on the graph. It allows the user to build a directed or undirected graph, add/remove nodes and edges, adjust edge weights, and run algorithms like depth-first search, cycle detection, topological sorting, and shortest path.

# Classes
## Graph: 
Represents a graph with nodes and edges. Stores the graph as an adjacency list (unordered_map). Key methods:

- addNode, removeNode: Add/remove nodes
- addEdge, removeEdge, adjustEdgeWeight: Add/remove/adjust edges
- DFS: Depth-first search
- hasCycle: Detect cycles
- topologicalSort: Topological ordering
- shortestPath: Shortest path between two nodes

# Algorithms
- DFS: Recursively explores nodes depth-first using a stack to track order. Uses a visited map to avoid re-exploring nodes.

- Cycle Detection: Uses a recursion stack in addition to visited map. If an edge points to a node already in the recursion stack, there is a cycle.

- Topological Sort: Repeatedly finds nodes with no remaining unvisited edges and pushes them to stack. Prints stack at end.

- Shortest Path: Implements BFS from start node, tracking distance in a map. Stops when reach end node.

# Usage
The main function allows the user to build a graph interactively, choosing whether it is directed and calling the key Graph methods. Users can add nodes/edges, run algorithms, etc. Exits when user enters 0.

# Key Data Structures
- unordered_map<string, vector<pair<string, int>>>: Adjacency list
- stack<string>: Tracks DFS order
- unordered_map<string, bool>: Visited and recursion stack maps
- queue<string>: BFS queue
- unordered_map<string, int>: Distance map in shortest path

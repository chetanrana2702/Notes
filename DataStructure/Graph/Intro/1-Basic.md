## Basics About Graph

#### 1. **Introduction to Graphs**

A **graph** is a collection of **vertices** (also called nodes) and **edges** (also called arcs) that connect pairs of vertices. Graphs are used to model relationships and connections in a variety of real-world problems. For example, in a social network, the vertices represent people, and the edges represent friendships or follow relationships.

A graph can be visualized as a set of dots (vertices) connected by lines (edges).

#### 2. **Components of a Graph**

*   **Vertex (Node)**: A fundamental unit in a graph. It can represent anything, such as a city, person, or computer.
    
*   **Edge (Arc)**: An edge connects two vertices. It represents the relationship between them. The edge can be **directed** (arrows indicate direction) or **undirected** (no arrows, just a simple connection).
    
    *   **Directed Edge**: An edge that has a direction. It indicates a one-way relationship.
        
    *   **Undirected Edge**: An edge that does not have a direction, indicating a bidirectional relationship.
        
*   **Degree of a Vertex**: The degree of a vertex is the number of edges incident to it. In a directed graph, we have:
    
    *   **In-degree**: The number of edges directed into a vertex.
        
    *   **Out-degree**: The number of edges directed out of a vertex.
        

#### 3. **Types of Graphs**

*   **Undirected Graph**: A graph in which edges have no direction. The relationship between two vertices is bidirectional.
    
*   **Directed Graph (Digraph)**: A graph in which edges have directions. Each edge has a source vertex and a target vertex.
    
*   **Weighted Graph**: A graph in which each edge has a weight or cost associated with it. This is useful for representing problems like shortest paths or network traffic.
    
*   **Unweighted Graph**: A graph where all edges are considered to have equal weight or cost.
    
*   **Cyclic Graph**: A graph that contains at least one cycle (a path that starts and ends at the same vertex).
    
*   **Acyclic Graph**: A graph that does not contain any cycles.
    
    *   **Directed Acyclic Graph (DAG)**: A directed graph that has no cycles. DAGs are commonly used in scheduling problems and dependency graphs.
        
*   **Complete Graph**: A graph in which every pair of vertices is connected by an edge.
    
*   **Subgraph**: A graph formed by a subset of the vertices and edges of the original graph.
    

#### 4. **Graph Representation**

There are multiple ways to represent a graph in computer memory:

*   **Adjacency Matrix:** A 2D matrix where each element indicates whether pairs of vertices are adjacent (connected by an edge). If there is an edge between vertex i and vertex j, the matrix element at row i and column j is marked (often with 1 for undirected or a specific weight for weighted graphs).

    Example of an adjacency matrix for an undirected graph:

    ```
    Graph G:
        A -- B
        |    |
        C -- D

    Adjacency Matrix:
          A  B  C  D
        A 0  1  1  0
        B 1  0  0  1
        C 1  0  0  1
        D 0  1  1  0
    ```
*  **Adjacency List**: A more space-efficient representation where each vertex stores a list of its adjacent vertices. This is better for sparse graphs.

    Example of an adjacency list for the same graph:
    ```
    Graph G:
        A -> [B, C]
        B -> [A, D]
        C -> [A, D]
        D -> [B, C]
    ```

*  **Edge List:** A list of all edges in the graph. Each edge is represented as a pair of vertices (for undirected graphs) or a triplet (for directed graphs with weights).

    Example of an edge list for the same graph:
    ```
    [(A, B), (A, C), (B, D), (C, D)]
    ```

#### 5. **Traversal of Graphs**

Graph traversal refers to visiting all the vertices in a graph. There are two primary methods of traversal:

*   **Depth-First Search (DFS)**: A traversal method that explores as far down a branch of the graph as possible before backtracking. DFS uses a stack (either explicitly or via recursion) to keep track of the vertices.
    
*   **Breadth-First Search (BFS)**: A traversal method that explores all the vertices at the current level before moving on to the next level. BFS uses a queue to manage the vertices.
    

Both DFS and BFS are useful in solving problems like pathfinding, finding connected components, and more.

#### 6. **Applications of Graphs**

Graphs have numerous applications in various fields:

*   **Social Networks**: Graphs are used to represent users and their relationships (friendships, followers).
    
*   **Computer Networks**: Graphs represent routers and connections between them.
    
*   **Web Page Link Analysis**: Pages are vertices, and hyperlinks between them are edges. Search engines use graphs to rank pages.
    
*   **Recommendation Systems**: Graphs help model user preferences and item relationships in systems like Netflix or Amazon.
    
*   **Shortest Path Algorithms**: Algorithms like **Dijkstra's** and **Bellman-Ford** are used to find the shortest path in weighted graphs.


### Example Graph with Diagram

Here's a simple undirected graph example:
```
  A -- B
  |    |
  C -- D
```

This graph has 4 vertices: A, B, C, D, and 4 edges: (A, B), (A, C), (B, D), (C, D).

**Adjacency Matrix:**
```
    A  B  C  D
A [ 0  1  1  0 ]
B [ 1  0  0  1 ]
C [ 1  0  0  1 ]
D [ 0  1  1  0 ]

```

**Adjacency List:**
```
A -> [B, C]
B -> [A, D]
C -> [A, D]
D -> [B, C]

```

### 5. **Graph Algorithms**

Graphs provide a rich set of algorithms for solving problems. Some of the most widely used graph algorithms are:

#### 5.1 **Breadth-First Search (BFS)**

Breadth-First Search is an algorithm for traversing or searching a graph. It starts at a root vertex and explores all of its neighbors before moving on to their neighbors, and so on. BFS is particularly useful for finding the shortest path in an unweighted graph.

#### 5.2 **Depth-First Search (DFS)**

Depth-First Search explores as far as possible along a branch before backtracking. It is useful for tasks like finding connected components or performing topological sorting in directed acyclic graphs (DAGs).

#### 5.3 **Dijkstra’s Algorithm**

Dijkstra’s Algorithm is used to find the shortest path between two vertices in a weighted graph. It works by progressively visiting the vertex with the smallest tentative distance and updating the distances to its neighbors.

#### 5.4 **Prim’s and Kruskal’s Algorithms**

Prim’s and Kruskal’s algorithms are used to find the **minimum spanning tree** (MST) of a weighted graph. An MST is a subgraph that connects all vertices with the minimum possible sum of edge weights.

#### 5.5 **Floyd-Warshall Algorithm**

The Floyd-Warshall algorithm is an all-pairs shortest path algorithm that finds the shortest paths between all pairs of vertices in a weighted graph.
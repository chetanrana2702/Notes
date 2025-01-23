## Unweighted Graph

- An unweighted graph is a type of graph in which the edges do not have any associated weights or values. 
- In an unweighted graph, the edges simply represent connections between vertices, and all edges are considered equal in terms of their significance. 
- This means that the graph does not take into account any cost, distance, or other metrics associated with traversing the edges.

### Example of an Unweighted Graph

Consider a simple unweighted graph with the following vertices and edges:

*   **Vertices (Nodes)**: A, B, C, D
    
*   **Edges**:
    
    *   (A, B)
        
    *   (A, C)
        
    *   (B, C)
        
    *   (C, D)
        

This can be visually represented as:
```shell
    A
   / \
  B---C
   \
    D
```

### Explanation

1.  **Vertices**: The graph has four vertices: A, B, C, and D. Each vertex can represent an entity, such as a person, a city, or any other object.
    
2.  **Edges**: The edges represent connections between the vertices:
    
    *   The edge (A, B) indicates that there is a connection between vertex A and vertex B.
        
    *   The edge (A, C) indicates a connection between vertex A and vertex C.
        
    *   The edge (B, C) indicates a connection between vertex B and vertex C.
        
    *   The edge (C, D) indicates a connection between vertex C and vertex D.
        
3.  **No Weights**: 
    -   Since this is an unweighted graph, there are no weights associated with the edges. 
    -   This means that all edges are treated equally, and the graph does not account for any cost or distance when traversing from one vertex to another.
    
4.  **Applications**: Unweighted graphs are commonly used in scenarios where the relationships between entities are binary (i.e., either there is a connection or there isn't) and do not require additional metrics. Examples include:
    
    *   Social networks (where friendships are either present or absent).
        
    *   Connectivity in computer networks (where devices are either connected or not).
        
    *   Simple pathfinding problems (where the goal is to find any path rather than the shortest path).
        

### Properties of Unweighted Graphs

*   **Pathfinding**: 
    - In unweighted graphs, algorithms like Breadth-First Search (BFS) can be used to find the shortest path in terms of the number of edges traversed. 
    - Since all edges are equal, the shortest path is simply the path with the fewest edges.
    
*   **Connectedness**: 
    - An unweighted graph can be connected or disconnected. 
    - A connected unweighted graph has a path between every pair of vertices, while a disconnected graph has at least one pair of vertices without a path connecting them.
    
*   **Degree of a Vertex**: The degree of a vertex in an unweighted graph is the number of edges connected to it. For example, in the graph above:
    
    *   Degree of A = 2 (connected to B and C)
        
    *   Degree of B = 2 (connected to A and C)
        
    *   Degree of C = 3 (connected to A, B, and D)
        
    *   Degree of D = 1 (connected to C)
        

This example illustrates the basic structure and properties of an unweighted graph, highlighting the simplicity of relationships represented without the complexity of weights.

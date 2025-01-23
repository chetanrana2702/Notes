## Connected Graphs

- A connected graph is a type of graph in which there is a path between every pair of vertices. 
- In other words, you can reach any vertex from any other vertex by traversing the edges of the graph. 
- Connected graphs can be either directed or undirected, but the concept of connectivity is often discussed in the context of undirected graphs.

### Example of a Connected Graph

Consider a simple undirected connected graph with the following vertices and edges:

*   **Vertices (Nodes)**: A, B, C, D, E
    
*   **Edges**:
    
    *   (A, B)
        
    *   (A, C)
        
    *   (B, C)
        
    *   (B, D)
        
    *   (C, E)
        

This can be visually represented as:
```
    A
   / \
  B---C
   \
    D
    |
    E
```
### Explanation

1.  **Vertices**: The graph has five vertices: A, B, C, D, and E. Each vertex can represent an entity, such as a city, a person, or any other object.
    
2.  **Edges**: The edges represent connections between the vertices:
    
    *   The edge (A, B) indicates a connection between vertex A and vertex B.
        
    *   The edge (A, C) indicates a connection between vertex A and vertex C.
        
    *   The edge (B, C) indicates a connection between vertex B and vertex C.
        
    *   The edge (B, D) indicates a connection between vertex B and vertex D.
        
    *   The edge (C, E) indicates a connection between vertex C and vertex E.
        
3.  **Connectivity**: The graph is connected because there is a path between every pair of vertices:
    
    *   From A to B: Directly connected by edge (A, B).
        
    *   From A to C: Directly connected by edge (A, C).
        
    *   From A to D: A → B → D (via edges (A, B) and (B, D)).
        
    *   From A to E: A → C → E (via edges (A, C) and (C, E)).
        
    *   From B to C: Directly connected by edge (B, C).
        
    *   From B to D: Directly connected by edge (B, D).
        
    *   From B to E: B → C → E (via edges (B, C) and (C, E)).
        
    *   From C to D: C → B → D (via edges (C, B) and (B, D)).
        
    *   From C to E: Directly connected by edge (C, E).
        
    *   From D to E: D → B → C → E (via edges (D, B), (B, C), and (C, E)).
        
4.  **Applications**: Connected graphs are important in various applications, including:
    
    *   **Network Design**: Ensuring that all nodes in a network can communicate with each other.
        
    *   **Social Networks**: Analyzing the connectivity between users or groups.
        
    *   **Transportation Networks**: Ensuring that all locations are reachable from one another.
        

### Properties of Connected Graphs

*   **Path Existence**: In a connected graph, there exists at least one path between every pair of vertices. This is the defining characteristic of connectivity.
    
*   **Subgraphs**: A connected graph can contain connected subgraphs. If you remove some edges or vertices, the remaining graph may still be connected or may become disconnected.
    
*   **Minimum Spanning Tree**: A connected graph can have a minimum spanning tree (MST), which is a subgraph that connects all vertices with the minimum total edge weight (if weights are present).
    
*   **Disconnected Graph**: If a graph is not connected, it is called a disconnected graph. In a disconnected graph, there are at least two vertices that do not have a path connecting them.
    

This example illustrates the basic structure and properties of a connected graph, emphasizing the importance of connectivity in various applications and scenarios.
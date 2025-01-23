## Directed Graph

- A directed graph (or digraph) is a type of graph in which the edges have a direction. 
- This means that each edge connects two vertices and has a specific starting point (tail) and an ending point (head). 
- In a directed graph, if there is an edge from vertex A to vertex B, you can traverse from A to B, but not necessarily from B to A unless there is a separate edge going in that direction.

### Example of a Directed Graph

Consider a simple directed graph with the following vertices and edges:

*   **Vertices (Nodes)**: A, B, C, D
    
*   **Edges**:
    
    *   (A → B)
        
    *   (A → C)
        
    *   (B → C)
        
    *   (C → D)
        

This can be visually represented as:
```shell
    A
   / \
  v   v
  B-->C
       |
       v
       D
```

### Explanation

1.  **Vertices**: The graph has four vertices: A, B, C, and D. Each vertex can represent an entity, such as a webpage, a task, or any other object.
    
2.  **Edges**: The edges represent directed connections between the vertices:
    
    *   The edge (A → B) indicates that there is a directed connection from vertex A to vertex B.
        
    *   The edge (A → C) indicates a directed connection from vertex A to vertex C.
        
    *   The edge (B → C) indicates a directed connection from vertex B to vertex C.
        
    *   The edge (C → D) indicates a directed connection from vertex C to vertex D.
        
3.  **Directionality**: Since this is a directed graph, the edges have a specific direction. For example, you can go from A to B, but you cannot go from B to A unless there is a separate edge (which there isn't in this case). This is a key difference from undirected graphs.
    
4.  **Applications**: Directed graphs are commonly used to model relationships where the connection is not mutual. Examples include:
    
    *   Webpage links (where a link from page A to page B does not imply a link from B to A).
        
    *   Task scheduling (where one task must be completed before another can start).
        
    *   Social networks (where one user can follow another without the need for mutual following).
        

### Properties of Directed Graphs

*   For the graph above:
    
    *   The **in-degree** of a vertex is the number of edges coming into that vertex.
        
    *   The **out-degree** of a vertex is the number of edges going out from that vertex.
        
    
    *   In-Degree of A = 0 (no edges coming into A)
        
    *   Out-Degree of A = 2 (edges going to B and C)
        
    *   In-Degree of B = 1 (edge coming from A)
        
    *   Out-Degree of B = 1 (edge going to C)
        
    *   In-Degree of C = 2 (edges coming from A and B)
        
    *   Out-Degree of C = 1 (edge going to D)
        
    *   In-Degree of D = 1 (edge coming from C)
        
    *   Out-Degree of D = 0 (no edges going out from D)
        
*   **Connectedness**: A directed graph can be strongly connected, weakly connected, or disconnected. A directed graph is strongly connected if there is a directed path from every vertex to every other vertex. In the example above, the graph is not strongly connected because there is no path from D to A or B.
    
*   **Cycles**: A directed graph can contain directed cycles, which are paths that start and end at the same vertex, following the direction of the edges. In the example above, there are no directed cycles.
    

This example illustrates the basic structure and properties of a directed graph, highlighting the importance of direction in the relationships between vertices.

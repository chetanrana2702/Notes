## Weighted Graph

- A weighted graph is a type of graph in which each edge has an associated numerical value, called a weight. 
- The weight can represent various things, such as cost, distance, time, or any other metric that quantifies the relationship between the vertices connected by the edge.

### Example of a Weighted Graph

Consider a simple weighted graph with the following vertices and edges:

*   **Vertices (Nodes)**: A, B, C, D
    
*   **Edges with Weights**:
    
    *   (A, B) with weight 4
        
    *   (A, C) with weight 2
        
    *   (B, C) with weight 5
        
    *   (B, D) with weight 10
        
    *   (C, D) with weight 3
        

This can be visually represented as:

```
        4
    A------B
    | \  / | 
 2  |  \/ 5| 10
    |  /\  |   
    C------D
       3
```

### Explanation

1.  **Vertices**: The graph has four vertices: A, B, C, and D. Each vertex can represent an entity, such as a city, a task, or any other object.
    
2.  **Edges with Weights**: The edges represent connections between the vertices, and each edge has a weight associated with it:
    
    *   The edge (A, B) has a weight of 4, which could represent the distance between A and B.
        
    *   The edge (A, C) has a weight of 2, indicating a shorter distance between A and C.
        
    *   The edge (B, C) has a weight of 5, representing the distance from B to C.
        
    *   The edge (B, D) has a weight of 10, indicating a longer distance from B to D.
        
    *   The edge (C, D) has a weight of 3, representing the distance from C to D.
        
3.  **Applications**: Weighted graphs are commonly used in various applications, including:
    
    *   **Transportation Networks**: Where weights represent distances or travel times between locations (e.g., roads between cities).
        
    *   **Network Routing**: Where weights can represent the cost of data transmission or latency in communication networks.
        
    *   **Project Management**: Where weights can represent the time or resources required to complete tasks in a project.
        

### Properties of Weighted Graphs

*   **Shortest Path**: One of the primary applications of weighted graphs is finding the shortest path between two vertices. Algorithms like Dijkstra's algorithm or the Bellman-Ford algorithm can be used to determine the path with the minimum total weight.
    
*   **Minimum Spanning Tree**: In a weighted graph, a minimum spanning tree (MST) is a subset of the edges that connects all vertices with the minimum possible total edge weight. Algorithms like Prim's or Kruskal's can be used to find the MST.
    
*   **Weighted Degree**: The weighted degree of a vertex can be defined as the sum of the weights of all edges connected to that vertex. For example, in the graph above:
    
    *   Weighted degree of A = 4 + 2 = 6
        
    *   Weighted degree of B = 4 + 5 + 10 = 19
        
    *   Weighted degree of C = 2 + 5 + 3 = 10
        
    *   Weighted degree of D = 10 + 3 = 13
        

This example illustrates the basic structure and properties of a weighted graph, emphasizing the significance of weights in determining the relationships between vertices.
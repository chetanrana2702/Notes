## Undirected Graph

- An undirected graph is a type of graph in which the edges have no direction. 
- This means that the connection between two vertices (or nodes) is bidirectional; if there is an edge between vertex A and vertex B, you can traverse from A to B and from B to A without any restrictions.

### Example of an Undirected Graph

Consider a simple undirected graph with the following vertices and edges:

- Vertices (Nodes): A, B, C, D
- Edges:
    - (A, B)
    - (A, C)
    - (B, C)
    - (C, D)

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
    
2.  **Edges**: The edges represent the connections between the vertices:
    
    *   The edge (A, B) indicates that there is a connection between vertex A and vertex B.
        
    *   The edge (A, C) indicates a connection between vertex A and vertex C.
        
    *   The edge (B, C) indicates a connection between vertex B and vertex C.
        
    *   The edge (C, D) indicates a connection between vertex C and vertex D.
        
3.  **Bidirectionality**: 
    - Since this is an undirected graph, the edges do not have a direction. For example, if you want to go from A to B, you can do so, and you can also go from B to A. 
    - This is in contrast to a directed graph, where edges have a specific direction (e.g., A → B does not imply B → A).
    
4.  **Applications**: Undirected graphs are commonly used to model relationships where the connection is mutual. Examples include:
    
    *   Social networks (where friendships are mutual).
        
    *   Road networks (where roads allow travel in both directions).
        
    *   Undirected communication networks (where devices can send and receive messages to and from each other).

### Properties of Undirected Graphs

*   **Degree of a Vertex**: The degree of a vertex in an undirected graph is the number of edges connected to it. For example, in the graph above:
    
    *   Degree of A = 2 (connected to B and C)
        
    *   Degree of B = 2 (connected to A and C)
        
    *   Degree of C = 3 (connected to A, B, and D)
        
    *   Degree of D = 1 (connected to C)
        
*   **Connectedness**: An undirected graph is connected if there is a path between every pair of vertices. In the example above, the graph is connected because you can reach any vertex from any other vertex.
    
*   **Cycles**: An undirected graph can contain cycles, which are paths that start and end at the same vertex without traversing any edge more than once. In the example, the path A -> B -> C -> A forms a cycle.
    

This simple example illustrates the basic structure and properties of an undirected graph.
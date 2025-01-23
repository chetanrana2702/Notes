## Complete Graph

- A complete graph is a type of graph in which every pair of distinct vertices is connected by a unique edge. 
- In other words, in a complete graph, there is an edge between every possible pair of vertices. 
- Complete graphs are denoted as ( K_n ), where ( n ) is the number of vertices in the graph.

### Example of a Complete Graph
Let's consider a complete graph with 4 vertices, denoted as ( K_4 ). The vertices can be labeled as ( A, B, C, ) and ( D ).

```
    A
   /|\
  / | \
 B--+--C
  \ | /
   \|/
    D
```

### Explanation

1.  **Vertices and Edges**:
    
    *   In ( K_4 ), there are 4 vertices: ( A, B, C ) and ( D ).
        
    *   The edges connecting these vertices are:
        
        *   ( A ) to ( B ) (edge ( AB ))
            
        *   ( A ) to ( C ) (edge ( AC ))
            
        *   ( A ) to ( D ) (edge ( AD ))
            
        *   ( B ) to ( C ) (edge ( BC ))
            
        *   ( B ) to ( D ) (edge ( BD ))
            
        *   ( C ) to ( D ) (edge ( CD ))
            
2.  **Total Number of Edges**:
    
    *   The total number of edges in a complete graph with ( n ) vertices can be calculated using the formula: `Number of edges = n(n - 1) / 2 `
        
    *   For ( K_4 ): 
    `Number of edges = 4(4 - 1) / 2 = 4(3) / 2 = 6 `
        
    *   This matches the 6 edges listed above.
        
3.  **Properties of Complete Graphs**:
    
    *   **Fully Connected**: Every vertex is directly connected to every other vertex, making complete graphs maximally connected.
        
    *   **Symmetry**: Complete graphs are symmetric; the structure looks the same from any vertex's perspective.
        
    *   **Planarity**: Complete graphs with 4 or fewer vertices ( K_1, K_2, K_3, K_4 ) can be drawn in a plane without edges crossing. However, ( K_5 ) (the complete graph with 5 vertices) cannot be drawn in a plane without edges crossing, making it non-planar.
        
4.  **Applications**:
    
    *   Complete graphs are often used in network design, where every node needs to communicate with every other node.
        
    *   They are also used in combinatorial problems, graph theory, and in algorithms that require a fully connected structure.
        

### Conclusion

In summary, a complete graph is a graph in which every pair of distinct vertices is connected by a unique edge. The complete graph ( K_n ) has ( n ) vertices and ( n(n-1)/2 ) edges, making it a highly connected structure. Understanding complete graphs is essential in various fields, including computer science, network theory, and combinatorial optimization.
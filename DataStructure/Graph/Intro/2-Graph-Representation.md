## Graph Representation Examples

Represent a graph using different methods: 
- The adjacency matrix, adjacency list, and edge list. These representations allow us to store the graph data efficiently and perform graph algorithms. 
- We will provide examples using an undirected graph and a directed graph.

#### 1. **Adjacency Matrix**

An **adjacency matrix** is a 2D array or table where each element A[i][j] indicates whether there is an edge from vertex i to vertex j.

*   **For an unweighted graph**, the matrix contains 1 if there is an edge between vertex i and vertex j, and 0 if there is no edge.
    
*   **For a weighted graph**, the matrix contains the weight of the edge between vertices i and j, and 0 or some other representation for non-existent edges.
    

##### Example: Undirected Graph

Consider the following undirected graph:
```
      A
     / \
    B---C
     \
      D
```
Vertices: A, B, C, D

Edges: (A,B),(A,C),(B,C),(B,D)

##### Adjacency Matrix for the Undirected Graph:

|   | A | B | C | D |
|---|---|---|---|---|
| A | 0 | 1 | 1 | 0 |
| B | 1 | 0 | 1 | 1 |
| C | 1 | 1 | 0 | 0 |
| D | 0 | 1 | 0 | 0 |

*   The matrix is symmetric because the graph is undirected (i.e., if (A,B) exists, then (B,A) also exists).

##### Example: Directed Graph

Consider the following directed graph:
```
A → B
↓   ↓
C ← D
```

Vertices: A, B, C, D
Edges: (A,B), (A,C), (B,D), (C,D)

##### Adjacency Matrix for the Directed Graph:

|   | A | B | C | D |
|---|---|---|---|---|
| A | 0 | 1 | 1 | 0 |
| B | 0 | 0 | 0 | 1 |
| C | 0 | 0 | 0 | 1 |
| D | 0 | 0 | 0 | 0 |

*   The matrix is not symmetric because the graph is directed (i.e., the edge A → B exists, but B → A does not).

#### 2. **Adjacency List**

An **adjacency list** is an array (or list) of lists, where each element of the array corresponds to a vertex and contains a list of adjacent vertices (neighbors). This representation is efficient in terms of space for sparse graphs, where the number of edges is much smaller than the square of the number of vertices.

##### Example: Undirected Graph

Consider the same undirected graph:
```
      A
     / \
    B---C
     \
      D
```
Vertices: A, B, C, D

Edges: (A,B), (A,C), (B,C), (B,D)

##### Adjacency List for the Undirected Graph:

*   A: [B, C]
    
*   B: [A, C, D]
    
*   C: [A, B]
    
*   D: [B]
    
*   Each vertex points to its list of adjacent vertices. In an undirected graph, each edge is listed twice (once for each vertex it connects).
    

##### Example: Directed Graph

Consider the directed graph:
```
A → B
↓   ↓
C ← D
```
Vertices: A, B, C, D

Edges: (A,B),(A,C),(B,D),(C,D)

##### Adjacency List for the Directed Graph:

*   A: \[B, C\]
    
*   B: \[D\]
    
*   C: \[D\]
    
*   D: \[\]
    
*   Each vertex points to the list of vertices that are reachable by directed edges. Notice that there is no edge from D to any other vertex, so D has an empty list.

#### 3. **Edge List**

An **edge list** is a collection of all the edges in the graph, where each edge is represented as a pair (or triplet for weighted graphs) of vertices. This is one of the simplest and most compact ways to represent a graph, especially when you only need to work with edges.

##### Example: Undirected Graph

Consider the undirected graph:

```
      A
     / \
    B---C
     \
      D
```
Vertices: A, B, C, D

Edges: (A,B), (A,C), (B,C), (B,D)

##### Edge List for the Undirected Graph:
```
[(A,B),(A,C),(B,C),(B,D)]
```

*   Each edge is represented as a pair of vertices.
    
*   Since the graph is undirected (A, B) represents the same relationship as (B, A).

##### Example: Directed Graph

Consider the directed graph:
```
      A → B
      ↓   ↓
      C ← D
```
Vertices: A, B, C, D

Edges: (A,B), (A,C), (B,D), (C,D)

**Edge List for the Directed Graph:**
```
[(A,B),(A,C),(B,D),(C,D)]
```
*   Each edge is represented as a directed pair of vertices.
    
*   This representation does not explicitly distinguish between incoming and outgoing edges for each vertex.


#### 4. Comparison of Representations

| Representation      | Memory Usage   | Efficient for     | Use Cases                                                                                     |
|---------------------|----------------|--------------------|-----------------------------------------------------------------------------------------------|
| Adjacency Matrix    | \( O(V^2) \)   | Dense graphs       | Suitable for small, dense graphs or when quick access to edge existence is needed.          |
| Adjacency List      | \( O(V + E) \) | Sparse graphs      | Ideal for sparse graphs where there are relatively few edges compared to vertices.           |
| Edge List           | \( O(E) \)     | Sparse or edge-focused | Good for iterating over all edges, such as when performing edge-based algorithms.            |


#### 5. **Choosing the Right Representation**

The choice of representation depends on the characteristics of the graph and the types of operations you need to perform:

*   **Adjacency Matrix**: Best suited for dense graphs or when you need to frequently check if an edge exists between two vertices.
    
*   **Adjacency List**: Best for sparse graphs, where there are fewer edges than vertices, and you need to iterate over the neighbors of a vertex.
    
*   **Edge List**: Best for applications where edges are the primary focus, and the graph is not too large. It's efficient for iterating over all edges.
    

#### 6. **Conclusion**

- Understanding the different ways to represent a graph is crucial for implementing graph algorithms and solving problems effectively. 
- Each representation has its strengths and is suited for different types of graphs and operations. 
- By choosing the right representation for a given task, you can optimize both time and space efficiency.
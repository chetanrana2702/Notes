## Types Of Graphs

- Graphs are mathematical structures used to model pairwise relationships between objects. 
- They can be classified based on their properties, structure, and characteristics. 
- Here are the key types and categories of graphs:

### **Based on Directionality**

1.  **Undirected Graph**:
    
    *   Edges have no direction.
        
    *   Example: A friendship network where if A is friends with B, B is also friends with A.

        
2.  **Directed Graph (Digraph)**:
    
    *   Edges have directions, represented by arrows.
        
    *   Example: A Twitter follower graph where A follows B, but B may not follow A.

### **Based on Weight**

1.  **Weighted Graph**:
    
    *   Edges have weights or costs associated with them (e.g., distance, time, capacity).
        
    *   Example: A road network with distances marked on edges.
        
2.  **Unweighted Graph**:
    
    *   Edges do not have any weights.
        
    *   Example: A social network where edges only represent relationships.

### **Based on Connectivity**

1.  **Connected Graph**:
    
    *   There is a path between every pair of vertices.
        
    *   Example: A network of computers where all are reachable from one another.
        
2.  **Disconnected Graph**:
    
    *   At least one pair of vertices has no path connecting them.
        
3.  **Strongly Connected Graph**:
    
    *   In a directed graph, every vertex is reachable from every other vertex.
        
4.  **Weakly Connected Graph**:
    
    *   In a directed graph, replacing all directed edges with undirected edges results in a connected graph.

### **Special Types of Graphs**

1.  **Complete Graph (Kₙ)**:
    
    *   Every pair of vertices is connected by a unique edge.
        
    *   Example: A fully connected network.
        
2.  **Cycle Graph**:
    
    *   A graph where all vertices form a closed loop.
        
    *   Example: A circular route.
        
3.  **Path Graph**:
    
    *   A graph where all vertices are connected in a single straight line.
        
4.  **Tree**:
    
    *   A connected, acyclic graph.
        
    *   Example: A file directory structure.
        
5.  **Forest**:
    
    *   A collection of disjoint trees.
        
6.  **Bipartite Graph**:
    
    *   Vertices can be divided into two disjoint sets, and edges only connect vertices from different sets.
        
    *   Example: A job allocation graph.
        
7.  **Planar Graph**:
    
    *   Can be drawn on a plane without any edges crossing.
        
    *   Example: A map of countries with shared borders.
        
8.  **Regular Graph**:
    
    *   All vertices have the same degree (number of edges).
        
9.  **Star Graph**:
    
    *   A single central node connected to all other nodes, forming a star shape.
        
10.  **Wheel Graph**:
    
        *  A cycle graph with an additional central node connected to all other vertices.
        
11.  **Hypergraph**:
    
        *   An edge can connect more than two vertices.

### **Based on Dynamic Properties**

1.  **Static Graph**:
    
    *   Structure does not change over time.
        
2.  **Dynamic Graph**:
    
    *   Vertices and edges can be added or removed over time.

### **Based on Applications**

1.  **Flow Network**:
    
    *   Directed graph where each edge has a capacity, used in problems like maximum flow.
        
    *   Example: Water or electricity distribution network.
        
2.  **Social Network Graph**:
    
    *   Models relationships among people or entities.
        
3.  **Knowledge Graph**:
    
    *   Represents entities and their relationships, often used in AI and machine learning.
        
4.  **Transportation Network Graph**:
    
    *   Models transportation systems like roads, railways, or air routes.

### **Mathematical Properties**

1.  **Sparse Graph**:
    
    *   Contains relatively few edges compared to the maximum possible edges.
        
2.  **Dense Graph**:
    
    *   Contains a large number of edges, close to the maximum possible.
        
3.  **Cyclic Graph**:
    
    *   Contains at least one cycle (a path where the start and end vertex are the same).
        
4.  **Acyclic Graph**:
    
    *   Contains no cycles.
        
    *   Example: Trees and Directed Acyclic Graphs (DAGs).


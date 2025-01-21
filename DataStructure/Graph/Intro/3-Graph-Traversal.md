## Depth First Search

DFS (Depth-First Search) and BFS (Breadth-First Search) are two common graph traversal algorithms used to explore nodes and edges of a graph, such as in a tree or a network. Both are fundamental techniques in computer science, but they differ in how they explore the graph.

### Depth-First Search (DFS)

*   **Approach**: DFS explores a graph by going as deep as possible along each branch before backtracking. It starts at the root (or any arbitrary node) and explores each branch before moving to the next branch.
    
*   **Data structure used**: DFS uses a **stack** (either explicitly or via recursion).
    
*   **Order of traversal**: It goes deeper into the graph first and backtracks when it hits a dead end.
    
*   **Applications**: DFS is used in applications like pathfinding, puzzle-solving (e.g., mazes), topological sorting, and cycle detection in graphs.
    

**Steps**:

1.  Start at the root (or any arbitrary node).
    
2.  Visit the node and mark it as visited.
    
3.  For each unvisited neighboring node, apply DFS recursively.
    
4.  If no unvisited neighbors are found, backtrack to the previous node.
    

### Breadth-First Search (BFS)

*   **Approach**: BFS explores a graph level by level, starting from the root (or any arbitrary node) and visiting all neighbors before moving to the next level of nodes.
    
*   **Data structure used**: BFS uses a **queue** to manage the nodes to be explored.
    
*   **Order of traversal**: It explores all neighbors at the present depth level before moving on to nodes at the next depth level.
    
*   **Applications**: BFS is used for finding the shortest path in unweighted graphs, solving problems like shortest path in a maze, and level-order traversal in trees.
    

**Steps**:

1.  Start at the root (or any arbitrary node).
    
2.  Visit the node and enqueue its unvisited neighbors.
    
3.  Dequeue a node from the queue and visit it, then enqueue its unvisited neighbors.
    
4.  Repeat until all nodes have been visited.
    

### Key Differences:

1.  **Traversal order**: DFS goes deep along a branch before backtracking, while BFS explores all nodes at the present depth before moving to the next level.
    
2.  **Data structure**: DFS uses a stack (LIFO), while BFS uses a queue (FIFO).
    
3.  **Memory usage**: DFS may require less memory if the tree/graph is deep, while BFS may require more memory if the tree/graph is wide because it stores all nodes at the current level.
    

In summary:

*   **DFS**: Deep dive, stack-based, backtracks.
    
*   **BFS**: Level-by-level, queue-based, explores neighbors first.
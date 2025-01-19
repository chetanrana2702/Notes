## Red Black Tree (Type of Balanced Binary Tree)

- A **Red-Black Tree** is a type of self-balancing binary search tree that ensures the tree remains approximately balanced, providing efficient operations for insertion, deletion, and search. 
- It is widely used in computer science for implementing associative arrays and sets. 
- The tree maintains balance by enforcing a set of properties during modifications (insertion or deletion).

### Properties of a Red-Black Tree:

1.  **Node Color**: Each node is either red or black.
    
2.  **Root Property**: The root of the tree is always black.
    
3.  **Red-Black Property**: No two consecutive red nodes are allowed (a red node cannot have a red parent or child).
    
4.  **Black-Height Property**: Every path from a node to its descendant null pointers (or leaves) contains the same number of black nodes.
    
5.  **Leaves**: All leaves (or null pointers) are considered black.
    

### Key Operations and Time Complexity:

*   **Search**: O(log ⁡n)
    
*   **Insertion**: O(log ⁡n), with re-balancing if necessary.
    
*   **Deletion**: O(log ⁡n), with re-balancing if necessary.
    

### Balancing Mechanism:

Red-Black Trees use **rotations** and **color flips** to maintain their properties:

*   **Rotations** (left or right): Adjust the structure of the tree while preserving the binary search tree property.
    
*   **Recoloring**: Changes the colors of nodes to maintain the Red-Black Tree properties.
    

### Advantages:

*   Guarantees that the tree's height is O(log ⁡n), where n is the number of nodes.

*   Easier to implement than some other self-balancing trees like AVL trees.
    
*   Efficient for scenarios requiring frequent insertions and deletions while maintaining ordered data.

### Complexity Analysis
*   **Time Complexity**:
    
    *   Search: O(log⁡n)
        
    *   Insert/Delete: O(log⁡n)
        
*   **Space Complexity**: O(n)


### Applications:

*   Used in implementations of associative containers like std::map and std::set in C++.
    
*   Basis for the TreeMap and TreeSet classes in Java.
    
*   Database systems and memory allocators.
    

By maintaining a balanced structure, Red-Black Trees ensure efficient operation for various dynamic sets and dictionary operations.
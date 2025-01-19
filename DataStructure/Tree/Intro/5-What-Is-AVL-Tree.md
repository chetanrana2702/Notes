## AVL Tree (Type Of Balanced Binary Tree)

An **AVL tree** is a type of self-balancing binary search tree (BST), named after its inventors **Adelson-Velsky and Landis**. It ensures that the tree remains approximately balanced after every insertion or deletion operation, maintaining logarithmic time complexity for basic operations like search, insertion, and deletion.

### Key Characteristics of AVL Tree:

1.  **Balance Factor**:
    
    *   Each node in an AVL tree has a balance factor, defined as the height difference between its left and right subtrees:
        ```
        Balance Factor = Height of Left Subtree − Height of Right Subtree
        ```
        
    *   The balance factor for every node must be -1, 0, or 1. If the balance factor falls outside this range, the tree is rebalanced.
        
2.  **Rebalancing**:
    
    *   Rebalancing is done using **rotations**:
        
        *   **Single Rotations**:
            
            *   Left Rotation (LL imbalance)
                
            *   Right Rotation (RR imbalance)
                
        *   **Double Rotations**:
            
            *   Left-Right Rotation (LR imbalance)
                
            *   Right-Left Rotation (RL imbalance)
                
    *   These rotations ensure that the height difference remains within the acceptable range.
        
3.  **Height-Balanced Property**:
    
    *   An AVL tree is always height-balanced, meaning the difference in height between the left and right subtrees of any node is at most 1.
        

### Advantages of AVL Tree:

*   Guaranteed logarithmic time complexity for search, insert, and delete operations.
    
*   Suitable for applications requiring frequent searches.
    

### Disadvantages of AVL Tree:

*   Slightly more complex to implement compared to a standard BST due to the need for rotations.
    
*   Insertions and deletions are slower than in an unbalanced BST because of the additional rebalancing step.
    

### Example of AVL Tree:

Consider the sequence of numbers inserted into an AVL tree: **10, 20, 30**.

- After inserting **10**:
    ```
        10
    ```

- After inserting 20:

    ```
        10
        \
        20
    ```

- After inserting 30, the tree becomes unbalanced (right-heavy). A left rotation on 10 results in:

    ```
      20
     /  \
    10   30
    ```

Now the tree is balanced again.

**Applications:**

- Databases and file systems.
- Memory management in operating systems.
- Situations requiring fast lookups.
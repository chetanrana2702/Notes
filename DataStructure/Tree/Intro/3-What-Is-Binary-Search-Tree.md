## Binary Search Tree

A **Binary Search Tree (BST)** is a type of binary tree that satisfies the following properties:

### Key Characteristics of a Binary Search Tree:

1.  **Node Structure**:Each node in a BST contains:
    
    *   A value (key).
        
    *   A pointer/reference to the left child.
        
    *   A pointer/reference to the right child.
        
2.  **Binary Property**:Each node has at most two children: the left child and the right child.
    
3.  **Search Property**:
    
    *   **Left Subtree**: All nodes in the left subtree of a node have values smaller than the node's value.
        
    *   **Right Subtree**: All nodes in the right subtree of a node have values greater than the node's value.
        
    *   This property ensures that for any node, all values in its left subtree are less, and all values in its right subtree are greater.
        
4.  **Recursive Nature**: A BST is recursive in nature, meaning:
    
    *   The left and right subtrees of a BST are also BSTs.
        

### Operations on a BST:

1.  **Search**: Efficiently find whether a value exists in the tree, typically with O(log⁡n) time complexity in a balanced tree.
    
2.  **Insertion**: Insert a new value while maintaining the BST properties.
    
3.  **Deletion**: Remove a node and adjust the tree to preserve the BST properties.
    
    *   Special cases include deleting a node with no children, one child, or two children.
        
4.  **Traversal**:
    
    *   **In-order Traversal**: Visits nodes in sorted order.
        
    *   **Pre-order and Post-order Traversals**: Used for specific tree operations.
        

### Advantages:

*   **Efficiency**: Search, insertion, and deletion operations are O(log⁡n) in a balanced BST.
    
*   **Dynamic Set**: Allows efficient dynamic set operations like union and intersection.
    

### Limitations:

*   **Unbalanced Trees**: If the tree becomes unbalanced (e.g., all nodes inserted in increasing order), the time complexity for operations can degrade to O(n).
    

### Example:

A BST with the following structure:

```
        50
       /  \
     30    70
    / \    / \
   20 40  60 80

```

*   **In-order traversal:** 20, 30, 40, 50, 60, 70, 80.
    
*   **Searching for 40:** Start at root (50), move to the left subtree (30), then to the right (40).
    

Variants like **self-balancing BSTs** (e.g., AVL Tree, Red-Black Tree) address the unbalanced tree issue by automatically maintaining balance during insertions and deletions.
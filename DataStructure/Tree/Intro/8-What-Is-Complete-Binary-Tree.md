## What Is Complete Binary Tree

A **Complete Binary Tree** is a binary tree in which every level, except possibly the last, is completely filled, and all nodes are as far left as possible. In other words, the tree is "complete" if every level is fully populated with nodes, and any missing nodes on the last level are positioned as far left as possible.

### Characteristics of a Complete Binary Tree:

1.  **All levels are full except possibly the last**:
    
    *   All levels of the tree are fully populated with nodes, except for the last level, which may have fewer nodes.
        
    *   The last level’s nodes are arranged as left as possible.
        
2.  **Nodes in the last level are positioned leftmost**:
    
    *   If there are missing nodes on the last level, they must be on the right side of the level and the missing spots must be as left as possible.
        
3.  **Balanced structure**:
    
    *   It ensures the tree is balanced up to the last level. The tree's height is minimal for the number of nodes.
        
4.  **Height of the tree**:
    
    *   The height of a complete binary tree is roughly ⌊log⁡2N⌋, where N is the total number of nodes in the tree.
        
5.  **Efficient in terms of storage and traversal**:
    
    *   Because of its structure, complete binary trees are often used for efficient implementation of data structures like heaps (e.g., max-heaps and min-heaps).
        

### Example:

For a complete binary tree with 7 nodes:
```
        1
       / \
      2   3
     / \ / \
    4  5 6  7
```

This is a complete binary tree because all levels are fully filled except the last one, and the nodes on the last level are left-justified.
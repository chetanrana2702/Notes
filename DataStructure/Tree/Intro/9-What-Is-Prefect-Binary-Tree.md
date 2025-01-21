## What Is Perfect Binary Tree

A **Perfect Binary Tree** is a type of binary tree in which all the interior nodes have exactly two children, and all leaf nodes are at the same level or depth.

### Characteristics of a Perfect Binary Tree:

1.  **All internal nodes have two children**: Every non-leaf node (internal node) has exactly two children—one left and one right.
    
2.  **All leaf nodes are at the same level**: The leaf nodes (nodes with no children) are all located at the same level or depth of the tree. This ensures that the tree is "complete" in terms of the number of levels.
    
3.  **Height of the tree**: In a perfect binary tree, if the tree has a height of hhh, then the total number of nodes in the tree will be 2h+1−12^{h+1} - 12h+1−1, where hhh is the number of edges on the longest path from the root to any leaf.
    
4.  **Balanced structure**: A perfect binary tree is always balanced, meaning the left and right subtrees of every node differ in height by no more than one.
    
5.  **Symmetry**: A perfect binary tree is symmetrical; the left and right subtrees of every node are mirror images of each other in terms of structure.
    

### Example:

A perfect binary tree of height 2:
```
        1
      /   \
     2     3
    / \   / \
   4   5 6   7
```

*   The root node is 1, with two children, 2 and 3.
    
*   Node 2 has children 4 and 5, and node 3 has children 6 and 7.
    
*   All the leaf nodes (4, 5, 6, 7) are at level 2.
    

In this case, the number of nodes is 2(2+1) −1 = 7
## Balanced Binary Tree

A **balanced binary tree** is a type of binary tree where the height difference between the left and right subtrees of every node is minimized. This ensures that the tree remains as flat as possible, which helps optimize operations like insertion, deletion, and searching.

### Key Characteristics:

1.  **Height Difference Constraint**:
    
    *   For every node in the tree, the height difference (or balance factor) between the left and right subtrees is either 0, 1, or -1.
        
    *   This constraint ensures that the tree does not degenerate into a linear structure, maintaining efficient operations.
        
2.  **Efficiency**:
    
    *   **Searching:** O(log⁡n)
        
    *   **Insertion:** O(log⁡n)
        
    *   **Deletion:** O(log⁡n) These time complexities are possible because the height of the tree is kept proportional to log n, where nnn is the number of nodes.
        
3.  **Self-Balancing Trees**:
    
    *   A balanced binary tree is often implemented with additional rules to maintain balance after insertions or deletions. Examples include:
        
        *   **AVL Tree**: Ensures that the height difference between left and right subtrees for any node is at most 1.
            
        *   **Red-Black Tree**: A binary search tree where nodes have an additional color property to ensure the tree remains approximately balanced.

### Example:
Consider this balanced binary tree:

```
       5
      / \
     3   7
    / \   \
   2   4   8

```
- The height difference between left and right subtrees for every node is within the allowed range, making it balanced.

By contrast, this is an **unbalanced binary tree:**

```
       5
      /
     3
    /
   2
```

- Here, the left subtree's height exceeds the right subtree's height by more than 1, making it unbalanced.

### Applications:
Balanced binary trees are widely used in:

- **Databases** (e.g., B-trees for indexing)
- **File systems**
- **Memory management**
- **Efficient searching and sorting algorithms**


A **Balanced Binary Tree** (BBT) ensures that the time complexity of common operations such as insert, delete, and search is O(log⁡n).

In contrast, an **Unbalanced Binary Tree** (UBT) can degrade these operations to O(n) in the worst case.

## Balanced Binary Tree (BBT)

A Balanced Binary Tree is defined by the property that every node’s left and right subtrees have heights that differ by at most 1:

```
| height(left) - height(right) | <= 1
```

### Maximum Nodes

The maximum number of nodes for a tree of height \( h \) is given by:

```
[2^h - 1]
```
This indicates that a BBT’s height and node count are directly related.



### Unbalanced Binary Tree (UBT)

An Unbalanced Binary Tree does not have specific criteria defining balance. 

### Node Count

It can have as few as \( h + 1 \) nodes or as many as \( 2^h - 1 \) nodes for a specific height \( h \).

## B-Tree

- A **B-tree** is a self-balancing search tree data structure that maintains sorted data and allows for efficient insertion, deletion, and search operations especially in disk-based systems. 
- It is widely used in databases and file systems due to its ability to handle large amounts of data while maintaining good performance.
- Also known as Multi-way Search Tree.


Here is a comprehensive explanation of the B-tree:

### **Definition**

A B-tree is a generalization of a binary search tree in which a node can have more than two children. It ensures that:

1.  The tree is balanced, meaning all leaf nodes are at the same depth.
    
2.  Nodes are maintained in a sorted order, facilitating fast searches.
    

### **Properties**

1.  **Node Structure**:
    
    *   Each node contains a certain number of keys and child pointers.
        
    *   The keys in each node are sorted in ascending order.
        
2.  **Order (m)**:
    
    *   The order mmm of a B-tree determines the range of keys each node can contain.
        
    *   Each internal node can have at most m − 1 keys and m children.
        
    *   A node must have at least ⌈m/2⌉ − 1  keys (except the root, which may have fewer keys).
        
3.  **Height**:
    
    *   The height of the tree is kept as small as possible by ensuring a balanced structure. This minimizes the number of disk I/O operations in applications like databases.
        
4.  **Keys**:
    
    *   Keys within a node are sorted, and all the keys in a subtree to the left of a key k are less than k, while all the keys in the subtree to the right are greater than k.
        

### **Operations**

#### 1\. **Search**

*   The search operation is similar to binary search. Start at the root, compare the key to the keys in the node, and decide which child subtree to follow.
    
*   Time complexity: O(log ⁡n).
    

#### 2\. **Insertion**

*   Insertions start at the leaf nodes.
    
*   If a node exceeds the maximum number of keys (m−1m-1m−1) after insertion, it is split into two nodes, and the middle key is promoted to the parent node.
    
*   This splitting may propagate upward, potentially increasing the height of the tree.
    
*   Time complexity: O(log n).
    

#### 3\. **Deletion**

*   Deletion may involve merging or borrowing keys from neighboring nodes to maintain the tree's properties.
    
*   Keys are removed from leaf nodes, and the structure is adjusted to maintain balance.
    
*   Time complexity: O(log n).
    

### **Advantages**

1.  **Efficient Disk Reads**:
    
    *   B-trees are optimized for systems that read and write large blocks of data. Nodes are designed to fit within disk pages, minimizing I/O operations.
        
2.  **Self-Balancing**:
    
    *   B-trees automatically balance themselves during insertions and deletions, ensuring consistent performance.
        
3.  **Scalability**:
    
    *   Suitable for very large datasets due to their logarithmic height and efficient use of disk space.
        
4.  **Range Queries**:
    
    *   B-trees efficiently support range queries due to their sorted nature.
        

### **Applications**

1.  **Databases**:
    
    *   Widely used for indexing in relational and non-relational databases.
        
2.  **File Systems**:
    
    *   Used in file allocation and directory indexing (e.g., NTFS, HFS+).
        
3.  **Search Engines**:
    
    *   Indexing of large datasets in search engines.
        

### **Example**

Let’s create a B-tree of order 3(m = 3):

1.  **Initial State**:Insert 10. The tree has only one key:
    ```
    [10]
    ```

2.  **Insert 20:**
    ```
    [10, 20]
    ```

3.  **Insert 5:**
    ```
    [5, 10, 20]
    ```

4.  **Insert 30:** The node exceeds the order, so it splits:
    ```
        [10]
        /    \
     [5]    [20, 30]
    ```

5.  **Insert 15:**
    ```
        [10]
        /    \
      [5]    [15, 20, 30]
    ```

## What Are Complex Operations

In the context of B-trees, **complex operations** typically refer to scenarios where the standard operations (like insertion, deletion, and search) require additional steps to handle edge cases while maintaining the structural properties of the B-tree. These operations include:

### 1\. **Splitting Nodes**

*   **When it occurs**: During insertion, if a node exceeds the maximum number of keys <i>(m − 1)</i>.
    
*   **How it works**:
    
    1.  Select the middle key in the overflowing node.
        
    2.  Promote this middle key to the parent node.
        
    3.  Split the overflowing node into two new nodes: one containing the keys smaller than the promoted key, and the other containing the keys larger than the promoted key.
        
*   **Complexity**: The splitting process might propagate up the tree, potentially increasing the height.
    

### 2\. **Merging Nodes**

*   **When it occurs**: During deletion, if a node has fewer than the minimum number of keys (⌈m/2⌉−1) and cannot borrow from a sibling.
    
*   **How it works**:
    
    1.  Merge the underflowing node with one of its siblings.
        
    2.  Move a key from the parent node to the merged node to maintain the B-tree properties.
        
*   **Complexity**: If the parent node becomes underfilled, the merging process might propagate upward.
    

### 3\. **Borrowing Keys (Redistribution)**

*   **When it occurs**: During deletion, if a node has fewer keys than allowed but its sibling has more than the minimum keys.
    
*   **How it works**:
    
    1.  Borrow a key from a sibling node.
        
    2.  Move a key from the parent node to the underfilled node to maintain the B-tree properties.
        
*   **Complexity**: Redistribution is a local operation and does not propagate.
    

### 4\. **Root Splitting**

*   **When it occurs**: During insertion, if the root node becomes full.
    
*   **How it works**:
    
    1.  Split the root into two nodes.
        
    2.  Create a new root node containing the middle key from the original root.
        
    3.  The new root will now have two child pointers, pointing to the two newly created nodes.
        
*   **Complexity**: This operation increases the height of the tree by 1.
    

### 5\. **Root Merging**

*   **When it occurs**: During deletion, if the root becomes empty after a merge.
    
*   **How it works**:
    
    1.  Merge the root’s two children into a single node.
        
    2.  The merged node becomes the new root, reducing the tree's height by 1.
        
*   **Complexity**: Reduces tree height but requires careful handling of pointers.
    

### 6\. **Rebalancing After Deletion**

*   Deletion in B-trees involves:
    
    *   Locating the key to be deleted.
        
    *   Handling underflow cases using merging or redistribution.
        
    *   Ensuring that all nodes (except the root) satisfy the minimum key constraint.
        
*   If the key to be deleted is in an internal node:
    
    1.  Replace it with its **inorder predecessor** (largest key in the left subtree) or **inorder successor** (smallest key in the right subtree).
        
    2.  Recursively delete the replacement key from the subtree.
        
*   This might involve multiple rebalancing steps.
    

### Example of Complex Deletion:

Consider a B-tree of order <i>3(m = 3)</i>:

Initial Tree:
```
       [20]
      /    \
   [10]   [30, 40]

```
1. Delete 40: The leaf node [30, 40] becomes [30].

    ```
       [20]
      /    \
    [10]   [30]
    ```

2. Delete 30: Node [30] becomes underfilled. Since it cannot borrow keys, it merges with [20], making [10] the root:

    ```
    [10, 20]
    ```

These complex operations ensure that the B-tree always maintains its structural properties, regardless of the operations performed on it.
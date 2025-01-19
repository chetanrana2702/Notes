## Tree Data Structure


### Definition
- A tree is a non-linear data structure consisting of nodes connected by edges. 
- It is often used to represent hierarchical relationships, such as filesystems, organizational charts, or parsing expressions.



### Basic Terminology
1. <b>Node:</b> A fundamental part of a tree that contains data and possibly references to other nodes.
    <ul>
    <li><b>Root:</b> The topmost node in a tree.</li>

    <li><b>Child:</b> A node directly connected to another node when moving away from the root.</li>

    <li><b>Parent:</b> A node directly connected to another node when moving toward the root.</li>

    <li><b>Leaf:</b> A node with no children.</li>

    <li><b>Internal Node:</b> A node that has at least one child.</li>
    </ul>

2. <b>Edge:</b> A connection between two nodes.

3. <b>Path:</b> A sequence of nodes and edges connecting a node to another node.

4. <b>Depth:</b> The number of edges from the root to a node.

5. <b>Height:</b> The number of edges in the longest path from a node to a leaf.

6. <b>Subtree:</b> A tree consisting of a node and its descendants.

7. <b>Degree:</b> The number of children a node has.

8. <b>Forest:</b> A collection of disjoint trees.



### Types of Trees

1. #### General Tree:

    - A tree with no constraints on the number of children each node can have.

2. #### Binary Tree:

    - Each node has at most two children, referred to as the left child and the right child.

3. #### Binary Search Tree (BST):

    - A binary tree where the left subtree contains nodes with values less than the parent, and the right subtree contains nodes with values greater than the parent.

4. #### Balanced Tree:

    - A tree where the height difference between the left and right subtrees of any node is minimal.
    Examples: AVL Tree, Red-Black Tree.

5. #### Complete Binary Tree:

    - A binary tree in which all levels are completely filled except possibly the last level, which is filled from left to right.

6. #### Perfect Binary Tree:

    - A binary tree in which all internal nodes have two children, and all leaf nodes are at the same level.

7. #### Full Binary Tree:

    - A binary tree in which every node has either 0 or 2 children.

8. #### Heap:

    - A special tree-based structure satisfying the heap property:
    
    - <b>Max-Heap:</b> Parent nodes are greater than or equal to their children.
    - <b>Min-Heap:</b> Parent nodes are less than or equal to their children.
    

9. #### Trie (Prefix Tree):

    - A tree used to store strings, where each node represents a prefix of the strings.

10. #### N-ary Tree:

    - A tree where each node can have at most N children.

11. #### Segment Tree:

    - Used for range queries and updates.

12. #### Fenwick Tree (Binary Indexed Tree):

    - Used for efficient computation of prefix sums.



### Traversal Techniques
Traversal involves visiting all nodes of a tree in a specific order:

#### 1. Depth-First Search (DFS)
    
- <b>Preorder:</b> Visit root → Traverse left → Traverse right.
- <b>Inorder:</b> Traverse left → Visit root → Traverse right.
- <b>Postorder:</b> Traverse left → Traverse right → Visit root.

#### 2. Breadth-First Search (BFS)
- <b>Level-order traversal:</b> Visit nodes level by level.


### Operations on Trees

1. <b>Insertion:</b> Add a node to the tree.
2. <b>Deletion:</b> Remove a node from the tree.
3. <b>Traversal:</b> Visit nodes in a specific order.
4. <b>Searching:</b> Find a node with a given value.
5. <b>Height Calculation:</b> Determine the height of the tree.
6. <b>Lowest Common Ancestor (LCA):</b> Find the lowest common ancestor of two nodes.
7. <b>Path Finding:</b> Identify the path between two nodes.


### Applications of Trees

1. #### Hierarchical Data Representation:
    - Filesystems, organizational structures.
2. #### Search Operations:
    - Binary Search Trees, Heaps.
3. #### Routing Algorithms:
    - Network routing, spanning trees.
4. #### Data Compression:
    - Huffman coding.
5. #### Databases:
    - B-trees and B+ trees for indexing.
6. #### Artificial Intelligence:
    - Decision trees, game trees.
7. #### Compiler Design:
    - Abstract syntax trees (ASTs).


### Advantages

1. Reflects hierarchical relationships naturally.
2. Efficient search, insert, and delete operations in balanced trees (e.g., O(log n) for AVL trees).
3. Supports operations like range queries (Segment Trees).



### Disadvantages

1. Requires extra memory for pointers.
2. Performance degrades with unbalanced trees.
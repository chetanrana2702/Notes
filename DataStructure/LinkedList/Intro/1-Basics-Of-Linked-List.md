### <b style="color:blue">Linked List</b>
A <b style="color:red">linked list</b> is a linear data structure in which elements, called nodes, are connected by pointers. Each node in a linked list contains two parts:

1.  <b style="color:blue">Data:</b> The value or data the node holds.
    
2.  <b style="color:blue">Pointer (or Reference):</b> A link to the next node in the sequence.
    

### <b style="color:darkorange">Characteristics of a Linked List</b>

*  <b style="color:blue">Dynamic Size:</b> Unlike arrays, linked lists do not have a fixed size and can grow or shrink as needed.
    
*  <b style="color:blue">Efficient Insertions/Deletions:</b> Adding or removing elements is easier and more efficient compared to arrays since no shifting of elements is required.
    
*  <b style="color:blue">No Random Access:</b> Accessing an element requires traversing the list from the beginning, making it slower than arrays for retrieval.
    

### <b style="color:darkorange">Types of Linked Lists</b>

1.  <b style="color:blue">Singly Linked List:</b>
    
    *   Each node contains data and a pointer to the next node.

    *   The last node points to null (or None in Python).
        
2.  <b style="color:blue">Doubly Linked List:</b>
    
    *   Each node contains data, a pointer to the next node, and a pointer to the previous node.
        
    *   Allows traversal in both directions.
        
3.  <b style="color:blue">Circular Linked List:</b>
    
    *   The last node points back to the first node, forming a circle.
        
    *   Can be singly or doubly linked.
        
4.  <b style="color:blue">Doubly Circular Linked List:</b>
    
    *   Combines the features of a doubly linked list and a circular linked list, where the last node points to the first node, and the first node points to the last node.
        

### <b style="color:darkorange">Basic Operations</b>

1.  <b style="color:blue">Traversal:</b> Visiting each node in the list.
    
2.  <b style="color:blue">Insertion:</b> Adding a node at the beginning, middle, or end of the list.
    
3.  <b style="color:blue">Deletion:</b> Removing a node from the beginning, middle, or end of the list.
    
4.  <b style="color:blue">Search:</b> Finding a node with a specific value.
    
5.  <b style="color:blue">Update:</b> Modifying the value of an existing node.


### <b style="color:darkorange">Time Complexity</b>
- <b style="color:blue">Traversal:</b> Scan through nodes — O(n).
- <b style="color:blue">Insertion at the Beginning:</b> Add a node at the start — O(1).
- <b style="color:blue">Insertion (other cases)/Deletion:</b> Add or remove nodes elsewhere in the list — O(n).
- <b style="color:blue">Search:</b> Locate specific nodes — O(n).
- <b style="color:blue">Sorting:</b> Order or organize nodes in the list. Commonly-used algorithms for linked lists like merge sort have a time complexity of O(n logn).
- <b style="color:blue">Merging:</b> Combine two lists — O(n) where n is the total number of nodes in both lists.
- <b style="color:blue">Reversal:</b> Flip node order — O(n).

### <b style="color:darkorange">Use Cases</b>

Linked lists are commonly utilized in real-world applications due to their benefits in dynamic memory management and efficient data manipulation.

1. <b style="color:blue">Dynamic Memory Allocation</b>
    - Linked lists are foundational for managing dynamic memory in operating systems and programming.
    - They help implement memory management algorithms, such as free lists or allocation tables.

2. <b style="color:blue">Implementation of Data Structures</b>
    - Linked lists are used as building blocks for other complex data structures, including:
        - Stacks (using singly linked lists).
        - Queues (using singly or doubly linked lists).
        - Hash tables (for handling collisions through chaining).

3. <b style="color:blue">Undo Functionality in Applications</b>
    - Many software applications (e.g., text editors) use linked lists to implement undo/redo functionality.
    - Each change is stored as a node in the list, allowing traversal to previous or next states.

4. <b style="color:blue">Graph Representation</b>
    - Linked lists are used in adjacency lists to efficiently represent sparse graphs in graph algorithms.

5. <b style="color:blue">Real-Time Systems</b>
    - Linked lists are employed in task scheduling systems where tasks dynamically enter and exit queues.

6. <b style="color:blue">Browser Navigation</b>
    - Doubly linked lists are used to maintain the history of web pages for forward and backward navigation.

7. <b style="color:blue">Music/Playlist Management</b>
    - Applications like media players use linked lists to organize playlists, allowing dynamic addition, deletion, and reordering of tracks.

8. <b style="color:blue">Operating System Kernels</b>
    - Linked lists are extensively used in operating systems for:
        - Process scheduling (e.g., round-robin schedulers).
        - File allocation tables.
        - Management of I/O buffers.


9. <b style="color:blue">Dynamic Hash Tables</b>
    - Linked lists manage collisions in hash tables through chaining, allowing efficient handling of multiple entries with the same hash.

10. <b style="color:blue">Polynomial Manipulation</b>
    - Linked lists are ideal for representing and performing operations on polynomials, where each node contains a term (coefficient and exponent).


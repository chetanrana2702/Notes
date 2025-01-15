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

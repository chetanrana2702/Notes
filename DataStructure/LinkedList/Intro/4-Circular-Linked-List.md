### <b style="color:blue">Circular Linked List</b>

A <b style="color:red">Circular Linked List</b> is a type of linked list in which:
1. The last node points back to the first node, forming a circular structure.
2. It can be either singly linked or doubly linked:
    - In a singly circular linked list, each node has one pointer, and the last node points to the first node.
    - In a doubly circular linked list, each node has two pointers: one pointing to the next node and the other pointing to the previous node. The last node points back to the first, and the first node points back to the last.


<b style="color:darkorange">Characteristics</b>
- There is no <i>NULL</i> in the list (<i style="color:blue">unless it's an empty circular linked list</i>).
- Traversal can continue indefinitely because of the circular reference.

<b style="color:darkorange">Advantages</b>
1. <b style="color:blue">Efficient traversal:</b> You can traverse the entire list starting from any node.
2. <b style="color:blue">Better use of memory:</b> Avoids dangling references to <i>NULL</i>.
3. <b style="color:blue">Useful for cyclic operations:</b> Commonly used in tasks like implementing queues or round-robin scheduling.

<b style="color:darkorange">Disadvantages</b>
1. <b style="color:blue">Complexity:</b> Implementation is slightly more complex than a regular singly or doubly linked list.
2. <b style="color:blue">Infinite loop risk:</b> Care must be taken during traversal to prevent infinite loops.

<b style="color:darkorange">Applications</b>
1. <b style="color:blue">Buffer management:</b> Circular buffers.
2. <b style="color:blue">Round-robin scheduling:</b> In operating systems.
3. <b style="color:blue">Multiplayer games:</b> Representing players in a circle.
4. <b style="color:blue">Data structures:</b> Implementing circular queues and priority queues.

---

<b style="color:darkorange">Key Operations</b>
1. <b style="color:blue">Traversal</b>
    - Begin at any node and continue moving to the next node.
    - Stop traversal when you encounter the starting node again.
    - Example (<i>Singly Circular</i>)
    ```python
    current = head
    while True:
        print(current.data)
        current = current.next
        if current == head:
            break

    ```

2. <b style="color:blue">Insertion</b>
    - <b style="color:deeppink">At the Beginning:</b> Adjust the next pointer of the new node to point to the current head, and the last node’s next to the new head.
    - <b style="color:deeppink">At the End:</b> Adjust the next pointer of the last node to point to the new node, and the new node’s next to the head.
    - <b style="color:deeppink">At a Specific Position:</b> Traverse to the desired position and adjust pointers accordingly.

3. <b style="color:blue">Deletion</b>
    - <b style="color:deeppink">From the Beginning:</b> Adjust the last node’s next pointer to skip the first node and point to the new head.
    - <b style="color:deeppink">From the End:</b> Traverse to the second-to-last node and update its next pointer to point to the head.
    - <b style="color:deeppink">From a Specific Position:</b> Adjust the pointers of the adjacent nodes to exclude the target node.

4. <b style="color:blue">Search</b>
    - Traverse the list and compare the target value with each node’s data until the target is found or the starting node is revisited.



<b style="color:darkorange">Advantages</b>
1. <b style="color:blue">Efficient Continuity:</b> No need for special cases for the first or last node during traversal.
2. <b style="color:blue">Dynamic Size:</b> Can grow or shrink dynamically with no memory waste.
3. <b style="color:blue">Cyclic Nature:</b> Perfect for tasks requiring cyclic iteration, such as round-robin processes.

<b style="color:darkorange">Applications in Depth</b>
1. <b style="color:blue">Circular Buffers</b>
    - Common in data streams or real-time applications where overwriting old data is necessary.
2. <b style="color:blue">Round-Robin Schedulers</b>
    - Circular linked lists help manage processes in a looped fashion.
3. <b style="color:blue">Music Playlists</b>
    - Seamless looping of tracks using circular linked lists.
4. <b style="color:blue">Token Passing in Networks</b>
    - Circular linked lists model the movement of control tokens in ring networks.

<b style="color:darkorange">Disadvantages</b>
1. <b style="color:blue">Complex Traversal:</b> Must keep track of the starting node to prevent infinite loops.
2. <b style="color:blue">Implementation Overhead:</b> More pointer adjustments during insertion or deletion.
3. <b style="color:blue">Debugging Issues:</b> Errors in pointers can cause infinite loops or broken lists.
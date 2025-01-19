### Basics Of Queue

A **queue** is a linear data structure that follows the **First In, First Out (FIFO)** principle. This means that the first element added to the queue is the first one to be removed, much like a real-world queue (e.g., a line of people waiting at a ticket counter).

### Characteristics of a Queue:

1.  **FIFO Order**: Elements are processed in the order they are added.
    
2.  **Two Main Operations**:
    
    *   **Enqueue**: Adding an element to the rear of the queue.
        
    *   **Dequeue**: Removing an element from the front of the queue.
        
3.  **Front and Rear Pointers**:
    
    *   The **front** pointer points to the first element to be dequeued.
        
    *   The **rear** pointer points to the last element added.
        

### Types of Queues:

1.  **Simple Queue**: Operates strictly under the FIFO principle.
    
2.  **Circular Queue**: The last position is connected back to the first position to make a circular connection, efficiently utilizing memory.
    
3.  **Priority Queue**: Elements are dequeued based on priority rather than the order of insertion.
    
4.  **Double-Ended Queue (Deque)**: Elements can be added or removed from both ends.
    

### Applications of Queues:

*   **Operating Systems**: Scheduling tasks (e.g., CPU scheduling, disk scheduling).
    
*   **Network Traffic**: Managing data packets in routers and switches.
    
*   **Printing Jobs**: Managing documents in a print queue.
    
*   **Breadth-First Search (BFS)**: Used in graph and tree traversal.
    

### Implementation:

Queues can be implemented using:

1.  **Arrays**: A fixed-size implementation.
    
2.  **Linked Lists**: A dynamic implementation where each element points to the next.
    
3.  **Stacks**: Using two stacks, a queue can be simulated.
    

Let me know if you'd like to see code examples!
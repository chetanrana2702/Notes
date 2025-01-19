## Priority Queue

A **Priority Queue** is a type of abstract data structure similar to a regular queue or stack but with an added feature: each element is associated with a priority. In a priority queue, the element with the highest priority is dequeued (removed) before elements with lower priority, regardless of the order in which they were enqueued.

**Key Features of a Priority Queue:**
-------------------------------------

1.  **Priority-Based Access:**
    
    *   Unlike a normal queue (FIFO), a priority queue dequeues elements based on their priority.
        
    *   If two elements have the same priority, the tie is resolved based on their insertion order (implementation-specific).
        
2.  **Dynamic Priority Management:**
    
    *   Some implementations allow dynamically changing the priority of elements already in the queue.
        

**Types of Priority Queues:**
-----------------------------

1.  **Ascending Priority Queue:**
    
    *   The element with the lowest priority is dequeued first.
        
2.  **Descending Priority Queue:**
    
    *   The element with the highest priority is dequeued first.
        

**Operations in Priority Queue:**
---------------------------------

| Operation      | Description                                          |
|----------------|------------------------------------------------------|
| Insert/Enqueue | Add an element to the queue with a given priority.  |
| Remove/Dequeue | Remove and return the element with the highest priority. |
| Peek/Top       | View the element with the highest priority without removing it. |
| IsEmpty        | Check if the queue is empty.                        |
| Size           | Get the number of elements in the queue.           |


**Implementation Approaches:**
------------------------------

1.  **Using Arrays or Lists:**
    
    *   Elements are stored in an unsorted array or list, and the highest-priority element is searched upon dequeue.
        
    *   **Pros:** Easy to implement.
        
    *   **Cons:** Inefficient for large datasets (O(n) for dequeue).
        
2.  **Using Sorted Arrays or Lists:**
    
    *   Elements are stored in sorted order based on their priority.
        
    *   **Pros:** Efficient for dequeue operation O(1).
        
    *   **Cons:** Insertion takes O(n) due to sorting.
        
3.  **Using Binary Heaps (Most Common):**
    
    *   A binary heap (min-heap or max-heap) is used, which ensures efficient insertion and removal.
        
    *   **Pros:** Both insertion and removal take O(log n) time.
        
    *   **Cons:** Slightly more complex to implement.
        
4.  **Using Balanced Binary Search Trees:**
    
    *   Priority queues can also be implemented using trees like AVL or Red-Black Trees.
        
    *   **Pros:** Efficient for all operations.
        
    *   **Cons:** More complex than heaps.
        
5.  **Using Fibonacci Heaps:**
    
    *   Provides improved performance for some operations like merging queues.
        
    *   **Pros:** Supports faster decrease-key operation.
        
    *   **Cons:** Complex to implement.
        

**Applications of Priority Queue:**
-----------------------------------

1.  **CPU Scheduling:**
    
    *   Used in operating systems to manage process execution based on priority.
        
2.  **Dijkstra’s Algorithm:**
    
    *   Used in graph algorithms to find the shortest path.
        
3.  **Huffman Coding:**
    
    *   Utilized in data compression algorithms.
        
4.  **Event-Driven Simulations:**
    
    *   Handles events in order of their occurrence time.
        
5.  **AI and Search Problems:**
    
    *   Employed in A\* and other search algorithms.
        
6.  **Job Scheduling:**
    
    *   For prioritizing and executing tasks in real-time systems.


### Example: Priority Queue Implementation in Python Using heapq

Here is a simple Python example using the heapq module:

```python
import heapq

# Initialize an empty priority queue
priority_queue = []

# Add elements with priority
heapq.heappush(priority_queue, (2, "Task A"))  # Priority 2
heapq.heappush(priority_queue, (1, "Task B"))  # Priority 1
heapq.heappush(priority_queue, (3, "Task C"))  # Priority 3

# Remove and return the element with the highest priority (lowest priority number)
while priority_queue:
    priority, task = heapq.heappop(priority_queue)
    print(f"Processing {task} with priority {priority}")

```

### **Advantages:**

*  Efficient priority-based task management.
    
*  Flexible data structure with multiple use cases.
    

### **Disadvantages:**

*  Requires careful handling for dynamic priority updates.
    
*  Some implementations may be less efficient for certain operations.
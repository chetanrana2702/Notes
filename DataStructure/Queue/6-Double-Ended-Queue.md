## Double Ended Queue

A **Double-Ended Queue (Deque)** is a linear data structure that allows insertion and deletion of elements from both ends, i.e., the front and the rear. This flexibility makes it more versatile than a standard queue, which typically allows operations only at one end (enqueue at the rear and dequeue from the front).

### **Key Features of a Deque**

1.  **Bidirectional Operations**:
    
    *   Elements can be added to or removed from either end.
        
2.  **Dynamic Size**:
    
    *   The size of the deque can grow or shrink dynamically as elements are added or removed.
        
3.  **Order Preservation**:
    
    *   Like a queue, elements in a deque are ordered, and their relative positions are maintained.
        

### **Types of Deques**

1.  **Input-Restricted Deque**:
    
    *   Insertion is allowed only at one end, while deletion is allowed at both ends.
        
2.  **Output-Restricted Deque**:
    
    *   Deletion is allowed only at one end, while insertion is allowed at both ends.
        

### **Operations on Deque**

1.  **Insert Front**:
    
    *   Add an element to the front of the deque.
        
2.  **Insert Rear**:
    
    *   Add an element to the rear of the deque.
        
3.  **Delete Front**:
    
    *   Remove an element from the front of the deque.
        
4.  **Delete Rear**:
    
    *   Remove an element from the rear of the deque.
        
5.  **Peek Front**:
    
    *   Retrieve the element at the front without removing it.
        
6.  **Peek Rear**:
    
    *   Retrieve the element at the rear without removing it.
        
7.  **IsEmpty**:
    
    *   Check if the deque is empty.
        
8.  **IsFull** (in a fixed-size implementation):
    
    *   Check if the deque has reached its capacity.
        

### **Applications of Deque**

1.  **Palindrome Checking**:
    
    *   Deques can be used to check if a string is a palindrome by comparing characters from both ends.
        
2.  **Sliding Window Problems**:
    
    *   Often used in algorithms that require processing a window of elements in a list, such as finding the maximum in a sliding window.
        
3.  **Job Scheduling**:
    
    *   Deques are helpful in scheduling jobs where tasks can be added or removed from both ends.
        
4.  **Undo/Redo Operations**:
    
    *   Used in applications like text editors where operations are undone or redone from both ends of a history stack.
        
5.  **Stepping Backward/Forward in Browsers**:
    
    *   Navigational systems can use a deque to manage forward and backward movement.
        

### **Deque Implementation**

A deque can be implemented in various ways:

1.  **Using Arrays**:
    
    *   Fixed-size implementation where the array acts as a circular buffer.
        
2.  **Using Linked List**:
    
    *   Each node contains a reference to the next and previous nodes, allowing dynamic resizing and efficient insertions and deletions.
        
3.  **Using Libraries**:
    
    *   Many programming languages have built-in support for deques. For example:
        
        *   **Python**: collections.deque
            
        *   **C++**: std::deque
            
        *   **Java**: ArrayDeque or LinkedList


## Example

```python
from collections import deque

# Create a deque
dq = deque()

# Insert elements
dq.append(10)        # Add to the rear
dq.appendleft(20)    # Add to the front

# Access elements
print("Front element:", dq[0])
print("Rear element:", dq[-1])

# Remove elements
dq.pop()             # Remove from the rear
dq.popleft()         # Remove from the front

# Check if deque is empty
print("Is empty?", len(dq) == 0)

```

### **Advantages of Deque**

1.  Flexible insertion and deletion.
    
2.  Efficient operations at both ends (constant time in dynamic implementations).
    

### **Disadvantages of Deque**

1.  Random access is not allowed, as deques are not indexable like arrays.
    
2.  Overhead in memory usage if implemented with linked lists.
    

By offering efficient two-ended operations, deques are a versatile and powerful data structure suitable for many real-world scenarios.
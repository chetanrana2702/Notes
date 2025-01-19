## Simple Queue

- A **simple queue** is a data structure that operates on the **First In, First Out (FIFO)** principle, meaning that the first element added to the queue will be the first one to be removed. 
- It is a linear data structure used to temporarily store data in the order it arrives.

### Key Operations

1.  **Enqueue**: Add an element to the back of the queue.
    
2.  **Dequeue**: Remove an element from the front of the queue.
    
3.  **Peek/Front**: Retrieve the element at the front without removing it.
    
4.  **IsEmpty**: Check if the queue is empty.
    
5.  **Size**: Get the number of elements in the queue.
    

### Characteristics

*   **FIFO Order**: Elements are served in the same order they were added.
    
*   **Single-ended access**: Operations like enqueue and dequeue are performed at opposite ends (enqueue at the rear and dequeue from the front).
    

### Implementation

A simple queue can be implemented using:

1.  **Arrays**: Using a fixed-size array, but it may require resizing when the queue exceeds capacity.
    
2.  **Linked List**: A dynamic approach, where each node contains the data and a reference to the next node.

### Python Example

Here’s an implementation of a simple queue using a list in Python:

```python
class SimpleQueue:
    def __init__(self):
        self.queue = []

    def enqueue(self, item):
        self.queue.append(item)

    def dequeue(self):
        if not self.is_empty():
            return self.queue.pop(0)
        raise IndexError("Dequeue from an empty queue")

    def peek(self):
        if not self.is_empty():
            return self.queue[0]
        raise IndexError("Peek from an empty queue")

    def is_empty(self):
        return len(self.queue) == 0

    def size(self):
        return len(self.queue)

# Example Usage
queue = SimpleQueue()
queue.enqueue(10)
queue.enqueue(20)
print(queue.dequeue())  # Output: 10
print(queue.peek())     # Output: 20
print(queue.is_empty()) # Output: False

```

### Implementation using linked list 
- Here’s an implementation of a simple queue using a linked list. 
- A linked list is a dynamic data structure that can grow or shrink as needed, making it an efficient choice for a queue.

```python
class Node:
    """A node in the linked list."""
    def __init__(self, data):
        self.data = data
        self.next = None

class LinkedListQueue:
    """A queue implemented using a linked list."""
    def __init__(self):
        self.front = None  # Points to the front of the queue
        self.rear = None   # Points to the rear of the queue
        self._size = 0     # Tracks the number of elements

    def enqueue(self, item):
        """Add an item to the rear of the queue."""
        new_node = Node(item)
        if self.is_empty():
            self.front = self.rear = new_node
        else:
            self.rear.next = new_node
            self.rear = new_node
        self._size += 1

    def dequeue(self):
        """Remove and return the item from the front of the queue."""
        if self.is_empty():
            raise IndexError("Dequeue from an empty queue")
        result = self.front.data
        self.front = self.front.next
        if self.front is None:  # If the queue becomes empty
            self.rear = None
        self._size -= 1
        return result

    def peek(self):
        """Return the front item without removing it."""
        if self.is_empty():
            raise IndexError("Peek from an empty queue")
        return self.front.data

    def is_empty(self):
        """Check if the queue is empty."""
        return self.front is None

    def size(self):
        """Get the number of elements in the queue."""
        return self._size

# Example Usage
queue = LinkedListQueue()
queue.enqueue(10)
queue.enqueue(20)
queue.enqueue(30)

print(queue.dequeue())  # Output: 10
print(queue.peek())     # Output: 20
print(queue.size())     # Output: 2
print(queue.is_empty()) # Output: False

```

### Explanation:

1.  **Node Class**:
    
    *   Represents a single node in the linked list.
        
    *   Each node contains data and a pointer (next) to the next node.
        
2.  **LinkedListQueue Class**:
    
    *   Uses front and rear pointers to track the start and end of the queue.
        
    *   Dynamically grows or shrinks as elements are added or removed.
        
3.  **Advantages**:
    
    *   No fixed size: It dynamically adjusts to the number of elements.
        
    *   No need to shift elements during dequeue operations as in array-based implementations.
        

This linked list implementation ensures efficient enqueue and dequeue operations with a time complexity of O(1).
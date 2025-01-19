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


## Some Common Problem Categories

### **1\. Sliding Window Problems**

Deques are highly efficient for maintaining the state of a sliding window. They allow us to process elements in constant time by adding and removing elements from the ends.

*   **Problem 1: Sliding Window Maximum**
    
    - **Description**: Find the maximum value in each sliding window of size k.
    - **Approach**: Use a deque to store indices of elements in the current window in decreasing order of their values. Remove indices that fall out of the window or whose corresponding values are less than the current element.
    
*   **Problem 2: Minimum Window Subsequence**
    
    - **Description**: Find the smallest window in a string S containing a subsequence T.
    

### **2\. BFS/DFS on Grids or Graphs**

Deque is often used to optimize BFS implementations.

*   **Problem 3: Shortest Path in Binary Matrix**
    
    - **Description**: Find the shortest path in a binary matrix from the top-left to the bottom-right corner.
    - **Approach**: Use a deque for BFS traversal to explore neighboring cells efficiently.
    
*   **Problem 4: Rotting Oranges**
    
    - **Description**: Determine the minimum time to rot all oranges in a grid.
    - **Approach**: Use a deque to simulate the spreading of rot layer by layer (multi-source BFS).
    

### **3\. Monotonic Queue Problems**

Monotonic deques are used to maintain elements in sorted order to efficiently find minimums or maximums.

*   **Problem 5: Jump Game VI**
    
    - **Description**: Given an array, find the maximum score you can achieve by jumping between indices with constraints.
    - **Approach**: Use a deque to store potential scores in decreasing order, ensuring efficient retrieval of the maximum score within a sliding window.
    
*   **Problem 6: Longest Subarray of 1's After Deleting One Element**
    
    - **Description**: Find the longest subarray containing only 1s after deleting at most one element.  
    - **Approach**: Use a deque to maintain the indices of zeros in the current valid subarray.
    

### **4\. Two Pointers / Sliding Window Techniques**

Deques help manage ranges efficiently when processing substrings or subarrays.

*   **Problem 7: Maximum Number of Events That Can Be Attended**
    
    - **Description**: Attend the maximum number of non-overlapping events.
    - **Approach**: Use a deque to track events ending soonest while iterating over sorted start times.
    
*   **Problem 8: Shortest Subarray with Sum at Least K**
    
    - **Description**: Find the shortest subarray with a sum of at least k.
    - **Approach**: Use a deque to maintain a sliding window with a sum greater than or equal to k.
    

### **5\. Design Problems**

Deque is a natural fit for problems requiring custom data structures.

*   **Problem 9: Design Circular Deque**
    
    - **Description**: Implement a circular deque with efficient operations on both ends.
    - **Approach**: Directly implement deque operations like insertFront, insertLast, deleteFront, and deleteLast.
    
*   **Problem 10: Design Front Middle Back Queue**
    
    - **Description**: Design a queue that supports operations to add or remove elements from the front, back, or middle.
    - **Approach**: Use a deque to manage elements efficiently.
    

### **6\. String or Parentheses Manipulation**

Deques are used for balancing or tracking characters.

*   **Problem 11: Minimum Add to Make Parentheses Valid**
    
    - **Description**: Find the minimum number of parentheses additions to make a string valid.
    - **Approach**: Use a deque to simulate stack-like behavior.
    
*   **Problem 12: Check If a String Is Transformable With Substring Sort Operations**

    - **Description**: Check if one string can be transformed into another using substring sorting.
    - **Approach**: Use a deque to track indices of characters.
    

### **7\. Others**

*   **Problem 13: Maximum Number of Points with Cost**

    - **Description**: Compute the maximum number of points with given constraints.
    - **Approach**: Use a deque to optimize the transition between rows.
    
*   **Problem 14: Sum of Subarray Minimums**

    - **Description**: Calculate the sum of minimums of all subarrays.
    - **Approach**: Use a monotonic deque to find the contribution of each element.
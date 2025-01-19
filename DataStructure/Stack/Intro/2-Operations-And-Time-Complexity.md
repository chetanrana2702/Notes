### <b style="color:blue">Stack Operations</b>

A **Stack** is a linear data structure that follows the **Last In, First Out (LIFO)** principle, where the last element added to the stack is the first one to be removed. Here are the primary operations performed on a stack along with their time complexities:

### 1. <b style="color:darkorange">Push (Adding an element)</b>

* <b style="color:blue">Description:</b> Adds an element to the top of the stack.
    
*  <b style="color:blue">Time Complexity:</b> O(1) (constant time) because the operation involves only updating the top pointer and inserting the element.
    

### 2. <b style="color:darkorange">Pop (Removing an element)</b>

*  <b style="color:blue">Description:</b> Removes the top element from the stack.
    
*  <b style="color:blue">Time Complexity:</b> O(1) (constant time) because the operation involves only updating the top pointer and removing the element.
    

### 3. <b style="color:darkorange">Peek/Top (Accessing the top element)</b>

*  <b style="color:blue">Description:</b> Retrieves the top element of the stack without removing it.
    
*  <b style="color:blue">Time Complexity:</b> O(1) (constant time) because it involves directly accessing the top pointer.
    

### 4. <b style="color:darkorange">IsEmpty (Checking if the stack is empty)</b>

* <b style="color:blue">Description:</b> Checks whether the stack contains any elements.
    
* <b style="color:blue">Time Complexity:</b> O(1) (constant time) because it only involves checking a pointer or a size variable.
    

### 5. <b style="color:darkorange">Size (Getting the number of elements in the stack)</b>

* <b style="color:blue">Description:</b> Returns the total number of elements in the stack.
    
* <b style="color:blue">Time Complexity:</b>
    
    * O(1) if the size is maintained as a separate variable.
        
    * O(n) if the size is calculated dynamically by traversing the stack.

### <b style="color:darkorange">Summary of Time Complexities:</b>

| Operation  | Time Complexity       |
|------------|-----------------------|
| Push       | O(1)                  |
| Pop        | O(1)                  |
| Peek/Top   | O(1)                  |
| IsEmpty    | O(1)                  |
| Size       | O(1) or O(n)*         |

(*The complexity for `Size` depends on the implementation of the stack.*)

<i>(Stacks can be implemented using arrays or linked lists, and the time complexities remain the same for most operations, provided there is sufficient capacity or proper handling of memory in dynamic cases.)</i>


Dynamic cases in the context of a stack occur when the underlying data structure needs to adjust dynamically based on its size or memory requirements. These cases typically arise when implementing a stack with a **dynamic array** or similar structure that adjusts its capacity as elements are added or removed.

### 1. <b style="color:darkorange">Dynamic Array Resizing</b>

*  If a stack is implemented using a dynamic array (e.g., in **C++** with std::vector or in **Java** with ArrayList), the array might need to grow when more elements are pushed than its current capacity.
    
*  <b style="color:blue">Growth Strategy:</b> Most implementations double the array size when the current capacity is exceeded. This involves:
    
    *  Allocating a new array with larger capacity.
        
    *  Copying all the existing elements to the new array.
        
    *  Adding the new element to the resized array.
        
*  <b style="color:blue">Amortized Time Complexity for Push:</b>
    
    *  <b style="color:deeppink">Typical Case:</b> O(1), when there's enough capacity.
        
    *  <b style="color:deeppink">Resize Case:</b> O(n), where n is the number of elements being copied during resizing.
        
    * <b style="color:deeppink">Amortized Overall Complexity:</b> Still O(1) on average, because resizing happens infrequently.
        

### 2. <b style="color:darkorange">Dynamic Deallocation (Optional)</b>

*  Some implementations shrink the array when many elements are popped, and the usage drops significantly below the current capacity (e.g., if size is less than 1/4 of the capacity).
    
*  This can reduce memory usage but may introduce additional O(n) operations during shrinking.
    

### 3. <b style="color:darkorange">Dynamic Linked List</b>

*  When using a linked list to implement a stack, nodes are dynamically allocated and deallocated for each push or pop.
    
*  <b style="color:deeppink">Dynamic Memory Allocation:</b>
    
    *  Allocating memory for a new node (during push).
        
    *  Deallocating memory for the removed node (during pop).
        
*  <b style="color:deeppink">Time Complexity:</b>
    
    *  O(1) for both push and pop, but the actual runtime might be slower than array-based stacks due to overhead associated with dynamic memory allocation.
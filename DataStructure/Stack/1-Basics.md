### <b style="color:blue">Stack Basics</b>

A **Stack** is a **linear data structure** that follows the **Last In, First Out (LIFO)** principle. This means the last element added (pushed) to the stack is the first one to be removed (popped). It is like a stack of plates where you can only add or remove the top plate.

### <b style="color:darkorange">Characteristics of a Stack:</b>

1. <b style="color:deeppink">LIFO Order:</b> The last element inserted is the first to be removed.

2. <b style="color:deeppink">Operations:</b>
    - <b style="color:blue">Push:</b> Add an element to the top of the stack.
    - <b style="color:blue">Pop:</b> Remove the top element of the stack.
    - <b style="color:blue">Peek/Top:</b> Retrieve the top element without removing it.
    - <b style="color:blue">IsEmpty:</b> Check if the stack is empty.
    - <b style="color:blue">Size:</b> Determine the number of elements in the stack.


### <b style="color:darkorange">Representation:</b>

- Stacks can be implemented using:
    - <b style="color:deeppink">Arrays:</b> Fixed-size stack, efficient for accessing elements by index.
    - <b style="color:deeppink">Linked Lists:</b> Dynamic-size stack, grows and shrinks as needed.


### <b style="color:darkorange">Applications of Stacks:</b>

1. <b style="color:deeppink">Expression Evaluation:</b>Converting and evaluating infix, postfix, and prefix expressions.

2. <b style="color:deeppink">Backtracking:</b> E.g., navigating backward in browsers or solving puzzles like mazes.

3. <b style="color:deeppink">Function Call Management:</b> The call stack maintains function calls in programming.

4. <b style="color:deeppink">Undo/Redo Operations:</b> Used in text editors or applications.

5. <b style="color:deeppink">Parenthesis Matching:</b> Checking balanced parentheses in expressions.

6. <b style="color:deeppink">Reversing Data:</b> Strings, numbers, or other sequences.

### <b style="color:darkorange">Example of a Stack:</b>
<b style="color:deeppink">Pushing elements:</b>
- Initially: Empty stack [].
- Push 10: Stack becomes [10].
- Push 20: Stack becomes [10, 20].
- Push 30: Stack becomes [10, 20, 30].

<b style="color:deeppink">Popping elements:</b>
- Pop: Stack becomes [10, 20] and the removed element is 30.

---
Here’s the time complexity of operations on a stack:

1. <b style="color:blue">Inserting an Element (Push)</b>
    
    - Time Complexity: O(1)
    
    - Explanation: Adding an element to the top of the stack involves simply placing the element at the next available position. No traversal is needed.

2. <b style="color:blue">Accessing an Element (Peek or Top)</b>
    - Time Complexity: O(1)
    
    - Explanation: Retrieving the top element requires no traversal, as the top is directly accessible.

3. <b style="color:blue">Removing an Element (Pop)</b>
    
    - Time Complexity: O(1)
    
    - Explanation: Removing the top element only involves adjusting the pointer to the next element or decreasing the index.

>NOTE:

>The time complexity of all these operations assumes a stack is implemented using a dynamic array or linked list.

> If you require random access (accessing elements other than the top), a stack does not support it efficiently, and this would take O(n), where n is the size of the stack. This is because stacks are designed to work with the LIFO principle, and accessing elements not at the top requires traversing from the beginning.



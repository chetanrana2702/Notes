### <b style="color:blue">Dynamic Arrays</b>

- Provides the ability to store elements and dynamically resize itself when necessary.
- Unlike static arrays, which have a fixed size defined at creation, dynamic arrays can grow or shrink as elements are added or removed.
- They are widely used in programming because they offer a balance between efficiency and flexibility.


### <b style="color:darkorange">Key Features Of a Dynamic Array</b>

- <b style="color:blue">Resizable:</b> The size of the dynamic array automatically adjusts as elements are added or removed.
- <b style="color:blue">Indexing:</b> Supports efficient random access using an index, similar to a static array.
- <b style="color:blue"> Amortized Cost:</b> The cost of adding elements is typically low(Constant Time), occasional resizing might take longer but with occasional expensive resizing operations spread out over time.

### <b style="color:darkorange">Time Complexity of Basic Operations</b>

- <b style="color:blue">Access:</b> <i>O(1)</i>
- <b style="color:blue">Search:</b> <i>O(1)</i> for exact matches, <i>O(n)</i> linearly for others
- <b style="color:blue">Insertion:</b> <i>O(1)</i> amortized, <i>O(n)</i> during resizing
- <b style="color:blue">Deletion:</b> <i>O(1)</i> amortized, <i>O(n)</i> during shifting or resizing
- <b style="color:blue">Append:</b> <i>O(1)</i> amortized, <i>O(n)</i> during resizing

```
The Amortized time complexity for appending elements is 𝑂(1) because resizing happens infrequently.
```


### <b style="color:darkorange">Internal Mechanics</b>

Dynamic arrays work by:

- Allocating an initial amount of memory.
- Using that memory to store elements.
- When the allocated memory is full:
    - Allocate a larger block of memory.
    - Copy existing elements to the new block.
    - Free the old memory.

### <b style="color:darkorange">Resizing Strategy</b>
Dynamic arrays often use a strategy to minimize the cost of resizing. A common approach is to double the capacity each time the array is full. This ensures that resizing happens less frequently.

For example:

- Start with a capacity of 4.
- Add 4 elements → Capacity is full.
- Double the capacity to 8.
- Copy the 4 existing elements to the new block.

### <b style="color:darkorange">Shrinkage</b>
Some implementations also shrink the array if a significant number of elements are removed. This reduces memory usage but may involve additional computational overhead.

### <b style="color:darkorange">Use Cases</b>
Dynamic arrays are ideal for:

- Storing collections of data with unknown or variable size.
- Applications requiring frequent append or removal of elements.
- Dynamic data structures like stacks, queues, and deques.


### <b style="color:darkorange">Implementation</b>
Dynamic arrays are implemented differently in various programming languages:

#### <b style="color:blue">C++: std::vector</b>
- Automatically resizes as elements are added.
- Provides methods like push_back(), pop_back(), resize().

#### <b style="color:blue">Java: ArrayList</b>
- Backed by an array that grows as needed.
- Methods like add(), remove(), and size() handle operations.

#### <b style="color:blue">Python: List</b>
- Python’s list is dynamic and handles resizing internally.
- Operations like append(), extend(), and pop() manage elements.

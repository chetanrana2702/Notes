<b style="color:blue">Dynamic arrays</b>

- Provides the ability to store elements and dynamically resize itself when necessary.

- Unlike static arrays, which have a fixed size defined at creation, dynamic arrays can grow or shrink as elements are added or removed.

- They are widely used in programming because they offer a balance between efficiency and flexibility.


### Key Features Of a Dynamic Array

- <b style="color:blue">Resizable:</b> The size of the dynamic array automatically adjusts as elements are added or removed.
- <b style="color:blue">Indexing:</b> Supports efficient random access using an index, similar to a static array.
- <b style="color:blue"> Amortized Cost:</b> The cost of adding elements is typically low(Constant Time), occasional resizing might take longer but with occasional expensive resizing operations spread out over time.

### Time Complexity of Basic Operations

- <b style="color:blue">Access:</b> <i>O(1)</i>
- <b style="color:blue">Search:</b> <i>O(1)</i> for exact matches, <i>O(n)</i> linearly for others
- <b style="color:blue">Insertion:</b> <i>O(1)</i> amortized, <i>O(n)</i> during resizing
- <b style="color:blue">Deletion:</b> <i>O(1)</i> amortized, <i>O(n)</i> during shifting or resizing
- <b style="color:blue">Append:</b> <i>O(1)</i> amortized, <i>O(n)</i> during resizing

```
The Amortized time complexity for appending elements is 𝑂(1) because resizing happens infrequently.
```


### Internal Mechanics

Dynamic arrays work by:

- Allocating an initial amount of memory.
- Using that memory to store elements.
- When the allocated memory is full:
    - Allocate a larger block of memory.
    - Copy existing elements to the new block.
    - Free the old memory.

### Resizing Strategy
Dynamic arrays often use a strategy to minimize the cost of resizing. A common approach is to double the capacity each time the array is full. This ensures that resizing happens less frequently.

For example:

- Start with a capacity of 4.
- Add 4 elements → Capacity is full.
- Double the capacity to 8.
- Copy the 4 existing elements to the new block.

### Shrinkage
Some implementations also shrink the array if a significant number of elements are removed. This reduces memory usage but may involve additional computational overhead.

### Use Cases
Dynamic arrays are ideal for:

- Storing collections of data with unknown or variable size.
- Applications requiring frequent append or removal of elements.
- Dynamic data structures like stacks, queues, and deques.



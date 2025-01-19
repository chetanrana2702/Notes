# Circular Queue

A **Circular Queue** is a data structure that overcomes the limitations of a standard queue by utilizing a circular array. Unlike a regular queue where elements can only be added or removed in a linear order, a circular queue efficiently reuses the storage by connecting the end of the queue back to the beginning, forming a circular shape.

### Features of Circular Queue:

1.  **Fixed Size**: Like a regular queue, a circular queue has a fixed size, defined when the queue is created.
    
2.  **Circular Nature**: The last position in the queue wraps around to the first position when the queue is full and there is space available due to previous dequeue operations.
    
3.  **Efficient Space Utilization**: It avoids the "wastage of space" that occurs in a regular queue when the front of the queue moves forward after multiple dequeues.
    

### Representation:

A circular queue is represented using an array, with two pointers:

*   **Front**: Indicates the position of the first element.
    
*   **Rear**: Indicates the position of the last element.
    

### Key Operations in Circular Queue:

1.  **Enqueue (Insertion)**:
    
    *   Adds an element to the queue.
        
    *   Check if the queue is full.
        
    *   If not, increment the rear pointer (circularly) and insert the element.
        
2.  **Dequeue (Deletion)**:
    
    *   Removes an element from the queue.
        
    *   Check if the queue is empty.
        
    *   If not, increment the front pointer (circularly) to remove the element.
        
3.  **Peek/Front**:
    
    *   Returns the element at the front of the queue without removing it.
        
4.  **IsFull**:
    
    *   Checks if the queue is full. This occurs when:
    ```
    (Rear + 1) % Size = Front
    ```
        
5.  **IsEmpty**:
    
    *   Checks if the queue is empty. This occurs when:
    ```
    Front = −1
    ```
        

### Algorithmic Steps:

#### **Enqueue Operation**

1.  Check if the queue is full:
    ```
    (Rear+1)%Size=Front
    ```
    If true, print an overflow error.
    
2.  If the queue is empty (Front = -1), set Front and Rear to 0.
    
3.  Else, update Rear using:
    ```
    Rear=(Rear+1)%Size
    ```
    
4.  Add the element to the queue at the new Rear position.
    

#### **Dequeue Operation**

1.  Check if the queue is empty:
    ```
    Front = −1
    ```
    If true, print an underflow error.
    
2.  Retrieve the element at Front.
    
3.  If Front equals Rear (only one element left), reset Front and Rear to -1 (empty queue).
    
4.  Else, update Front using:
    ```
    Front = (Front + 1) % Size
    ```

### Example:

Consider a circular queue of size 5.

1.  **Initial State**: Empty queue.
    ```
    Queue: [_, _, _, _, _]
    Front = -1, Rear = -1
    ```

2.  **Enqueue 10, 20, 30**:
    ```
    Queue: [10, 20, 30, _, _]
    Front = 0, Rear = 2
    ```

3.  **Dequeue an element** (10 is removed):
    ```
    Queue: [_, 20, 30, _, _]
    Front = 1, Rear = 2
    ```

4.  **Enqueue 40, 50:**
    ```
    Queue: [_, 20, 30, 40, 50]
    Front = 1, Rear = 4
    ```

5.  **Enqueue 60** (wrap-around):
    ```
    Queue: [60, 20, 30, 40, 50]
    Front = 1, Rear = 0
    ```

6.  **Dequeue two elements** (20 and 30 are removed):
    ```
    Queue: [60, _, _, 40, 50]
    Front = 3, Rear = 0
    ```

### Advantages:

1.  Optimizes memory by reusing unused space.
    
2.  Avoids the need to shift elements after a dequeue operation.
    
3.  Maintains constant time complexity O(1)_O_(1) for both enqueue and dequeue operations.
    

### Disadvantages:

1.  Requires careful handling of circular conditions.
    
2.  Fixed size may still lead to overflow if not managed properly.
    

### Applications:

*   CPU scheduling (round-robin scheduling).
    
*   Buffer management in network routers.
    
*   Handling real-time data streams, like audio or video buffering.


### Using an Array

#### Python Implementation (Array)

```python
class CircularQueueArray:
    def __init__(self, size):
        self.size = size
        self.queue = [None] * size
        self.front = -1
        self.rear = -1

    def enqueue(self, value):
        if (self.rear + 1) % self.size == self.front:
            print("Queue is full")
            return
        if self.front == -1:  # First insertion
            self.front = 0
        self.rear = (self.rear + 1) % self.size
        self.queue[self.rear] = value
        print(f"Enqueued: {value}")

    def dequeue(self):
        if self.front == -1:
            print("Queue is empty")
            return None
        dequeued_value = self.queue[self.front]
        if self.front == self.rear:  # Queue becomes empty
            self.front = self.rear = -1
        else:
            self.front = (self.front + 1) % self.size
        print(f"Dequeued: {dequeued_value}")
        return dequeued_value

    def display(self):
        if self.front == -1:
            print("Queue is empty")
            return
        i = self.front
        print("Queue elements:", end=" ")
        while True:
            print(self.queue[i], end=" ")
            if i == self.rear:
                break
            i = (i + 1) % self.size
        print()

# Example usage
cq = CircularQueueArray(5)
cq.enqueue(10)
cq.enqueue(20)
cq.enqueue(30)
cq.dequeue()
cq.enqueue(40)
cq.enqueue(50)
cq.enqueue(60)
cq.display()

```

#### Ruby Implementation (Array)
```ruby
class CircularQueueArray
  def initialize(size)
    @size = size
    @queue = Array.new(size)
    @front = -1
    @rear = -1
  end

  def enqueue(value)
    if (@rear + 1) % @size == @front
      puts "Queue is full"
      return
    end
    if @front == -1  # First insertion
      @front = 0
    end
    @rear = (@rear + 1) % @size
    @queue[@rear] = value
    puts "Enqueued: #{value}"
  end

  def dequeue
    if @front == -1
      puts "Queue is empty"
      return nil
    end
    dequeued_value = @queue[@front]
    if @front == @rear  # Queue becomes empty
      @front = @rear = -1
    else
      @front = (@front + 1) % @size
    end
    puts "Dequeued: #{dequeued_value}"
    dequeued_value
  end

  def display
    if @front == -1
      puts "Queue is empty"
      return
    end
    print "Queue elements: "
    i = @front
    loop do
      print "#{@queue[i]} "
      break if i == @rear
      i = (i + 1) % @size
    end
    puts
  end
end

# Example usage
cq = CircularQueueArray.new(5)
cq.enqueue(10)
cq.enqueue(20)
cq.enqueue(30)
cq.dequeue
cq.enqueue(40)
cq.enqueue(50)
cq.enqueue(60)
cq.display

```

## Using a Linked List

#### Python Implementation (Linked List)

```python
class Node:
    def __init__(self, data):
        self.data = data
        self.next = None

class CircularQueueLinkedList:
    def __init__(self):
        self.front = None
        self.rear = None

    def enqueue(self, value):
        new_node = Node(value)
        if self.front is None:  # First insertion
            self.front = self.rear = new_node
            self.rear.next = self.front  # Circular link
        else:
            self.rear.next = new_node
            self.rear = new_node
            self.rear.next = self.front  # Maintain circular link
        print(f"Enqueued: {value}")

    def dequeue(self):
        if self.front is None:
            print("Queue is empty")
            return None
        dequeued_value = self.front.data
        if self.front == self.rear:  # Single element
            self.front = self.rear = None
        else:
            self.front = self.front.next
            self.rear.next = self.front  # Maintain circular link
        print(f"Dequeued: {dequeued_value}")
        return dequeued_value

    def display(self):
        if self.front is None:
            print("Queue is empty")
            return
        current = self.front
        print("Queue elements:", end=" ")
        while True:
            print(current.data, end=" ")
            current = current.next
            if current == self.front:
                break
        print()

# Example usage
cq = CircularQueueLinkedList()
cq.enqueue(10)
cq.enqueue(20)
cq.enqueue(30)
cq.dequeue()
cq.enqueue(40)
cq.enqueue(50)
cq.display()

```

#### Ruby Implementation (Linked List)

```ruby
class Node
  attr_accessor :data, :next

  def initialize(data)
    @data = data
    @next = nil
  end
end

class CircularQueueLinkedList
  def initialize
    @front = nil
    @rear = nil
  end

  def enqueue(value)
    new_node = Node.new(value)
    if @front.nil?  # First insertion
      @front = @rear = new_node
      @rear.next = @front  # Circular link
    else
      @rear.next = new_node
      @rear = new_node
      @rear.next = @front  # Maintain circular link
    end
    puts "Enqueued: #{value}"
  end

  def dequeue
    if @front.nil?
      puts "Queue is empty"
      return nil
    end
    dequeued_value = @front.data
    if @front == @rear  # Single element
      @front = @rear = nil
    else
      @front = @front.next
      @rear.next = @front  # Maintain circular link
    end
    puts "Dequeued: #{dequeued_value}"
    dequeued_value
  end

  def display
    if @front.nil?
      puts "Queue is empty"
      return
    end
    current = @front
    print "Queue elements: "
    loop do
      print "#{current.data} "
      current = current.next
      break if current == @front
    end
    puts
  end
end

# Example usage
cq = CircularQueueLinkedList.new
cq.enqueue(10)
cq.enqueue(20)
cq.enqueue(30)
cq.dequeue
cq.enqueue(40)
cq.enqueue(50)
cq.display

```
Both implementations in Python and Ruby showcase the array-based and linked-list-based circular queues.
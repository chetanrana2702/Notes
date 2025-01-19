Main Operations in Queue

### 1. **Enqueue**:

The operation to add an element to the rear of the queue.

### 2. **Dequeue**:

The operation to remove an element from the front of the queue.

### 3. **Peek/Front**:

Retrieve the element at the front of the queue without removing it.

### 4. **Is Empty**:

Check if the queue is empty.

### Python Implementation

- Using a list to simulate a queue:

```python
class Queue:
    def __init__(self):
        self.queue = []

    # Enqueue operation
    def enqueue(self, item):
        self.queue.append(item)
        print(f"Enqueued: {item}")

    # Dequeue operation
    def dequeue(self):
        if not self.is_empty():
            item = self.queue.pop(0)
            print(f"Dequeued: {item}")
            return item
        else:
            print("Queue is empty!")
            return None

    # Peek operation
    def peek(self):
        if not self.is_empty():
            return self.queue[0]
        else:
            print("Queue is empty!")
            return None

    # Check if queue is empty
    def is_empty(self):
        return len(self.queue) == 0

    # Display the queue
    def display(self):
        print(f"Queue: {self.queue}")


# Example Usage
q = Queue()
q.enqueue(10)
q.enqueue(20)
q.enqueue(30)
q.display()
q.dequeue()
q.peek()
q.display()

```

### Ruby Implementation
- Using a class with an array:

```ruby
class Queue
  def initialize
    @queue = []
  end

  # Enqueue operation
  def enqueue(item)
    @queue.push(item)
    puts "Enqueued: #{item}"
  end

  # Dequeue operation
  def dequeue
    if !is_empty?
      item = @queue.shift
      puts "Dequeued: #{item}"
      return item
    else
      puts "Queue is empty!"
      return nil
    end
  end

  # Peek operation
  def peek
    if !is_empty?
      return @queue.first
    else
      puts "Queue is empty!"
      return nil
    end
  end

  # Check if queue is empty
  def is_empty?
    @queue.empty?
  end

  # Display the queue
  def display
    puts "Queue: #{@queue.inspect}"
  end
end

# Example Usage
q = Queue.new
q.enqueue(10)
q.enqueue(20)
q.enqueue(30)
q.display
q.dequeue
puts "Front: #{q.peek}"
q.display

```

### Key Points in Both Implementations:

1.  **Enqueue**:
    
    *   Python: append()
        
    *   Ruby: push
        
2.  **Dequeue**:
    
    *   Python: pop(0)
        
    *   Ruby: shift
        
3.  Both languages provide a dynamic array, making it easy to simulate a queue without worrying about resizing.
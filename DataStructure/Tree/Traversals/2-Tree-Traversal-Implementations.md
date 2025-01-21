## Tree Traversal Implementation

### Python Code:
**Recursive Approach:**
```python
class Node:
    def __init__(self, value):
        self.value = value
        self.left = None
        self.right = None

# In-order Traversal (Left, Root, Right)
def inorder_recursive(root):
    if root:
        inorder_recursive(root.left)
        print(root.value, end=' ')
        inorder_recursive(root.right)

# Pre-order Traversal (Root, Left, Right)
def preorder_recursive(root):
    if root:
        print(root.value, end=' ')
        preorder_recursive(root.left)
        preorder_recursive(root.right)

# Post-order Traversal (Left, Right, Root)
def postorder_recursive(root):
    if root:
        postorder_recursive(root.left)
        postorder_recursive(root.right)
        print(root.value, end=' ')

# Example Tree:
root = Node(1)
root.left = Node(2)
root.right = Node(3)
root.left.left = Node(4)
root.left.right = Node(5)

print("In-order (Recursive):")
inorder_recursive(root)

print("\nPre-order (Recursive):")
preorder_recursive(root)

print("\nPost-order (Recursive):")
postorder_recursive(root)

```

**Iterative Approach:**

```python
# Iterative In-order Traversal using Stack
def inorder_iterative(root):
    stack = []
    current = root
    while current or stack:
        while current:
            stack.append(current)
            current = current.left
        current = stack.pop()
        print(current.value, end=' ')
        current = current.right

# Iterative Pre-order Traversal using Stack
def preorder_iterative(root):
    if not root:
        return
    stack = [root]
    while stack:
        node = stack.pop()
        print(node.value, end=' ')
        if node.right:
            stack.append(node.right)
        if node.left:
            stack.append(node.left)

# Iterative Post-order Traversal using Two Stacks
def postorder_iterative(root):
    if not root:
        return
    stack1 = [root]
    stack2 = []
    while stack1:
        node = stack1.pop()
        stack2.append(node)
        if node.left:
            stack1.append(node.left)
        if node.right:
            stack1.append(node.right)
    while stack2:
        print(stack2.pop().value, end=' ')

print("\nIn-order (Iterative):")
inorder_iterative(root)

print("\nPre-order (Iterative):")
preorder_iterative(root)

print("\nPost-order (Iterative):")
postorder_iterative(root)

```

## Ruby Code:

**Recursive Approach:**
```ruby
class Node
  attr_accessor :value, :left, :right
  def initialize(value)
    @value = value
    @left = nil
    @right = nil
  end
end

# In-order Traversal (Left, Root, Right)
def inorder_recursive(root)
  return if root.nil?
  inorder_recursive(root.left)
  print "#{root.value} "
  inorder_recursive(root.right)
end

# Pre-order Traversal (Root, Left, Right)
def preorder_recursive(root)
  return if root.nil?
  print "#{root.value} "
  preorder_recursive(root.left)
  preorder_recursive(root.right)
end

# Post-order Traversal (Left, Right, Root)
def postorder_recursive(root)
  return if root.nil?
  postorder_recursive(root.left)
  postorder_recursive(root.right)
  print "#{root.value} "
end

# Example Tree:
root = Node.new(1)
root.left = Node.new(2)
root.right = Node.new(3)
root.left.left = Node.new(4)
root.left.right = Node.new(5)

puts "In-order (Recursive):"
inorder_recursive(root)

puts "\nPre-order (Recursive):"
preorder_recursive(root)

puts "\nPost-order (Recursive):"
postorder_recursive(root)

```

**Iterative Approach:**
```ruby
# Iterative In-order Traversal using Stack
def inorder_iterative(root)
  stack = []
  current = root
  while !stack.empty? || current
    while current
      stack.push(current)
      current = current.left
    end
    current = stack.pop
    print "#{current.value} "
    current = current.right
  end
end

# Iterative Pre-order Traversal using Stack
def preorder_iterative(root)
  return if root.nil?
  stack = [root]
  while !stack.empty?
    node = stack.pop
    print "#{node.value} "
    stack.push(node.right) if node.right
    stack.push(node.left) if node.left
  end
end

# Iterative Post-order Traversal using Two Stacks
def postorder_iterative(root)
  return if root.nil?
  stack1 = [root]
  stack2 = []
  while !stack1.empty?
    node = stack1.pop
    stack2.push(node)
    stack1.push(node.left) if node.left
    stack1.push(node.right) if node.right
  end
  while !stack2.empty?
    print "#{stack2.pop.value} "
  end
end

puts "\nIn-order (Iterative):"
inorder_iterative(root)

puts "\nPre-order (Iterative):"
preorder_iterative(root)

puts "\nPost-order (Iterative):"
postorder_iterative(root)

```

### Explanation:

*   **Recursive Methods**: Simple and easy-to-understand functions that call themselves for left and right subtrees. They are easy to implement but can suffer from stack overflow for deep trees.
    
*   **Iterative Methods**: These use explicit stacks to simulate the recursion and avoid the call stack limits. They are more complex but useful for large trees.
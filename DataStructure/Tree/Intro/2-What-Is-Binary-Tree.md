## What is Binary Tree

- A binary tree is a data structure in which each node has at most two children, commonly referred to as the left and right children. 
- These children can be either another node or null (no child). 
- Binary trees are used extensively in computer science for tasks such as searching, sorting, and representing hierarchical data.


### **Properties of a Binary Tree:**

1.  **Root**: The topmost node of the tree, which doesn't have a parent.
    
2.  **Node**: An element in the tree that contains data and possibly references to other nodes (its children).
    
3.  **Edge**: A connection between two nodes.
    
4.  **Leaf Node**: A node that has no children.
    
5.  **Internal Node**: A node that has at least one child.
    
6.  **Height of the Tree**: The number of edges on the longest path from the root to a leaf.
    
7.  **Depth of a Node**: The number of edges from the root to the node.


### **Types of Binary Trees:**

1.  **Full Binary Tree**: Every node has either 0 or 2 children (no node has only one child).

    - Example
    ```
         1
       /   \
      2     3
     / \   / \
    4   5 6  7
    ```

2. **Complete Binary Tree:** A binary tree in which all levels, except possibly the last, are completely filled, and all nodes are as far left as possible.

    - Example
    ```
        1
      /   \
     2     3
    / \   / 
    4  5 6
    ```

3. **Perfect Binary Tree**: A binary tree where all internal nodes have exactly two children, and all leaf nodes are at the same level.


    - Example
    ```
         1
       /   \
      2     3
     / \   / \
    4   5 6   7
    ```

4. **Degenerate (or Pathological) Tree:** A tree where each parent node has only one child, essentially behaving like a linked list.

    - Example
    ```
      1
       \
        2
         \
          3
           \
            4
    ```

5. **Balanced Binary Tree:** A binary tree where the difference in heights of the left and right subtrees of any node is at most 1.

6. **Binary Search Tree (BST):** A binary tree where for each node, all nodes in its left subtree have lesser values, and all nodes in its right subtree have greater values.

    - Example
    ```
         10
       /    \
      5      15
     / \    /  \
    2   7  12  20
    ```

### **Basic Operations on Binary Trees:**

1.  **Insertion**: Adding a new node to the tree.
    
2.  **Deletion**: Removing a node from the tree.
    
3.  **Traversal**: Visiting each node in a specific order. There are three common types of tree traversals:
    
    *   **Preorder**: Visit the root node first, then traverse the left subtree, followed by the right subtree.
        
    *   **Inorder**: Traverse the left subtree first, then visit the root node, followed by the right subtree.
        
    *   **Postorder**: Traverse the left subtree first, then the right subtree, followed by visiting the root node.

**Example:** Consider this example of a binary tree:

```
       1
      / \
     2   3
    / \   \
   4   5   6

```
- **Inorder Traversal:** Left, Root, Right
    - Result: 4, 2, 5, 1, 3, 6

- **Preorder Traversal:** Root, Left, Right
    - Result: 1, 2, 4, 5, 3, 6

- **Postorder Traversal:** Left, Right, Root
    - Result: 4, 5, 2, 6, 3, 1

## Binary Tree Example in Code (Python):

```python
class Node:
    def __init__(self, key):
        self.left = None
        self.right = None
        self.value = key

# Example tree:
#        1
#       / \
#      2   3
#     / \   \
#    4   5   6

root = Node(1)
root.left = Node(2)
root.right = Node(3)
root.left.left = Node(4)
root.left.right = Node(5)
root.right.right = Node(6)

# Simple function for inorder traversal
def inorder(root):
    if root:
        inorder(root.left)
        print(root.value, end=" ")
        inorder(root.right)

# Traversing the tree
inorder(root)  # Output: 4 2 5 1 3 6

```

###  Ruby
```ruby
# Define the Node class
class Node
  attr_accessor :value, :left, :right

  def initialize(value)
    @value = value
    @left = nil
    @right = nil
  end
end

# Define the Binary Tree class
class BinaryTree
  def initialize
    @root = nil
  end

  # Method to insert a new value in the binary tree
  def insert(value)
    if @root.nil?
      @root = Node.new(value)
    else
      insert_recursive(@root, value)
    end
  end

  def insert_recursive(node, value)
    if value < node.value
      if node.left.nil?
        node.left = Node.new(value)
      else
        insert_recursive(node.left, value)
      end
    else
      if node.right.nil?
        node.right = Node.new(value)
      else
        insert_recursive(node.right, value)
      end
    end
  end

  # Method for inorder traversal
  def inorder
    inorder_recursive(@root)
    puts
  end

  def inorder_recursive(node)
    return if node.nil?
    
    inorder_recursive(node.left)
    print "#{node.value} "
    inorder_recursive(node.right)
  end

  # Method for preorder traversal
  def preorder
    preorder_recursive(@root)
    puts
  end

  def preorder_recursive(node)
    return if node.nil?

    print "#{node.value} "
    preorder_recursive(node.left)
    preorder_recursive(node.right)
  end

  # Method for postorder traversal
  def postorder
    postorder_recursive(@root)
    puts
  end

  def postorder_recursive(node)
    return if node.nil?

    postorder_recursive(node.left)
    postorder_recursive(node.right)
    print "#{node.value} "
  end
end

# Example usage:
binary_tree = BinaryTree.new
binary_tree.insert(10)
binary_tree.insert(5)
binary_tree.insert(15)
binary_tree.insert(2)
binary_tree.insert(7)
binary_tree.insert(12)
binary_tree.insert(20)

# Perform different tree traversals
puts "Inorder Traversal:"
binary_tree.inorder  # Output: 2 5 7 10 12 15 20

puts "Preorder Traversal:"
binary_tree.preorder # Output: 10 5 2 7 15 12 20

puts "Postorder Traversal:"
binary_tree.postorder # Output: 2 7 5 12 20 15 10

```

### Explanation:

*   **Node Class**: This class represents a single node in the tree. Each node stores a value and has two child references: left and right.
    
*   **BinaryTree Class**:
    
    *   insert method is used to insert values into the binary tree. It inserts them recursively using the insert\_recursive method.
        
    *   The inorder, preorder, and postorder methods are used to traverse the tree in respective orders.
        
    *   Each traversal method calls a corresponding recursive helper method to traverse the tree.



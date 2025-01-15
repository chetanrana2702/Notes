### <b style="color:blue">Matrix: A Two-Dimensional Array</b>

- A matrix is a two-dimensional array - imagine a table or grid where data is organized in rows and columns. 
- Each element can be accessed using two indices: one for the row and one for the column.
- It is commonly used in mathematics, computer science, and various programming scenarios to handle grid-like or tabular data.

### <b style="color:darkorange">Structure of a Matrix</b>
```python
# Example of a 3x3 matrix in Python
matrix = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]
```

### <b style="color:darkorange">Key Concepts</b>
1. <b style="color:blue">Dimensions</b>

    - Rows (m): Horizontal lines
    - Columns (n): Vertical lines
    - Size is described as m × n (rows × columns)

2. <b style="color:blue">Accessing Elements</b>
```python
# To access element in row 1, column 2
element = matrix[1][2]  # Gets value 6
```

3. <b style="color:blue">Common Matrix Types</b>

- Square Matrix: Equal number of rows and columns
- Identity Matrix: Square matrix with 1's on diagonal, 0's elsewhere
- Zero Matrix: All elements are 0
- Diagonal Matrix: Non-zero elements only on diagonal

### <b style="color:darkorange">Examples</b>

#### <b style="color:deeppink">Python Example (List of Lists):</b>
```python
# Creating a 2x3 matrix
matrix = [
    [1, 2, 3],
    [4, 5, 6]
]

# Accessing elements
print(matrix[0][1])  # Output: 2 (row 0, column 1)

# Iterating through the matrix
for row in matrix:
    for element in row:
        print(element, end=" ")
    print()

```

#### <b style="color:deeppink">Java Example (2D Array):</b>

```java
public class MatrixExample {
    public static void main(String[] args) {
        // Creating a 2x3 matrix
        int[][] matrix = {
            {1, 2, 3},
            {4, 5, 6}
        };

        // Accessing elements
        System.out.println(matrix[0][1]);  // Output: 2

        // Iterating through the matrix
        for (int i = 0; i < matrix.length; i++) {
            for (int j = 0; j < matrix[i].length; j++) {
                System.out.print(matrix[i][j] + " ");
            }
            System.out.println();
        }
    }
}
```

#### <b style="color:deeppink">Ruby Example (Array of Arrays):</b>

```ruby
# Creating a 2x3 matrix
matrix = [
  [1, 2, 3],
  [4, 5, 6]
]

# Accessing elements
puts matrix[0][1]  # Output: 2 (row 0, column 1)

# Iterating through the matrix
matrix.each do |row|
  row.each do |element|
    print "#{element} "
  end
  puts
end

```
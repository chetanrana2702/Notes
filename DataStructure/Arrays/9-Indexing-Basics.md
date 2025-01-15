### <b style="color:blue">How Indexing Work In Array</b>

Indexing in an array refers to accessing individual elements within the array using their respective positions, known as indices.

### <b style="color:darkorange">Indexing Basics</b>
- An array is a collection of elements stored in contiguous memory locations.
- Each element in the array can be accessed by its index, which is an integer representing its position in the array.

### <b style="color:darkorange">Zero-Based Indexing</b>
- Most programming languages (like C, C++, Java, Python) use zero-based indexing, where the first element has an index of 0, the second has an index of 1, and so on.
    - For example:
    ```python
    arr = [10, 20, 30, 40]
    print(arr[0])  # Output: 10
    print(arr[2])  # Output: 30
    ```

### <b style="color:darkorange">Accessing Elements</b>
- To access an element, you specify the array name followed by the index in square brackets:
```
element = array[index]
```

- Example: array[3] gives the 4th element (in zero-based indexing).

### <b style="color:darkorange">Negative Indexing (in some languages like Python)</b>
- Some languages support negative indexing, where:
    - -1 refers to the last element.
    - -2 refers to the second-to-last element.
    - Example:
    ```python
    arr = [10, 20, 30, 40]
    print(arr[-1])  # Output: 40
    print(arr[-2])  # Output: 30
    ```

### <b style="color:darkorange">Multidimensional Arrays</b>
- For arrays with multiple dimensions (e.g., 2D arrays), indexing involves specifying an index for each dimension:
    ```python
    arr = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
    print(arr[1][2])  # Output: 6
    ```
- arr[1] accesses the second row [4, 5, 6].
- arr[1][2] accesses the third element in the second row, which is 6.

### <b style="color:darkorange">Index Out of Bounds</b>
- If you try to access an index that is outside the array’s range, most languages will raise an error (e.g., IndexError in Python).
    ```python
    arr = [10, 20, 30]
    print(arr[5])  # IndexError: list index out of range
    ```

### <b style="color:darkorange">Time Complexity</b>
- Accessing an element in an array using its index is an O(1) operation since arrays provide direct access to memory locations.

!!! In summary, array indexing is the mechanism to directly retrieve or update elements stored in contiguous memory, using integer indices.
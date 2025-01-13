An <b style="color:blue">array</b> is a fundamental data structure used for storing a <b style="color:blue">sequence</b> of elements that can be accessed via an <b style="color:blue">index</b>.


### Key Characteristics
- <b style="color:blue">Homogeneity:</b> All elements are of the same data type.
- <b style="color:blue">Contiguous Memory:</b> Elements are stored in adjacent memory locations for quick access.
- <b style="color:blue">Fixed Size:</b> Arrays are generally static in size, although dynamic arrays exist in modern languages.
- <b style="color:blue">Indexing:</b> Usually zero-based, though some languages use one-based indexing.

### More Key Characteristics

- Each element can be accessed directly using its index <b style="color:chocolate">(position number, usually starting from 0)</b>
- Arrays have a fixed size in most programming languages <b style="color:chocolate">(though some languages like Python, Ruby and JavaScript use dynamic arrays)</b>


### Arrays are incredibly useful for many tasks like:

- Storing a collection of similar items <b style="color:chocolate">(like test scores or names)</b>
- Implementing other data structures <b style="color:chocolate">(like stacks and queues)</b>
- Processing data in a sequential manner
- Performing operations on multiple values efficiently


### Time Complexity of Basic Operations

- <b style="color:blue">Access:</b> <i style="color:chocolate">O(1)</i>
- <b style="color:blue">Search:</b> <i style="color:chocolate">O(1)</i>, <i style="color:chocolate">O(n)</i> assuming unsorted array
- <b style="color:blue">Insertion:</b> <i style="color:chocolate">O(1)</i> for the end, <i style="color:chocolate">O(n)</i> for beginning/middle
- <b style="color:blue">Deletion:</b> <i style="color:chocolate">O(1)</i> for the end, <i style="color:chocolate">O(n)</i> for beginning/middle
- <b style="color:blue">Append:</b> <i style="color:chocolate">O(1)</i> amortized, <i style="color:chocolate">O(n)</i> during resizing

### Code Example

```ruby
arr_with_fixed_size = Array.new(5)
puts arr_with_fixed_size # [nil, nil, nil, nil, nil]

arr_with_fixed_size_and_default_value = Array.new(5, 1)
puts arr_with_fixed_size_and_default_value # [1, 1, 1, 1, 1]

empty_arr_one_way = Array.new()
empty_arr_second_way = []
puts empty_arr

integer_arr = [1, 2, 3, 4, 5]
puts integer_arr

string_arr = ["red", "black", "blue", "white"]
puts string_arr

char_arr = ['a', 'c', 'd', 'e', 'd']
puts char_arr

bool_arr = [1, 1, 1, 0, 0, 0]
puts bool_arr

float_arr = [1.3, 5.1, 4.2]
puts float_arr
```

### Types Of An Arrays

- <b style="color:blue">Single Dimensional Array: </b> These are the most common type of arrays where elements are stored in a linear order.

    ```ruby
    single_dimensional_array = [1, 2, 3, 4, 5]    
    ```

- <b style="color:blue">Multi-Dimensional Array: </b> Arrays with more than one dimension, such as two-dimensional arrays <span style="color:darkred">(Matrices)</span>.

    ```ruby
    multi_dimensional_array = [
        [1, 2, 3],
        [4, 5, 6],
        [7, 8, 9]
    ]
    ```

### Advantages of Arrays

- <b style="color:blue">Efficient Access:</b> Accessing an element by its index is fast and has constant time complexity, O(1).
- <b style="color:blue">Memory Management:</b> Arrays have a fixed size, which makes memory management straightforward and predictable.

### More Operation

- <b style="color:blue">Passing Arrays To Methods: </b> Arrays can be passed to methods for processing, such as calculating the sum of its elements.

    ```ruby
    def sum(arr)
        sum = 0
        arr.each do |ele|
            sum += ele
        end
        puts "Sum of array values: #{sum}"
    end
    ```

- <b style="color:blue">Copying Arrays: </b> To copy the contents of one array to another, you must do it element by element.

    ```ruby
    list_one = []
    list_two = [1, 2, 3, 4, 5]

    list_two.each_with_index do |ele, index|
        list_one[index] = ele
    end
    puts list_one
    ```

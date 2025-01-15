### <b style="color:blue">Sparse Array</b>
- Sparse and dense arrays are concepts that relate to how data is stored and how efficiently memory is utilized, particularly when dealing with arrays in computing.
- A sparse array is an array where the majority of its elements have a default value, typically zero or null. 
    ```ruby
    Example of a Sparse Array Representation
    [0,0,3,0,0,5,0]
    ```

- Sparse arrays are useful when most of the elements are not significant and don't need to store actual data.
- Instead, sparse arrays focus on storing only the non-default values and their positions.

### <b style="color:darkorange">Characteristics:</b>
- Most elements are empty or have default values.
- Only non-default values and their indices are stored.
- They save memory by not storing default values explicitly.
- Commonly used in scenarios like matrices in scientific computations, where only a few elements have meaningful values (e.g., adjacency matrices, document-term matrices).

### <b style="color:darkorange">Benefits:</b>
- Reduced memory usage.
- Faster processing for certain operations since unnecessary values are not stored.

### <b style="color:darkorange">Drawbacks:</b>
- More complex representation.
- May involve additional computation for indexing.

### <b style="color:darkorange">Sparse Array Representation in Ruby</b>
```ruby
# Full array with many default values (e.g., 0)
full_array = [0, 0, 3, 0, 0, 5, 0]

# Sparse representation using a hash
sparse_array = {}

# Populate the sparse array
full_array.each_with_index do |value, index|
  sparse_array[index] = value unless value == 0
end

# Output the sparse array
puts "Sparse Representation: #{sparse_array}"
# Output: Sparse Representation: {2=>3, 5=>5}

# Fetch value at index 2
index = 2
value = sparse_array.fetch(index, 0) # Default to 0 if index is missing
puts "Value at index #{index}: #{value}"
# Value at index 2: 3
```


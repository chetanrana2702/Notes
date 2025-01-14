<b style="color:blue">Associative Array</b>

- It is a data structure that stores data in key-value pairs. 
- An associative array, also known as a map, dictionary, or hash table
- It allows us to associate a unique key with a specific value, making it easy to retrieve values by their corresponding keys.
- Its an abstract data type that enables key-based access to its elements and offers dynamic resizing and fast retrieval.


### Key Characteristics:
1. <b style="color:blue">Key-Value Pairs:</b> Each element in the array has a key and a value.

    - Key: A unique identifier used to access the associated value.
    - Value: The data associated with the key.

2. <b style="color:blue">Fast Lookup:</b> Associative arrays provide efficient retrieval of values based on keys, typically in constant time 𝑂(1), depending on the implementation.

3. <b style="color:blue">Unordered:</b> In most implementations, the elements in an associative array are not stored in any specific order.

4. <b style="color:blue">Dynamic Sizing:</b> Many implementations dynamically resize the array as new key-value pairs are added.

### Common Implementations
- <b style="color:blue">Hash Table:</b> Efficiency can degrade due to hash collisions.

    - Average Case O(1)
    - Worst Case O(n)

- <b style="color:blue">Self-Balancing Trees:</b> Consistent efficiency due to balanced structure.

    - Average Case O(log⁡ n)
    - Worst Case O(log n)

- <b style="color:blue">Unbalanced Trees:</b> Efficiency can vary, making them less reliable.

    - Average Case Variable
    - Worst Case between O(log n) and O(n)

- <b style="color:blue">Association Lists:</b> Simple structure, not ideal for large datasets.

    - Average and Worst Case O(n)

### Example

```ruby
    regular_array = ["apple", "banana", "cherry"]
    
    # using rocket sign (=>)
    associative_array = {
        "name" => "krishna",
        "age" => 30,
        "city" => "Bengaluru"
    }
    
    # Accessing values using keys as string
    puts associative_array["name"]
    puts associative_array["city"]
    puts associative_array["age"]

    # using (:) semicolon
    associative_array = {
        "name": "krishna",
        "age": 30,
        "city": "Bengaluru"
    }

    # Accessing values using keys as symbol
    puts associative_array[:name]
    puts associative_array[:city]
    puts associative_array[:age]

    # Add new key-value pair
    associative_array[:address] = "Whitefield"
    puts associative_array

    # Updating an existing value
    associative_array[:age] = 31

    # Iterating through the associative array (hash)
    associative_array.each do |key, value|
        puts "#{key}: #{value}"
    end

```
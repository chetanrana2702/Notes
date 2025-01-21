## Some Of the Collision Techniques

In a hash table, a **collision** occurs when two distinct keys hash to the same index in the hash table. Since hash tables are designed to quickly look up values associated with keys, handling collisions efficiently is crucial. Here are several common methods used to handle collisions:

### 1\. **Chaining**

*   **Concept**: Each table index (bucket) contains a linked list (or another collection) of all the keys that hash to that index. When multiple keys hash to the same index, they are simply added to the list or chain at that index.
    
*   **Pros**:
    
    *   Allows multiple keys to share the same index without needing to reorganize the table.
        
    *   The performance is relatively good when the table is large and the hash function is well-designed.
        
*   **Cons**:
    
    *   If many keys collide, the linked list could grow long, and the time complexity for lookup operations can degrade to O(n)O(n)O(n), where nnn is the number of elements in the list.
        
    *   Extra memory overhead for storing pointers in the linked list.

**Example:**
```
Hash Table: [ 0 -> {key1, key5}, 1 -> {key2}, 2 -> {key3, key6} ]
```

### 2\. **Linear Probing**

*   **Concept**: When a collision occurs at a given index, the algorithm checks the next consecutive index to find an empty slot. If that’s occupied, it continues checking the next one until an empty slot is found.
    
*   **Pros**:
    
    *   Simple to implement.
        
    *   Uses fewer memory resources than chaining, as it doesn’t require linked lists.
        
*   **Cons**:
    
    *   Can lead to **clustering**, where groups of keys are clustered together in consecutive slots, which degrades performance over time (i.e., increasing search time).
        
    *   Requires resizing and rehashing the table when it becomes too full.
        

**Example**:
```
Hash Table: [ 0 -> key1, 1 -> key2, 2 -> key3, 3 -> key4 ]
```

### 3\. **Quadratic Probing**

*   **Concept**: Similar to linear probing, but instead of checking the next consecutive index, it checks positions that are increasingly further apart using a quadratic formula. For example, if a collision occurs at index iii, the next slot checked would be at i+12i + 1^2i+12, then i+22i + 2^2i+22, and so on.
    
*   **Pros**:
    
    *   Reduces clustering compared to linear probing.
        
*   **Cons**:
    
    *   Still can lead to clustering (although less severe) and may require table resizing.
        
    *   If the hash table has a prime number of slots, it helps ensure that an empty slot will be found.
        

**Example**:
```
Hash Table: [ 0 -> key1, 1 -> key2, 2 -> key3, 4 -> key5 ]
```

### 4\. **Double Hashing**

*   **Concept**: This technique uses two hash functions to resolve collisions. The second hash function is used to determine the step size for probing. When a collision occurs, the index is adjusted by the value returned by the second hash function.
    
*   **Pros**:
    
    *   Reduces clustering more effectively than linear or quadratic probing.
        
    *   Can be very efficient if both hash functions are well-designed.
        
*   **Cons**:
    
    *   Requires careful selection of two hash functions to ensure that all table slots are eventually probed.
        
    *   Slightly more complex to implement than linear or quadratic probing.
        

**Example**:
```
* Hash function 1: h1(k) = k % 10
    
* Hash function 2: h2(k) = 1 + (k%7) (must ensure that h2(k)h2(k)h2(k) is non-zero)
```

If a collision occurs at index iii, the next slot to check would be i +h 2(k), then i + 2 × h2(k), etc.

**Example of table with collisions resolved via double hashing:**
```
Hash Table: [ 0 -> key1, 2 -> key2, 5 -> key3 ]
```

### 5\. **Rehashing**

*   **Concept**: Rehashing involves resizing the hash table when it reaches a certain load factor (ratio of filled slots to total slots) and rehashing all existing keys to new positions in a larger table.
    
*   **Pros**:
    
    *   Helps to maintain a low collision rate and ensures that the table remains efficient.
        
*   **Cons**:
    
    *   Rehashing can be an expensive operation because it requires recalculating the hash for all existing elements and moving them to new slots.

## Summary of Techniques:

| Collision Handling Method | Complexity (Average) | Memory Overhead                              | Performance Impact                             |
|--------------------------|----------------------|----------------------------------------------|------------------------------------------------|
| Chaining                 | O(1) (if balanced)   | High (linked lists)                         | Efficient for large tables                     |
| Linear Probing           | O(1)                 | Low                                         | Can suffer from clustering                     |
| Quadratic Probing       | O(1)                 | Low                                         | Reduces clustering compared to linear probing  |
| Double Hashing           | O(1)                 | Low                                         | Efficient with proper hash functions           |
| Rehashing                | O(n)                 | O(n) when resizing                          | Can significantly improve performance post-resizing |

> Note: 
> Choosing the appropriate collision resolution technique depends on factors like table size, hash function quality, and memory constraints.
## What is Hash Table

A **hash table** (also known as a **hash map**) is a data structure that allows for efficient data retrieval, insertion, and deletion. It works by using a **hash function** to compute an index (or "hash code") into an array of buckets or slots, from which the desired value can be found.

### Key Concepts:

1.  **Hash Function**: A function that takes an input (or "key") and returns an integer, which corresponds to an index in an array. The goal of the hash function is to distribute the keys uniformly across the array to minimize collisions.
    
2.  **Collisions**: Occur when two different keys generate the same hash code. Hash tables handle collisions using techniques like:
    
    *   **Chaining**: Each slot in the table holds a linked list of values that hash to the same index.
        
    *   **Open Addressing**: If a slot is occupied, the table searches for another available slot, often using methods like linear probing or quadratic probing.
        
3.  **Buckets/Slots**: The array used to store the values. The size of the array and the hash function determine how well the hash table performs.
    
4.  **Operations**:
    
    *   **Insertion**: The hash table uses the hash function to find an index, and the key-value pair is inserted at that index.
        
    *   **Search**: The key is hashed, and the value is found at the computed index or in the associated list if a collision occurred.
        
    *   **Deletion**: The key is hashed, and the value is removed from the appropriate index or chain.
        

### Benefits:

*   **Efficient Lookups**: On average, operations like insertion, deletion, and search can be done in constant time, O(1), if the hash function is good and collisions are minimal.
    
*   **Flexible**: Can store key-value pairs, where the key is unique and used to access its corresponding value.
    

### Drawbacks:

*   **Collisions**: If many keys hash to the same index, the performance degrades.
    
*   **Memory**: Hash tables can require more memory than simpler data structures like arrays or linked lists.
    

Hash tables are commonly used in applications like:

*   Caching systems
    
*   Implementing associative arrays or dictionaries
    
*   Databases for fast lookups
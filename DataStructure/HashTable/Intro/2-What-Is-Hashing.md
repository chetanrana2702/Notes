## What Is Hashing

- In the context of a **hash table**, **hashing** refers to the process of converting a given key (such as a string, number, or object) into an integer value, which is then used to index into an array (called a "hash table"). 
- This integer value is known as the **hash code** or **hash value**.

The key idea behind hashing is to map large, potentially complex keys to a fixed size array in a way that allows for efficient searching, inserting, and deleting operations. 

Here's how hashing works in a hash table:

1.  **Hash Function**: 
    - A function takes an input (the key) and computes a hash code, usually an integer, that represents the key. 
    - A good hash function distributes keys uniformly across the hash table, minimizing collisions (situations where different keys get mapped to the same hash value).
    
2.  **Indexing:** 
    - The hash code is typically mapped to an index in the array. 
    - If the hash table has an array of size n, the index is usually calculated as:
    ```shell
    index = hashcode mod  n
    ```
    This ensures the index falls within the bounds of the array.
    
3.  **Collision Handling**: 
    - Sometimes, different keys can produce the same hash code (a **collision**). There are several strategies for handling collisions, including:
    
        *    **Chaining**: Each array element is a linked list, and multiple keys that hash to the same index are stored in that list.
        
        *   **Open Addressing**: If a collision occurs, the algorithm searches for the next available slot in the table.
        

In summary, hashing in the context of a hash table is the process of converting a key into an index that determines where the key-value pair should be stored or retrieved in the hash table. 

This process enables fast lookups, insertions, and deletions, ideally in constant time, O(1).
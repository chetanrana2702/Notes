## What is the Time Complexity of HashTable/HashMap

The time complexity of operations in a **HashTable** or **HashMap** largely depends on how efficiently collisions are handled. Here are the time complexities for common operations:

1.  **Insert (Put)**:
    
    *   **Average case**: O(1) — This occurs when there are few or no collisions, and the key can be directly mapped to a bucket.
        
    *   **Worst case**: O(n) — This happens if many keys hash to the same bucket (due to collisions), leading to a long linked list or tree structure in that bucket, and the insertion could potentially take linear time in the worst case.
        
2.  **Search (Get)**:
    
    *   **Average case**: O(1) — In the absence of significant collisions, finding the value associated with a key is constant time.
        
    *   **Worst case**: O(n) — If there are many collisions, all keys might end up in a single bucket, requiring traversal of that bucket (e.g., linked list, tree), making it linear in the number of entries.
        
3.  **Delete (Remove)**:
    
    *   **Average case**: O(1) — As long as there are few collisions, removal is constant time.
        
    *   **Worst case**: O(n) — In the case of a high number of collisions in a bucket, removing an item could involve traversing a list or tree structure in the worst case.
        
4.  **Rehashing** (when the table needs to be resized):
    
    *   **Worst case**: O(n) — Rehashing happens when the load factor exceeds a certain threshold. This operation involves resizing the table and re-inserting all elements into the new table, which takes linear time.
        

### Factors Affecting Time Complexity:

*   **Load Factor**: The ratio of the number of elements to the size of the hash table. A higher load factor increases the chance of collisions, which can degrade performance.
    
*   **Collision Resolution**: Common techniques include **chaining** (using linked lists or trees) or **open addressing** (e.g., linear probing). Chaining generally leads to average-case constant time complexity, but with poor collision resolution, the worst-case can be O(n).
    

In summary:

*   **Average case time complexities** for insert, search, and delete: O(1)
    
*   **Worst case time complexities** for insert, search, and delete: O(n)
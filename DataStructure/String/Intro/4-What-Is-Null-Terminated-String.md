## What Is Null Terminated String?

A **null-terminated string** is a string representation in programming where the end of the string is indicated by a special null character, often represented as '\\0' in C and C-like languages. This null character signals the end of the string, allowing functions to determine its length and process it without requiring explicit length information.

### Key Characteristics

1.  **Null Character ('\\0')**:
    
    *   The null character is a byte with the value 0.
        
    *   It is used to mark the end of the string.
        
2.  **Memory Layout**:
    
    *   A null-terminated string is stored as a contiguous block of characters in memory, followed by the null character.
        
    *   For example, the string "Hello" is stored in memory as:
    ```python
    'H' 'e' 'l' 'l' 'o' '\0'
    ```

3.  **Operations**:
    
    *   Functions like strlen, strcpy, and strcat in C depend on the null character to determine the string's length or its boundaries.
        
4.  **Advantages**:
    
    *   Compact: Strings are stored without needing extra metadata like an explicit length.
        
    *   Compatibility: Many standard libraries and APIs are designed to work with null-terminated strings.
        
5.  **Disadvantages**:
    
    *   Error-prone: If the null character is missing or misplaced, operations can read beyond the intended string boundary, causing undefined behavior or security vulnerabilities.
        
    *   Performance: Functions like strlen must traverse the entire string to find the null terminator, which can be inefficient for long strings.

### Usage Example in C
```
#include <stdio.h>
#include <string.h>

int main() {
    char str[] = "Hello"; // Automatically null-terminated
    printf("String: %s\n", str);
    printf("Length: %lu\n", strlen(str)); // Output: 5 (null character is not counted)
    return 0;
}
```

### Comparison with Other Representations

*   **Explicit Length Strings**:
    
    *   In some programming languages (e.g., Python, Java), strings are stored with explicit length metadata, making them safer and more efficient to manipulate.
        
    *   Example: Python's len("Hello") doesn't need to traverse the string because the length is pre-stored.
        

The null-terminated string concept is fundamental in low-level programming and forms the basis of string handling in languages like C and C++.
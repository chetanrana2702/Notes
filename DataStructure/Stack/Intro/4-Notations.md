### <b style="color:blue">Notations</b>

### <b style="color:orange">Infix, Prefix, and Postfix Notations</b>


Mathematical expressions can be represented in three primary notations: **infix**, **prefix**, and **postfix**. Each notation has its own structure and advantages, particularly in terms of human readability and computational efficiency.

### <b style="color:mediumvioletred">Infix Notation</b>


Infix notation is the most commonly used format for writing mathematical expressions. In this notation, operators are placed **between** their operands. For example, the expression for adding two numbers is written as:

*   **Infix**: A+B_A_+_B_
    

<b style="color:blue">Characteristics:</b>

*   **Human-readable**: Infix notation is intuitive and easy for humans to understand.
    
*   **Parentheses usage**: Parentheses are often required to indicate the order of operations, especially when multiple operators are involved (e.g., (A+B)×C(_A_+_B_)×_C_).
    
*   **Operator precedence**: The evaluation of expressions depends on operator precedence rules, which can complicate parsing for computers.

### <b style="color:mediumvioletred">Prefix Notation (Polish Notation)</b>


In prefix notation, also known as Polish notation, the operator precedes its operands. For example, the same addition expression would be written as:

*   **Prefix**: +AB+_AB_
    

<b style="color:blue">Characteristics:</b>

*   **No parentheses needed**: The order of operations is clear from the placement of operators, eliminating the need for parentheses.
    
*   **Evaluation method**: Expressions are evaluated from right to left, making it efficient for machines to parse.
    
*   **Example transformation**:
    
    *   Infix: A+B_A_+_B_
        
    *   Prefix: +AB+_AB_
        
    *   For a more complex expression like (A+B)×C(_A_+_B_)×_C_: Prefix becomes ×+ABC×+_ABC_.
        

### <b style="color:mediumvioletred">Postfix Notation (Reverse Polish Notation)</b>


In postfix notation, also known as Reverse Polish notation (RPN), the operator follows its operands. For instance:

*   **Postfix**: AB+_AB_+
    

<b style="color:blue">Characteristics:</b>

*   **No parentheses needed**: Similar to prefix, postfix does not require parentheses due to its unambiguous structure.
    
*   **Evaluation method**: Expressions are evaluated from left to right, which simplifies computation for machines.
    
*   **Example transformation**:
    
    *   Infix: A+B_A_+_B_
        
    *   Postfix: AB+_AB_+
        
    *   For the expression (A+B)×C(_A_+_B_)×_C_: Postfix becomes AB+C×_AB_+_C_×.
        

### <b style="color:orange">Comparison Summary</b>


FeatureInfixPrefixPostfixOperator PlacementBetween operandsBefore operandsAfter operandsReadabilityHighModerateModerateParentheses RequiredOftenNoNoEvaluation DirectionLeft-to-rightRight-to-leftLeft-to-rightComplexity for MachinesHigherLowerLower

### <b style="color:orange">Conclusion</b>

In summary, infix notation is user-friendly but less efficient for computation due to its reliance on operator precedence and parentheses. Prefix and postfix notations streamline expression evaluation by removing these complexities, making them favorable in programming and computational contexts. Each notation serves distinct purposes depending on the application requirements in mathematics and computer science.


## <b style="color:blue">How Stack Datastructure is involved with them</b>

The stack data structure plays a crucial role in the conversion and evaluation of infix, prefix, and postfix expressions. Here's how stacks are involved with these notations:

### <b style="color:red">Conversion from Infix to Postfix and Prefix</b>


1.  <b style="color:blue">Infix to Postfix Conversion:</b>
    
    *   The conversion process uses a stack to temporarily hold operators and parentheses while scanning the infix expression from left to right.
        
    *   **Steps**:
        
        *   When an operand is encountered, it is added directly to the output (postfix expression).
            
        *   When an operator is encountered, it is pushed onto the stack after popping operators from the stack that have higher or equal precedence.
            
        *   Parentheses are handled by pushing '(' onto the stack and popping until '(' when ')' is encountered.
            
        *   After scanning the entire expression, any remaining operators in the stack are popped to form the final postfix expression.
            
2.  <b style="color:blue">Infix to Prefix Conversion:</b>
    
    *   Similar to postfix conversion, but the process involves reversing the infix expression first. Operators are then pushed onto a stack while scanning from right to left.
        
    *   The final prefix expression is constructed by popping operators from the stack after processing all operands.
        

### <b style="color:red">Evaluation of Postfix Expressions</b>

*   Postfix expressions can be evaluated efficiently using a stack:
    
    *   <b style="color:blue">Steps:</b>
        
        *   Scan the postfix expression from left to right.
            
        *   When an operand is encountered, it is pushed onto the stack.
            
        *   When an operator is encountered, operands are popped from the stack, the operation is performed, and the result is pushed back onto the stack.
            
        *   This continues until the entire expression has been processed, leaving the final result at the top of the stack.
            

### <b style="color:red">Advantages of Using Stack</b>


*   <b style="color:blue">Efficiency:</b> Stacks allow for efficient management of operators and operands without needing to consider operator precedence during evaluation in postfix notation.
    
*   <b style="color:blue">Simplicity:</b> The use of stacks simplifies both conversion and evaluation processes by providing a clear structure for handling operators and operands.
    

In summary, stacks are integral for converting between infix, prefix, and postfix notations and for evaluating postfix expressions efficiently. Their Last In First Out (LIFO) nature makes them well-suited for these tasks.
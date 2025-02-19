- logical operators
- conditional expressions

Here are the notes on Logical Operators in Python without styling:

# Logical Operators in Python:

1. `and` Operator:
   - Syntax: `a and b`
   - Returns: True if both `a` and `b` are True; otherwise, False.
   - Example: 
     True and True  # Returns True
     True and False # Returns False

2. `or` Operator:
   - Syntax: `a or b`
   - Returns: True if at least one of `a` or `b` is True; otherwise, False.
   - Example:
     True or False  # Returns True
     False or False # Returns False

3. `not` Operator:
   - Syntax: `not a`
   - Returns: The inverse boolean value of `a`. If `a` is True, it returns False, and vice versa.
   - Example:
     not True  # Returns False
     not False # Returns True

Short-circuit Evaluation:

- With `and`: Evaluates to the first False value it encounters, or the last value if all are True.

- With `or`: Evaluates to the first True value it encounters, or the last value if all are False.

Examples:
- With 'and'
  0 and 1  # Returns 0, because 0 is treated as False
  1 and 0  # Returns 0, because after 1 (True), 0 (False) is encountered
  1 and 2  # Returns 2, because both are True, so it returns the last value

- With 'or'
  0 or 1  # Returns 1, because after 0 (False), 1 (True) is encountered
  1 or 0  # Returns 1, because the first value is True
  0 or 0  # Returns 0, as neither is True

Practical Use:

- Conditionals:
  if age > 18 and has_permission:
      print("Access granted")

- Combining conditions:
  if (x > 0 or y > 0) and not (z < 0):
      print("Condition met")

These operators are fundamental in controlling the flow of programs, especially in conditional statements and loops. Remember, Python treats None, False, zero of any numeric type, any empty sequence (like '', [], ()), or any empty mapping (like {}) as False in a boolean context. Anything else is True.


### Conditional Expressions in Python  

A **conditional expression** (also known as the **ternary operator**) in Python allows you to write an `if-else` statement in a single line.  

#### Syntax:  
```
value_if_true if condition else value_if_false
```

---

### Examples:  

#### Basic Example  
```
age = 20
status = "Adult" if age >= 18 else "Minor"
print(status)  # Output: Adult
```

#### Checking Even or Odd  
```
num = 7
result = "Even" if num % 2 == 0 else "Odd"
print(result)  # Output: Odd
```

#### Finding Maximum of Two Numbers  
```
a, b = 10, 20
max_value = a if a > b else b
print(max_value)  # Output: 20
```

#### Nested Ternary Expression  
```
marks = 85
grade = "A+" if marks >= 90 else "A" if marks >= 80 else "B"
print(grade)  # Output: A
```

#### Checking if a Number is Positive, Negative, or Zero  
```
num = -5
result = "Positive" if num > 0 else "Negative" if num < 0 else "Zero"
print(result)  # Output: Negative
```

---

### Why Use Conditional Expressions?  
- Shorter Code: Makes `if-else` conditions more compact.  
- Readability: Good for simple conditions, but avoid complex nesting. 

Remember, while conditional expressions are powerful for concise code, they should be used judiciously to maintain code clarity. For more complex logic, traditional if-else statements or multi-line if structures might be more appropriate.


- string functions
- string indexing
- format specifiers

### String Methods in Python  

Python provides various built-in methods to work with strings. Here are some commonly used string methods with examples.  

1. **Changing Case**  
   - `upper()` – Converts all characters to uppercase  
   ```
   text = "hello"
   print(text.upper())  # Output: HELLO
   ```
   - `lower()` – Converts all characters to lowercase  
   ```
   text = "HELLO"
   print(text.lower())  # Output: hello
   ```
   - `title()` – Converts the first letter of each word to uppercase  
   ```
   text = "hello world"
   print(text.title())  # Output: Hello World
   ```
   - `capitalize()` – Converts only the first character to uppercase  
   ```
   text = "hello world"
   print(text.capitalize())  # Output: Hello world
   ```

2. **Checking String Content**  
   - `isalpha()` – Returns `True` if all characters are alphabets  
   ```
   text = "Python"
   print(text.isalpha())  # Output: True
   ```
   - `isdigit()` – Returns `True` if all characters are digits  
   ```
   num = "12345"
   print(num.isdigit())  # Output: True
   ```
   - `isalnum()` – Returns `True` if all characters are alphanumeric (letters and numbers)  
   ```
   text = "Python123"
   print(text.isalnum())  # Output: True
   ```
   - `isspace()` – Returns `True` if the string contains only spaces  
   ```
   text = "   "
   print(text.isspace())  # Output: True
   ```

3. **Finding and Replacing**  
   - `find()` – Returns the index of the first occurrence of a substring (-1 if not found)  
   ```
   text = "Hello World"
   print(text.find("World"))  # Output: 6
   ```
   - `replace()` – Replaces a substring with another substring  
   ```
   text = "Hello World"
   print(text.replace("World", "Python"))  # Output: Hello Python
   ```
   - `count()` – Counts the occurrences of a substring  
   ```
   text = "banana banana apple"
   print(text.count("banana"))  # Output: 2
   ```

4. **String Splitting and Joining**  
   - `split()` – Splits a string into a list based on a delimiter  
   ```
   text = "apple,banana,orange"
   print(text.split(","))  # Output: ['apple', 'banana', 'orange']
   ```
   - `join()` – Joins a list into a string with a specified separator  
   ```
   words = ["Hello", "World"]
   print(" ".join(words))  # Output: Hello World
   ```

5. **Removing Whitespace**  
   - `strip()` – Removes spaces from both ends  
   ```
   text = "  hello  "
   print(text.strip())  # Output: 'hello'
   ```
   - `lstrip()` – Removes spaces from the left side  
   ```
   text = "  hello  "
   print(text.lstrip())  # Output: 'hello  '
   ```
   - `rstrip()` – Removes spaces from the right side  
   ```
   text = "  hello  "
   print(text.rstrip())  # Output: '  hello'
   ```

6. **String Formatting**  
   - `format()` – Formats a string using placeholders  
   ```
   name = "John"
   age = 25
   print("My name is {} and I am {} years old.".format(name, age))  
   # Output: My name is John and I am 25 years old.
   ```
   - `f-strings` – Another way to format strings  
   ```
   name = "John"
   age = 25
   print(f"My name is {name} and I am {age} years old.")  
   # Output: My name is John and I am 25 years old.
   ```

### String Indexing in Python  

In Python, strings are indexed using numerical positions starting from 0 for the first character. You can access individual characters using their index.  

1. **Positive Indexing (Left to Right)**  
   The first character is at index 0, the second at 1, and so on.  

   ```
   text = "Python"
   print(text[0])  # Output: P
   print(text[3])  # Output: h
   print(text[5])  # Output: n
   ```

2. **Negative Indexing (Right to Left)**  
   Python allows negative indexing, where -1 represents the last character, -2 is the second last, and so on.  

   ```
   text = "Python"
   print(text[-1])  # Output: n
   print(text[-3])  # Output: h
   print(text[-6])  # Output: P
   ```

3. **Accessing Characters in a Loop**  
   You can iterate through a string using a loop.  

   ```
   text = "Python"
   for char in text:
       print(char)
   ```

   Output:  
   ```
   P  
   y  
   t  
   h  
   o  
   n  
   ```

4. **String Slicing**  
   You can extract a substring using slicing [start:end].  
   - text[1:4] → starts at index 1 and stops before 4.  

   ```
   text = "Python"
   print(text[1:4])  # Output: yth
   ```

   - text[:4] → starts from the beginning (index 0) up to 4.  

   ```
   print(text[:4])  # Output: Pyth
   ```

   - text[2:] → starts from index 2 and goes till the end.  

   ```
   print(text[2:])  # Output: thon
   ```

   - text[-4:-1] → negative indexing slice.  

   ```
   print(text[-4:-1])  # Output: tho
   ```

5. **Skipping Characters with Step**  
   You can define a step size using text[start:end:step].  

   ```
   text = "Python"
   print(text[::2])  # Output: Pto
   print(text[::-1])  # Output: nohtyP (Reverses string)
   ```

These indexing techniques help extract and manipulate parts of a string in Python.

Format specifiers in Python are used to format output, especially with the `format()` method or f-strings. They define how values should be displayed in terms of width, precision, and type.  

1. **Basic Formatting using `format()`**  
   ```
   name = "Alice"
   age = 25
   print("My name is {} and I am {} years old.".format(name, age))
   ```
   Output: My name is Alice and I am 25 years old.  

   You can also specify positions:  
   ```
   print("My name is {1} and I am {0} years old.".format(age, name))
   ```
   Output: My name is Alice and I am 25 years old.  

2. **f-Strings (Python 3.6+)**  
   ```
   name = "Alice"
   age = 25
   print(f"My name is {name} and I am {age} years old.")
   ```
   Output: My name is Alice and I am 25 years old.  

3. **Format Specifiers for Numbers**  
   - `{:.2f}` Floating-point with 2 decimal places  
   - `{:.3f}` Floating-point with 3 decimal places  
   - `{:d}` Integer  
   - `{:b}` Binary format  
   - `{:o}` Octal format  
   - `{:x}` Hexadecimal (lowercase)  
   - `{:X}` Hexadecimal (uppercase)  
   - `{:e}` Scientific notation (lowercase)  
   - `{:E}` Scientific notation (uppercase)  

   ```
   num = 10
   print("Decimal: {:d}".format(num))    
   print("Binary: {:b}".format(num))     
   print("Octal: {:o}".format(num))      
   print("Hexadecimal: {:x}".format(num))
   print("Scientific: {:.2e}".format(1234.5678))  
   ```
   Output:  
   ```
   Decimal: 10
   Binary: 1010
   Octal: 12
   Hexadecimal: a
   Scientific: 1.23e+03
   ```

4. **Formatting Width and Alignment**  
   - `{:<10}` Left-align within 10 spaces  
   - `{:>10}` Right-align within 10 spaces  
   - `{:^10}` Center-align within 10 spaces  

   ```
   text = "Python"
   print("{:<10}".format(text))  
   print("{:>10}".format(text))  
   print("{:^10}".format(text))  
   ```
   Output:  
   ```
   Python    
       Python
     Python  
   ```

5. **Padding with Zeros**  
   ```
   num = 42
   print("{:05d}".format(num))  
   ```
   Output: 00042  

6. **Combining Multiple Specifiers**  
   ```
   pi = 3.14159
   print("Pi value: {:08.3f}".format(pi))  
   ```
   Output: Pi value: 003.142  

These format specifiers help control output presentation in Python.
# Index
- variables
- type casting
- input
- example

### Python Variables

A variable in Python is a name that refers to a value stored in memory. Python is dynamically typed, meaning you don’t need to declare the data type explicitly; Python determines it automatically.

#### Declaring and Assigning Variables

```python
x = 10         # Integer
name = "Konka" # String
price = 99.99  # Float
is_valid = True # Boolean
```

#### Variable Naming Rules

- Must start with a letter or an underscore  
- Cannot start with a number  
- Can contain letters, digits, and underscores  
- Case-sensitive (`name` and `Name` are different)  
- Cannot use Python keywords like `if`, `while`, `return`, etc.  

#### Reassigning Variables

Python allows reassigning variables to different values or even different types.

```python
x = 10
x = "Now I'm a string"
```

#### Multiple Assignments

```python
a, b, c = 1, 2, 3
x = y = z = 100  # All three variables get the value 100
```

#### Type Checking

To check the type of a variable, use the `type()` function.

```python
x = 10
print(type(x))  # Output: <class 'int'>

y = "Hello"
print(type(y))  # Output: <class 'str'>
```

#### Deleting Variables

```python
x = 10
del x
```
# Type Casting
Type casting in Python is the process of converting one data type into another. Python provides built-in functions for both implicit and explicit type casting.  

Implicit type casting happens automatically when Python converts a smaller data type to a larger one.  

```python
a = 10  
b = 2.5  
c = a + b  
print(c)  # Output: 12.5  
print(type(c))  # Output: <class 'float'>  
```

Explicit type casting requires using functions to manually convert data types.  

- `int()` converts to integer  
- `float()` converts to float  
- `str()` converts to string  
- `bool()` converts to boolean  
- `list()` converts to list  
- `tuple()` converts to tuple  
- `set()` converts to set  

```python
x = "100"  
y = int(x)  
print(y, type(y))  # Output: 100 <class 'int'>  

a = 5.75  
b = int(a)  
print(b)  # Output: 5  

c = 10  
d = float(c)  
print(d)  # Output: 10.0  

e = 1  
f = bool(e)  
print(f)  # Output: True  

g = [1, 2, 3]  
h = tuple(g)  
print(h)  # Output: (1, 2, 3)  
```

# input

In Python, the `input()` function is used to take user input from the keyboard. It always returns the input as a string, so type conversion is needed if you require a different data type.  

Basic usage:  

```python
name = input("Enter your name: ")  
print("Hello, " + name)  
```

Taking numerical input:  

```python
age = input("Enter your age: ")  
age = int(age)  # Convert string to integer  
print("You are", age, "years old.")  
```

Using `float()` for decimal input:  

```python
price = float(input("Enter the price: "))  
print("Price is:", price)  
```

Taking multiple inputs in one line using `split()`:  

```python
x, y = input("Enter two numbers: ").split()  
x = int(x)  
y = int(y)  
print("Sum:", x + y)  
```

Using `map()` for multiple integer inputs:  

```python
a, b, c = map(int, input("Enter three numbers: ").split())  
print("Product:", a * b * c)  
```
# Example 
Here’s a simple Mad Libs game using Python and the input() function. The game asks the user for different words and then places them into a fun story.

```python
# Mad Libs Game

# Taking user inputs
name = input("Enter a name: ")  
place = input("Enter a place: ")  
animal = input("Enter an animal: ")  
food = input("Enter a food item: ")  
verb = input("Enter a verb: ")  

# Creating the story
story = f"One day, {name} went to {place} and saw a {animal}. The {animal} was eating {food} while trying to {verb}. It was the funniest thing {name} had ever seen!"  

# Displaying the story
print("\nHere is your Mad Libs story:\n")
print(story)
```
1. The program asks for inputs like a name, place, animal, food, and verb.
2. It then inserts those words into a predefined story.
3. The final story is displayed with the user’s inputs.
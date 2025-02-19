# Index
- arithmetic & math using python
- if else conditions
- examples
# arithmetic & math
Arithmetic Operations in Python
Python provides basic arithmetic operators for mathematical calculations:

1. Addition (+): Adds two numbers.
2. Subtraction (-): Subtracts one number from another.
3. Multiplication (*): Multiplies two numbers.
4. Division (/): Divides two numbers and returns the result as a float.
5. Floor Division (//): Divides two numbers and rounds down to the nearest whole number.
6. Modulus (%): Returns the remainder of a division.
7. Exponentiation (**): Raises a number to the power of another.

```python
a = 10  
b = 3  

print(a + b)  # 13  
print(a - b)  # 7  
print(a * b)  # 30  
print(a / b)  # 3.3333  
print(a // b) # 3 (floor division rounds down)  
print(a % b)  # 1 (remainder of 10/3)  
print(a ** b) # 1000 (10^3)  
```

**Math Module in Python**
Python’s math module provides advanced mathematical functions.

1. math.sqrt(x): Returns the square root of x.
2. math.pow(x, y): Returns x raised to the power y (same as x ** y).
3. math.ceil(x): Rounds x up to the nearest whole number.
4. math.floor(x): Rounds x down to the nearest whole number.
5. math.factorial(x): Returns the factorial of x (e.g., 5! = 5 × 4 × 3 × 2 × 1 = 120).
6. math.log(x): Returns the natural logarithm (base e) of x.
7. math.log10(x): Returns the logarithm (base 10) of x.
8. math.sin(x), math.cos(x): Returns the sine and cosine of x (in radians).
9. math.pi: Returns the value of π (3.14159...).
10. math.e: Returns Euler’s number (2.718...).

**Example**
```python
import math  

print(math.sqrt(16))       # 4.0  
print(math.pow(2, 3))      # 8.0  
print(math.ceil(3.2))      # 4  
print(math.floor(3.9))     # 3  
print(math.factorial(5))   # 120  
print(math.log(10))        # 2.3025 (natural log)  
print(math.log10(100))     # 2  
print(math.sin(math.radians(30)))  # 0.5  
print(math.cos(math.radians(60)))  # 0.5  
print(math.pi)            # 3.14159...  
print(math.e)             # 2.718...  
```

# if statement in python
Python's if statement is used to make decisions in a program. It executes a block of code only if a given condition is True.

```python
# Basic if statement
age = 20
if age >= 18:
    print("You are an adult.")

# if-else statement
num = int(input("Enter a number: "))
if num % 2 == 0:
    print("Even number")
else:
    print("Odd number")

# if-elif-else statement
marks = 85
if marks >= 90:
    print("Grade: A+")
elif marks >= 80:
    print("Grade: A")
elif marks >= 70:
    print("Grade: B")
else:
    print("Grade: C")

# Checking multiple conditions using
age = 25
income = 40000
if age > 18 and income > 30000:
    print("Eligible for loan")
else:
    print("Not eligible")

# Checking multiple conditions using or
day = "Sunday"
if day == "Saturday" or day == "Sunday":
    print("It's the weekend!")
else:
    print("It's a weekday.")

# Nested if statements
num = 15
if num > 10:
    print("Number is greater than 10")
    if num % 5 == 0:
        print("Number is also divisible by 5")

# Using not for negation
logged_in = False
if not logged_in:
    print("Please log in to continue")

# Ternary if (One-Line if-else)
x = 10
result = "Positive" if x > 0 else "Negative"
print(result)

# Using in with if
vowels = "aeiou"
letter = "a"
if letter in vowels:
    print(f"{letter} is a vowel")

# Comparing strings
password = "secret123"
if password == "secret123":
    print("Access granted")
else:
    print("Access denied")
```
**Examples**
# Simple Calculator using if statements
```python
num1 = float(input("Enter first number: "))
operator = input("Enter operator (+, -, *, /, //, %, **): ")
num2 = float(input("Enter second number: "))

if operator == "+":
    print("Result:", num1 + num2)
elif operator == "-":
    print("Result:", num1 - num2)
elif operator == "*":
    print("Result:", num1 * num2)
elif operator == "/":
    if num2 != 0:
        print("Result:", num1 / num2)
    else:
        print("Error: Division by zero")
elif operator == "//":
    if num2 != 0:
        print("Result:", num1 // num2)
    else:
        print("Error: Division by zero")
elif operator == "%":
    if num2 != 0:
        print("Result:", num1 % num2)
    else:
        print("Error: Division by zero")
elif operator == "**":
    print("Result:", num1 ** num2)
else:
    print("Invalid operator")
```

# Weight Conversion Program
```python
weight = float(input("Enter weight: "))
unit = input("Enter unit (kg, g, lb, oz): ").lower()

if unit == "kg":
    print("In grams:", weight * 1000)
    print("In pounds:", weight * 2.20462)
    print("In ounces:", weight * 35.274)
elif unit == "g":
    print("In kilograms:", weight / 1000)
    print("In pounds:", weight * 0.00220462)
    print("In ounces:", weight * 0.035274)
elif unit == "lb":
    print("In kilograms:", weight / 2.20462)
    print("In grams:", weight * 453.592)
    print("In ounces:", weight * 16)
elif unit == "oz":
    print("In kilograms:", weight / 35.274)
    print("In grams:", weight * 28.3495)
    print("In pounds:", weight / 16)
else:
    print("Invalid unit")
```

```python
# Temperature Conversion Program

temperature = float(input("Enter temperature: "))
unit = input("Enter unit (C for Celsius, F for Fahrenheit, K for Kelvin): ").upper()

if unit == "C":
    print("In Fahrenheit:", (temperature * 9/5) + 32)
    print("In Kelvin:", temperature + 273.15)
elif unit == "F":
    print("In Celsius:", (temperature - 32) * 5/9)
    print("In Kelvin:", (temperature - 32) * 5/9 + 273.15)
elif unit == "K":
    print("In Celsius:", temperature - 273.15)
    print("In Fahrenheit:", (temperature - 273.15) * 9/5 + 32)
else:
    print("Invalid unit")
```
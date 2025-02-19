# loops
- while
- for
- nested loops
- compound interest program

### Loops in Python  

Loops in Python allow executing a block of code multiple times. There are two main types of loops: while and for loops.  

1. **While Loop**  
A while loop runs as long as a condition is true.  

```python
count = 1
while count <= 5:
    print("Count:", count)
    count += 1
```
Output:  
```
Count: 1  
Count: 2  
Count: 3  
Count: 4  
Count: 5  
```

2. **For Loop**  
A for loop is used to iterate over a sequence (list, string, range, etc.).  

```python
for i in range(1, 6):
    print("Number:", i)
```
Output:  
```
Number: 1  
Number: 2  
Number: 3  
Number: 4  
Number: 5  
```

3. **Nested Loops**  
A loop inside another loop is called a nested loop.  

```python
for i in range(1, 4):
    for j in range(1, 4):
        print("i =", i, "j =", j)
```
Output:  
```
i = 1 j = 1  
i = 1 j = 2  
i = 1 j = 3  
i = 2 j = 1  
i = 2 j = 2  
i = 2 j = 3  
i = 3 j = 1  
i = 3 j = 2  
i = 3 j = 3  
```

4. **Compound Interest Program**  
The formula for compound interest is:  
A = P(1 + r/n)^(nt)  

- P = Principal amount  
- r = Annual interest rate (in decimal)  
- n = Number of times interest is compounded per year  
- t = Number of years  
- A = Final amount  

```
P = float(input("Enter principal amount: "))
r = float(input("Enter annual interest rate (in %): ")) / 100
n = int(input("Enter number of times interest is compounded per year: "))
t = int(input("Enter number of years: "))

A = P * (1 + r/n) ** (n*t)

print("Compound Interest:", round(A, 2))
```

Example Input:  
```
Enter principal amount: 1000  
Enter annual interest rate (in %): 5  
Enter number of times interest is compounded per year: 4  
Enter number of years: 2  
```

Example Output:  
```
Compound Interest: 1104.49  
```

# Countdown Timer Program in Python  

A countdown timer decreases the time and prints the remaining seconds until it reaches zero.  

```python
import time

seconds = int(input("Enter the countdown time in seconds: "))

while seconds > 0:
    print("Time left:", seconds, "seconds")
    time.sleep(1)  
    seconds -= 1

print("Time's up!")
```

Example Input and Output  

Input:  
```
Enter the countdown time in seconds: 5
```

Output:  
```
Time left: 5 seconds  
Time left: 4 seconds  
Time left: 3 seconds  
Time left: 2 seconds  
Time left: 1 second  
Time's up!  
```
This program takes a number of seconds as input and decreases it every second using the time.sleep(1) function.

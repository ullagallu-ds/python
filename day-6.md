# collections
- lists 
- sets 
- tuples
- dictionary

- shopping cart program
- concession stand program


Collections in Python include lists, sets, tuples, and dictionaries. These data structures help store and manage data efficiently.  

1. Lists  
A list is an ordered, mutable collection that allows duplicate values.  

```python
fruits = ["apple", "banana", "cherry"]
fruits.append("orange")
print(fruits)
```
Output:  
```
['apple', 'banana', 'cherry', 'orange']
```

2. Sets  
A set is an unordered collection with unique elements.  

```python
numbers = {1, 2, 3, 4, 5}
numbers.add(3)
print(numbers)
```
Output:  
```
{1, 2, 3, 4, 5}
```
(The number 3 is not added again since sets do not allow duplicates.)  

3. Tuples  
A tuple is an ordered, immutable collection.  

```python
colors = ("red", "green", "blue")
print(colors[1])
```
Output:  
```
green
```

4. Dictionary  
A dictionary stores key-value pairs.  

```python
student = {"name": "John", "age": 20, "grade": "A"}
print(student["name"])
```
Output:  
```
John
```

Shopping Cart Program  

A shopping cart program allows users to add, remove, and view items.  

```python
cart = {}

while True:
    action = input("Enter 'add', 'remove', 'view', or 'exit': ").lower()

    if action == "add":
        item = input("Enter item name: ")
        quantity = int(input("Enter quantity: "))
        cart[item] = cart.get(item, 0) + quantity
    elif action == "remove":
        item = input("Enter item name to remove: ")
        if item in cart:
            del cart[item]
        else:
            print("Item not in cart.")
    elif action == "view":
        print("Shopping Cart:", cart)
    elif action == "exit":
        break
    else:
        print("Invalid action.")
```

Example Interaction:  
```
Enter 'add', 'remove', 'view', or 'exit': add  
Enter item name: Apple  
Enter quantity: 3  

Enter 'add', 'remove', 'view', or 'exit': view  
Shopping Cart: {'Apple': 3}  

Enter 'add', 'remove', 'view', or 'exit': exit  
```

Concession Stand Program  

A concession stand sells snacks. This program allows users to order items and calculates the total cost.  

```python
menu = {"Popcorn": 5, "Soda": 2, "Candy": 3}
order = {}

while True:
    print("Menu:", menu)
    item = input("Enter item to order (or 'done' to finish): ").capitalize()
    
    if item == "Done":
        break
    elif item in menu:
        quantity = int(input("Enter quantity: "))
        order[item] = order.get(item, 0) + quantity
    else:
        print("Item not available.")

total = sum(menu[item] * qty for item, qty in order.items())
print("Order Summary:", order)
print("Total Cost: $", total)
```

Example Interaction:  
```
Menu: {'Popcorn': 5, 'Soda': 2, 'Candy': 3}  
Enter item to order (or 'done' to finish): Popcorn  
Enter quantity: 2  

Menu: {'Popcorn': 5, 'Soda': 2, 'Candy': 3}  
Enter item to order (or 'done' to finish): Soda  
Enter quantity: 1  

Enter item to order (or 'done' to finish): done  
Order Summary: {'Popcorn': 2, 'Soda': 1}  
Total Cost: $12  
```

This covers collections and two programs using lists, dictionaries, and loops.
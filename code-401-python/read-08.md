# Read: 08 - List Comprehensions - 01/04/2022

```python
# Syntax
# [ expression for item in list ]

# Example 1: Create a List with range()
digits = [ x for x in range(10) ]

# Example 2: Multiplying parts of a List
multiples_of_five = [x * 3 for x in range(10)]

# Example 3: Reading line from a text file
file = open("example.txt", "r")
lines = [ line for line in file ]
```

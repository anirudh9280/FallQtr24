- Recursion is the process of defining something in terms of itself
- two parallel mirrors facing each other would be reflected recursively
- a function can call other functions in Python, as we saw with Higher-Order Functions
- However, they can also call themselves, this is recursion
Example of a Recursive Function
```python
def factorial(x):
	if x == 1:
		return 1
	else:
		return (x * factorial(x-1))
print("The factorial of", 3 "is", factorial(3))
Output:
The factorial of 3 is 6
```
- ![[Screenshot 2024-02-14 at 12.59.45 AM.png]]
As you can see, the function stops when it is called with 1 as the argument, this is called the **base case**
All recursive functions must have this so they stop being called
if the base case is not provided, the Python interpreter stops after the maximum depth of recursion which is 1000
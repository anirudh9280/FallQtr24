- functions are considered "first-class" citizens of Python
```python
def function1():
	print("Hello from the outer function")
	def function2():
		print("Hello from the inner function")
	function2()
function1()
```
This returns nothing when it is executed because the inner function is not returned 
```python
def num1(x):
	def num2(y):
		return x*y
	return num2
res = num1(10)
print(res(5))
Output
50
```
Keep in mind that we cannot change any variables defined in the outer function, however we can access them
So why should we use inner functions?
- an inner function is protected from what is happening outside of the function -> it is protected from the global scope
```python
def outer_function(x):
	def inner_increment(x):
		return x + 2
	y = inner_increment(x)
	print(x, y)
inner_increment(5)
```
This won't work because the outer function has to be called before the inner one, this means that the inner function is protected from bad inputs


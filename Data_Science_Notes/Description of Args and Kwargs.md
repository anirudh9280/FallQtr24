## **args **kwargs link summary

**args**
- used to pass non-keyword arguments
- func(3, 4) and func('foo', 'bar') are args 
code examples of args: 
```python
def add(a, b, c):
	print (a+b+c)
add(1, 2, 3)
>>> 6
```
If we pass in four arguments instead of three, we would get an error as we can only take in 3
To change this with * args:
```python
def add(*args):
	total = 0
	for arg in args:
		total += arg
	print(total)
```
In this case, we could pass in 1,2 or 1, 2, 3, 4 and we would get the correct answer
If we pass in a list, the list is treated as one item and it is displayed. In the case above, since we are adding to total, we would unpack the parameter itself with add(* list) where list would be [12, 3, 5]
**kwargs
- this is a dictionary of keyword arguments and this is basically a dictionary
- an example of this would be fun(foo=2, bar=7)
- these are just like args except we declare the variables and the amount within the function arguments
These are useful when you want to reduce code writing and reusing 

Code Examples: 
```python
def my_function(x=10, y=20):
	print x, y
>>> 10, 20
```
```python
def capital_cities(**kwargs)
	result = []
	for key, value in kwargs.items():
		result.append("The capital city of {} is {} .format (key,value)
		return result
print(capital_city("China"="Beijing", "Egypt"="Cairo"))
>>> The capital city of China is Beijing. The capital city of Egypt is Cairo
```
Summary:
- `*args` and `**kwargs` are special syntax that are used in functions to pass a variable number of arguments to a function.
- `*args` occur before `**kwargs` in a function definition.  
    
- `*args` and `**kwargs` are best used in situations where the number of inputs will remain relatively small.
- You can use any name you want; `args` and `kwargs` are only by convention and not a requirement. For example, you can use `*foo` instead of `*args` or `**foo` instead of `**kwargs`.

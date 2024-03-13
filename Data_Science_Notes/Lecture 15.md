First Example: 
	growth rate of 
	sum = 0
	j = n
	while j > i:
		print(j)
		 j = j // 2
	the growth rate of this would be O(log n) because of the floor division 
	it would be while n // 2^x > 1
	what is x to make n go 1
	n = 2^
	x = log base 2 n so this would be logarithmic
Second Example:
```python
	sum = 0
	j = 1
	for i in range(1, n+1):
		while j <= i:
			sum = sum *  i + j
				j = j + 1
```
```
		This would be O(n) because the second loop would terminate after the first iteration as j would be bigger than i, then that leaves the top for loop and this would just be O(n)
Third Example: 
``
	sum = 0 
	j = n 
	while j <= n:
	print(j)
	 j = j * 2

```
O(1) because the loop would only run once as j would be set to 2n which is not less than or equal to n 
Fourth Example:
```python
	def f1(n):
		sum = 0
		 for i in range(1, n+1):
			 sum = sum * i
			 print(i)
		def f2(n):
			for i in range(1, n +1):
				f1(n)

```
this would be O(n^2) because the first function runs n times inside of the for loop of the second function which also runs in O(n^2)


# Advanced Argument Passing (**args and **kwargs)
[[Description of Args and Kwargs]]

- Always have default arguments at the end to avoid errors
```python
def report(day, time, name="Ani"):
	return "The day is " + day + " and the time is " + time + " and my name is " + name
print(report("Saturday", "morning"))
>>> The day is Saturday and the time is morning and my name is Ani.
```
Of course, if we do pass in a value for name, then the default argument is ignored

Checkpoint Question:
```python
def student(fname, lname="Potter", house="Gryffindor"):
	print(fname, lname, 'studies in', house)
>>> student("Harry")
>>> student("Draco", "Malfoy", "Slytherin")
Output:
Harry Potter studies in Gryffindor
Draco Malfoy studies in Slytherin
```
Checkpoint Question:
```python
def student(fname, lname="Potter", house="Gryffindor"):
	print(fname, lname, 'studies in', house)
>>> student("Draco Malfoy")
>>> student("Draco", "Slytherin")
Output:
Draco Malfoy studies in Gryffindor
Draco Slytherin studies in Gryffindor
```
To avoid the above bullshit:
```python
def student(fname, lname="Potter", house="Gryffindor"):
	print(fname, lname, 'studies in', house)
>>> student("Draco" house="Slytherin", lname="Malfoy")
Output:
Draco Potter studies in Slytherin
```
Note cannot say student(fname="Draco", "Slytherin"), push the default arguments or the * args to the end

Arbitrary Number of Arguments
- want functions that can work with any number of students
- the lnames in the function below becomes a tuple of all of the arguments that are passed in 
- you can use * lnames, or * args or whatever the hell you want 
```python
def logins(*lnames):
	for name in lnames:
		login = name[0] + name[::-1]
		print(name + " login is " + login)
>>> logins("Langlois")
Output:
Lsiolgnal
```
Example of * arg
```python
def test_args(f_arg, *args):
	print("first normal arg: ", f_arg)
	for arg in args:
		print("arg through *args: ", arg)
>>> test_args('one', 'two', '3')
Output:
first normal arg: one
arg through *args: two
arg through *args: 3
```

**kwargs
- unlimited number of keyword arguments
```python
def concatenate(**kwargs):
	result = ""
	# iterating over the Python kwargs dictionary
	for arg in kwargs.values():
		result += arg
	return result
print(concatentate(a="Real", b="Python", c="Is", d="Great", e="!"))
Output
RealPythonIsGreat!
```
You can check to make sure the length of the kwargs is positive by doing an if check with if len(kwargs) > 0: 
what happens in this scenario?
```python
name(marina="Langlois", donald="Trump", donald="Duck")
Output:
```
Error, cannot have parameters with exact same names
```python
def my_function(a, b=2, c=3, *args, **kwargs):

    print("a:", a)

    print("b:", b)

    print("c:", c)

    print("args:", args)

    print("kwargs:", kwargs)

  

my_function(1, "demo", "q", kw = "args")
```
This would return:
- a:1
- b: "demo"
- c: "q"
- args: ()
- kwargs: {'kw':'args'}

**Unpacking**
```python
def unpacking_example(a, b, c, d):
	return a * b * c *d
input_list = [1, 2, 3, 4]
unpacking_example(*input_list)
```
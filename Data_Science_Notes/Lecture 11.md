If you want to access a global variable in a function you would do: 
```python
x = 10
def add():
	global x 
	return x + 10
add(10) -> 20
```
How does **zip** work in python?
```python
people = {"kaii":['anisha', 'jay', 'amisha'], 'chunku':['thing', 'cat', 'dog']}
z = zip(people.values()[0],zip(people.values()[1]))
print(z)
Output:
[('anisha','thing'),('jay','cat'),('amisha','dog')]
```
- [[Nested Functions]]
Higher Order Functions add a level of abstraction to your code:
```python
def list_to_letter(lst):
	output = []
def first_letter(word):
	return word[0]
	for word in lst:
		output.append(first_letter(word))
	return output
```
Example
```python
def outer():
	x = 2
	def inner(a):
		print(a+x)
	print(x)
	inner(3)
outer()
Output:
2 
5
```
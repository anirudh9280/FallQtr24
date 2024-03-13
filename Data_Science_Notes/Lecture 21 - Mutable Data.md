- **Immutable** the value of the object cannot be changed
	- integers, strings, booleans, tuples, floats
- **mutable** - the value of the object can be changed
	- lists, dictionaries
- if you were to try and reassign a tuple, it would fail
```python
tup = (1, 2, 3, 4)
tup[2] = 3
Traceback (most recent call last):
...
TypeError: 'tuple' object does not support item assignment
```
- a variable is assigned to a compound value (object) and this is a reference or memory address to that object
- mutable objects can be changed but the variables still refer to it
- ![[Screenshot 2024-03-12 at 2.53.31 PM.png]]
```python
def test(x):
	x = x + 1
y = 10
test(y)
print(y) -> 10 
```
```python
def test(x):
	x[0] = x[0] + 1
y = [1, 2, 3]
test(y)
print(y)
[2, 2, 3]

var = ([1, 2], [3, 4])
copy = var
var[0][1] = 'changed'
var = ([1, 'changed'], [3, 4])
print(copy is var)
prints false because the reference point of var (id) changes after it is reassingned. whereas the id of copy is still the same as before
```
**Key**
![[Screenshot 2024-03-12 at 3.17.39 PM.png]]

```python
def func(lst):
	new_list = lst
	new_list[0] = 'a'
param = 'string'
func(param)
print(param)
Error
```
```python
x = [1, 2, 4]
y = x
x[0] = 'hei'
print(y) -> ['hei', 2, 4]
```

![[Screenshot 2024-03-12 at 3.30.07 PM.png]]
- ![[Screenshot 2024-03-12 at 3.45.58 PM.png]]
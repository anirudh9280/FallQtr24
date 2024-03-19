[[Exceptions]]
- an exception is an event which occurs during the execution of the program that disrupts the flow of the program's instructions
	- function receives an argument value of an improper type
	- file is not available
	- network connection is lost in the middle of the data transmission
- in general when a script is given some situation that it cannot cope with, it will *raise* an exception
- an exception is not a string object, it is a Python object
- there are built in exceptions that are in programming languages to respond to exceptional conditions
- exceptions are raised with the raise statement
- so it has to be raise expression(optional message 
- function that takes a list of numbers and represents ages that should be over 21 and prints the invitations should be
```python
lst = [1, 30, 21, 20, 17]
for item in lst:
	if item < 21:
		raise ValueError("Too young to come")
	else:
		print(f'{item} is invited')
```
- this fucks over the other numbers because 1 is less than 21, so to keep the program running for the other elements in the list, we have to use a try except block
- the try block is executed first and if there is an exception, the except block is ran
- you can have multiple try statements 
```python
def invert(x):
	inverse = 1/x
	print("Never printed if x is 0")
	return inverse
def invert_safe(x):
	try:
		return invert(x)
	except ZeroDivisionError as e:
		print(x) # 0 
		return str(e)
print(invert_safe(0))
-> divison by zero
```
what if we did invert_safe(1/0):
-> ZeroDivisionError: division by zero
if we added:
try:
	invert_safe(0)
except ZeroDivisionError as e:
	print("hello")
we get 'division by 0' because the except from the closest try except is called which is from invert_safe, not from the try at the bottom. also there is no error from the first try so it wouldnt go to the exception 
- if we did inverrrrt_safe(0) we would get a NameError  
- ![[Screenshot 2024-03-09 at 11.09.32 PM.png]]
```python
def invites(names, ages):
	for i in range(len(ages)):
		if (ages[i] < 21):
			raise ValueError("Too young to come")
		else:
			print("{} is above 21. {} you are invited".format(names[i], ages[i]))

def better_invites(names, ages):
	try:
		invites(names, ages)
	except ValueError as e:
		print(e)
better_invites(["Tom", "Mary", "Rosa"], [13, 44, 87])
```
Output: Too young to come
```python
try:
	x = 17 + "Marina"
except:
	pass
```
Nothing will happen 
```python
a = [0, 1, 2]
for element in a:
	if not element:
		pass
	print(element)
0 
1
2
for element in a;
	if not element:
		continue
	print(element)
1
2
```
```python
try:
	a = 1/0
except NameError as e:
	print("printed error")
```
Output: ZeroDivisionError: division by zero

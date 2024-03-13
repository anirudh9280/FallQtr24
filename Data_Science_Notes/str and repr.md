- hard to print out an instance of a class and get meaningful information about it if we do not implement a str or repr method 
```python
class Car:
	def __init__(self, color, mileage):
		self.color = color
		self.mileage = mileage
	def __str__(self):
		return f'a {self.color} car'
red_car = Car("red", 32)
print(red_car) -> 'a red car'
```
Difference between repr and str
```python
class Car:
    def __init__(self, color, mileage):
        self.color = color
        self.mileage = mileage

    def __repr__(self):
        return '__repr__ for Car'

    def __str__(self):
        return '__str__ for Car'
```
```python
my_car = Car('red', 37281)
print(my_car)
__str__ for Car
'{}'.format(my_car)
'__str__ for Car'
my_car
__repr__ for Car
```
you should use str(my_car) and repr(my_car) though
python real life example
```python
import datetime
today = datetime.date.today()
```
if you do str(today), you get '2017-02-02' because that is the human-consumable date.
if you do repr(today), you get 'datetime.date(2017, 2, 2)'
to properly define repr
```python
def __repr__(self):
   return (f'{self.__class__.__name__}('f'{self.color!r}, {self.mileage!r})')
```
If you do print(my_car) -> 'Car(red, 37281)' or str(my_car) you get the same thing even if __str__ is not defined in the class
![[Screenshot 2024-03-11 at 6.32.03 PM.png]]
```python
from fractions import Fraction
half = Fraction(1, 2)
repr(half) -> 'Fraction(1, 2)'
str(half) -> '1/2'
print(half) -> '1/2'
```

![[Screenshot 2024-03-11 at 6.55.16 PM.png]]
E is the right answer
**Polymorphic functions are functions that apply to different forms of data**
- str and repr are both polymorphic because they apply to objects
- if __str__ is not in a user defined class, then repr is the default
**Special Method**
python special methds
```python
__init__ (method that is invoked when an object is constructed)
__repr__ (method invoked when you want to display an object as a Python expression)
__add__ (method invoked to add one object to another)
__bool__(method invoked to convert an object to true or false)
__float__(method invoked to convert an object to a float)
```
```python
zero, one, two = 0, 1, 2
one.__add__(two) gives 3
zero.__bool__(), one.__bool__()
(False, True)
```
Question:
```python
class Student:
	def __init__(self, age):
		self.age = age
	def __lt__(self, another_Student):
		if self.age<anoter_Student.age:
		return True
```
s1 = Student(20)
s2 = Student(22)
print(s1<s2) -> True
CFU
```python
class Check:
	num = 10
	def question(self):
		print(self.num)
	def setter(self, number):
		self.num = number		
```
obj1 = Check()
obj2 = Check()
obj1.question() -> 10 
obj2.question() -> 10
When implementing repr you want to do 
def repr(x):
	return type(x).__repr__(x)


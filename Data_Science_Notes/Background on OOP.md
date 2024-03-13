- very good software maintaining 
- takes a lot of memory and is slow
- **Python**
	- offers very high level data types so this makes OOP support in python very easy 
	- however python is a lot slower than languages like Java and C++
- to create a class:
```python
class Dog:
	def __init__(self):
		pass
	
```
- __ init __  always needs to be called in a class definition and this is the constructor
- self is the same as this in java or c++
```python
#following the same code as above
class dog:
	def __init__(self, name, age):
		self.name = name
		self.age = age	
Kaia = Dog("Kaia", 3)
```
- now Kaia is an instance of the Dog class that is 3 years old
- to print her age and name, you can do print(Kaia.age, Kaia.name)
```python
	class Dog:

    def __init__(self, name, age):  
        self.name = name
        self.age = age

    def bark(self):
        print("bark bark!")
```
Now, you can do Kaia.bark() to print the statement
To add more complexity:
```python
class Dog:

    def __init__(self, name, age):  
        self.name = name
        self.age = age

    def bark(self):
        print("bark bark!")

    def doginfo(self):
        print(self.name + " is " + str(self.age) + " year(s) old.")

ozzy = Dog("Ozzy", 2)
skippy = Dog("Skippy", 12)
filou = Dog("Filou", 8)

ozzy.doginfo()
skippy.doginfo()
filou.doginfo()
ozzy.bark()
```
Output:
Ozzy is 2 year(s) old.
Skippy is 12 year(s) old.
Filou is 8 year(s) old.
bark bark
if you want to add a birthday method, you could do 
```python
class Dog:

    def __init__(self, name, age):  
        self.name = name
        self.age = age

    def bark(self):
        print("bark bark!")

    def doginfo(self):
        print(self.name + " is " + str(self.age) + " year(s) old.")
	def birthday():
		self.age += 1
```
If you want to change the instance's attributes through a function, you can do 
```python
class Dog:

    def __init__(self, name, age):  
        self.name = name
        self.age = age

    def bark(self):
        print("bark bark!")

    def doginfo(self):
        print(self.name + " is " + str(self.age) + " year(s) old.")
	def birthday():
		self.age += 1
	def setBuddy(self, buddy):
		self.buddy = buddy
		buddy.buddy = self
```
- this way, when you call the function setBuddy, you can set the buddy of one dog to another, but in this case you would only write one line of code compared to two because you have to make them buddies of each other to make it reciprocal 
- in Java, we would have to say the type of the parameter when passing it in 
- To visualize this
```python
kaia = Dog("kaia", 2)
ozzy = Dog("ozzy", 3)
kaia.setBuddy(ozzy)
print(kaia.buddy.age)
print(ozzy.buddy.name)
Output:
"3"
"kaia"
```
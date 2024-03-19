- The subclasses inherit the parent class
```python
class Animal():
	name = ""
	def eat(self):
		print("I can eat")
class Dog(Animal):
	def display(self):
		print("My name is ", self.name)
labrador = Dog()
labrador.name = "Rohu"
labrador.eat()
# I can eat
labrador.display()
# My name is Rohu
```
This is an 'is-a' relationship between two classes
**Method Overriding in Python Inheritance**
```python
class Animal():
	name = ""
	def eat(self):
		print("I can eat")
class Dog(Animal):
	def eat():
		print("I like to eat bones")
	def display(self):
		print("My name is ", self.name)
labrador = Dog()
labrador.name = "Rohu"
labrador.eat()
# I like to eat bones
labrador.display()
# My name is Rohu
```
The method in the subclass, eat, overrides the method in the parent class
```python
class Animal:
	name = ""
	def eat(self):
		print("I can eat")
class Dog(Animal):
	def eat(self):
		super().eat()
	print("I like to eat bones")
labrador = Dog()
labrador.eat()
# I can eat 
# I like to eat bones
```

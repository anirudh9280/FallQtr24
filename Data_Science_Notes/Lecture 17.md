[[Background on OOP]]
Used in real life to manage things such as bank accounts
- in the bank account example:
	- the account class will create instances of itself when the class constructor function is called with a name parameter
	- the init constructor creates instances of the class and passes in the parameters to attributes of the INSTANCE, not class
```python
class Account():
	def __ init __ (self, account_holder):
		self.balance = 0
		self.holder = account_holder
```
- if you create an object of the a=Account("a") class, and you do b = a, it doesn't create a new object it just points to where a is stored in memory
- you can add methods to class such as deposit in the account class
```python
class Account():
	def __ init __ (self, account_holder):
		self.balance = 0
		self.holder = account_holder
	def deposit(self, amount):
		self.balance += amount
		print(self.balance)
	def withdraw(self, amount):
		if amount > self.balance:
			return 'Insufficient Funds'
		self.balance -= amount
		return self.balance
```
Example:
```python
class Example:
count = 1
another_number = 6
def __init__(self, initial_value):
	self.count = 0
	self.count = self.count + initial_value
def increment(self, amount):
	self.count = self.count + amount
	
	Example.count = Example.count + 1
	
	return self.count
e = Example(4)
print(e.count)
print(Example.count)
print(e.another_number)
e.increment(10)
print (e.count)
print (Example.count)
```
Output:
4
1
6
14
2
```python
class Example:

    count = 1
    another_number = 6
    def __init__(self, initial_value):
        self.count = 0
        self.count = self.count + initial_value

    @classmethod
    def change_me(cls, new_count):
        cls.count = new_count
@staticmethod
 def i_am_static(param):
	 print(param+5)
e = Example(4)
Example.change_me(10)
print(e.count)
print(Example.count)
Example.i_am_static(10)
```
Output:
4 
2
- this class method modifies the attribute of the class itself
- the static method does not modify anything related to the class
- bound methods are when you call a function such as deposit on an instance
**Class Attributes**
- class attributes are shared across all instances of the class
```python
class Account:
interest = 0.02
def __init__(self, account_holder):
	self.balance = 0
	self.holder = account_holder
```
tom_account = Account("Tom")
jim_account = Account("Jim")
print(tom.interest, jim.interest) -> 0.02, 0.02

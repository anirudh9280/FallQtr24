[[Nested Functions]]
```python
def make_adder(n):
	def adder(k):
		return k + n
	return adder
add3 = make_adder(3)
print(add3(9))
Output:
12
```
This way, each function exactly has one job and this is the best way to avoid any debugging that is unnecessary
```python
def repeat(f, x):
	while f(x) != x:
		x = f(x)
	return x
	def g(y):
		return (y+5)//3
	result = repeat(g,5)
```


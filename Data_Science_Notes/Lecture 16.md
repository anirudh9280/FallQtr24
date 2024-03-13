[[Recursion Link Summary]]
```python
def anyOdd(lst):
	for num in lst:
		if num % 2 == 0:
			return True
		return False
anyOdd([2, 4, 6, 8])
```
This returns false if any of the elements in the list aren't even
We can use recursion to solve this problem, it would call itself until atleast one or more base case stops it

Above example with recursion
```python
def anyOdd(lst):
	if len(lst) == 0:
		return False
	if lst[0] % 2 == 0:
		return True
	else:
		smaller_list = anyOdd(lst[1:]) 
anyOdd([0, 4, 6, 8])
```

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
	
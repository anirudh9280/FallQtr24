## Big O Notation Examples|
```python
sum = 0
for i in range(1, n+1):
	sum = sum * i
	print(i)
```
This would be O(n) because it goes through the loop n times
``` python
sum = 0
for i in range(1, n+1):
	if (i%3 == 0):
		sum = sum * i
		print(i)
```
This would be O(n) because the i gets divided each time, the work would decrease 

```python
sum = 0
for i in range(1, n+1):
	for j in range(1, n+1):
		sum = sum * i + j
```
This would be O(n^2) because there are two nested for loops
```python
sum = 0
for i in range(1, n+1):
   j = 1
	while j <=i:
		sum = sum * i + j
		j = j + 1
```
This would be O(n^2) because the inner loop would run till the outer loop terminates
```python
sum = 0
j = n
while j>1:
	print(j)
	j = j//2
```
n/2^x = 1 -> log2n 
```python
sum = 0
for i in range(1, n+1):
	sum = sum * i
	for j in range(1, n+1):
		sum = sum + j
```
O(n^2)
```python
sum = 0
j = 1
for i in range(1, n+1):
	while j <=i:
		sum = sum * i + j
		j = j + 1
```
O(n) because the while loop stops 
```python
sum = 0
j = n
while j<=n:
	print(j)
	j = j*2
```
This is O(1) because j changes to 2n after the first iteration
```python
def f1(n):  
    sum = 0
for i in range(1, n+1):
	sum = sum * i
	print(i)
def f2(n):
for i in range(1, n+1):
	f1(n)
```
This is O(n^2)

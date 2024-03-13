- raise an exception with raise
- debug and test code with assert
- handle exceptions with try and except
- else and finally fine tune exception handling
- syntax error would occur when the parser detects an incorrect statement such as:
```python
print(0/ 0))
SyntaxError: unmatched ')'
```
if you were to do 
```python
print(0/0)
ZeroDivisionError: division by zero
```
to stop this from raising an exception, you can do this with **raise**
```python
number = 10 
if number > 5:
	raise Exception(f'The number should not exceed 5.({numnber=})')
	print(number)
```
Exception: The number should not exceed 5. (number=10)
the print(number) never got executed because the program stopped
if you want to do this with an assert (to check for conditions)
you would do 
```python
number = 10
assert number < 5
'The number should not exceed 5.'
print(number)
```
Assertion Error: The number should not exceed 5
however, python globally disables assertions when running python in optimized mode with -0
If you do not want your program to fail when encountering an exception, you could use a try except block 
To check if linux is in the mac os
```python
try:
	linux_interaction()
except RuntimeError as error:
	print(error)
	print("Linux function was not executed.")
```
![[Screenshot 2024-03-05 at 11.36.01 PM.png]]


Consider the following code: 
```python
from math import pi
tau = 2 *pi
```
The first import statement executes first and then the second one calculates the value of tau. In the global frame, pi is the name and the value is 3.1416, this cannot be repeated. 
- ![[Screenshot 2024-02-14 at 11.58.24 PM.png]]
- The built in function from the import and the function defined by the user is stored in the global frame and the function call is in the local frame and the returned value. 
An **environment** is a sequence of frames

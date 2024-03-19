str1.lower() - not in place
set1.update({5,6})  - in place
set1 - set2 - not in place
set_d.union(set_a) - not in place
lst.sort() - in place
sorted(lst)  - not in place
lst[::-1] - not in place       
lst.reverse()  - in place
list(iterable)  - not in place
dict1.update(dict2) - in place

reverse a list in place:
```python
    halve = 2 
    for i in range(len(lst)//halve):
        lst[i], lst[len(lst)-i-1] = lst[len(lst)-i-1],lst[i]
    return None
```


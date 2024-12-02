### Find the Maximum and Minimum in an Array
**Solution 1**
```python
arr=[] # Initializing an empty list
arr=[int(x) for x in input(f"Enter elements: ").split()] # Taking input from user using list comprehension.
man_num=max(arr) # Using max keyword
print(man_num)
min_num=min(arr)
print("The minimum number is: ",min_num)
```

**Solution 2**
```python
arr=[]
arr=[int(x) for x in input(f"Enter elements: ").split()]
sorting_the_array=sorted(arr)
print("The maximum number is :",sorting_the_array[-1])
print("The minimum number is :",sorting_the_array[0])
```

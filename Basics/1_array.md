### Find Missing Number in Array

```python
def find_large():

    my_array=[3,4,5,7,8,9,2,1]
    sum1=sum(my_array)
    arr=[]
    for i in range(1,10):
       arr.append(i)
    sum2=sum(arr)
    missing_no=sum2-sum1
    print(missing_no)
find_large()
```
-------------------------------------------------------

Q.Given an integer n perform the following conditional actions:<br>

-If n is odd, print Weird<br>
-If n is even and in the inclusive range of 2 to 5 , print Not Weird<br>
-If  is even and in the inclusive range of 6 to 20 , print Weird<br>
-If  is even and greater than 20, print Not Weird<br>


```python
n = int(input())

if n % 2 != 0:
    print("Weird")
elif n % 2 == 0 and (2 <= n <= 5):
    print("Not Weird")
elif n % 2 == 0 and (6 <= n <= 20):
    print("Weird")
elif n % 2 == 0 and n > 20:
    print("Not Weird")
```


```python
n = int(input())

if n % 2 != 0 or (n % 2 == 0 and 6 <= n <= 20):
    print("Weird")
else:
    print("Not Weird")
```

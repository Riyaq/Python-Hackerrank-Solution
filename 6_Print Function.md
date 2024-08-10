[The included code stub will read an integer n , from STDIN](https://www.hackerrank.com/challenges/python-print/problem?isFullScreen=true)

Without using any string methods, try to print the following:<br>
123....n<br>
Note that "...." represents the consecutive values in between.<br>

**Example**

Print the string 5.
```
12345
```

------------------------------------------------------------------------------------
```python
if __name__ == '__main__':
    n = int(input())
    i=1
    while(i<=n):
        print(i, end="")
        i+=1

```
------------------------------------------------------------------------------------
```python
def print_numbers(n):
    for i in range(1, n+1):
        print(i, end="")
    print()

n = int(input())
print_numbers(n)
```
------------------------------------------------------------------------------------





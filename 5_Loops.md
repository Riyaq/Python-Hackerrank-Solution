The provided code stub reads and integer n, from STDIN. For all non-negative integers i<n, print i^2.

[Example](https://www.hackerrank.com/challenges/python-loops/problem?isFullScreen=true)<br>

The list of non-negative integers that are less than n is  . Print the square of each number on a separate line.<br>
```
0
1
4
```
**Solution**


```python
n=int(input())
i=0
while i<n:

    print(i*i)
    i += 1
```

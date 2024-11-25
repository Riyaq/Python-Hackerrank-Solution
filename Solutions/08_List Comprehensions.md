[List Comprehensions](https://www.hackerrank.com/challenges/list-comprehensions/problem?isFullScreen=false)<br>
<br>
<br>
<img width="939" alt="Screenshot 2024-11-25 at 12 31 34 PM" src="https://github.com/user-attachments/assets/0b3af68d-fe9b-4b89-b43f-9028fd71b751">
<br>
<br>
**Concept:** <br>

List comprehensions are a concise and expressive way to create or transform lists in Python. They allow you to generate a new list by applying an expression to each item in an existing iterable (like a list, tuple, or range) in a single line of code. List comprehensions can replace traditional for loops that append to a list, often making the code shorter and more readable.

-------------------------------------------------
**Code when we don't use list comprehension-**
```python
if __name__ == '__main__':
    x = int(input())
    y = int(input())
    z = int(input())
    n = int(input())

    ar = []
    p = 0

    for i in range(x + 1):
        for j in range(y + 1):
            for k in range(z + 1):
                if i + j + k != n:
                    ar.append([])
                    ar[p] = [i, j, k]
                    p += 1
    print(ar)
```
Explanation:<br>
```
ar = []
p = 0
```
<mark>ar</mark> is an empty list that will store the result (a list of lists).<br>
<mark>p</mark> is used as an index to keep track of the position in ar when appending new lists.<br>
Nested Loop-<br>
```python
for i in range(x + 1):
    for j in range(y + 1):
        for k in range(z + 1):
```
<mark style="background-color: lightblue">i</mark> ranges from 0 to x (inclusive).<br>
<mark style="background-color: lightblue">j</mark> ranges from 0 to y (inclusive).<br>
<mark style="background-color: lightblue">k</mark> ranges from 0 to z (inclusive).<br>
```python
            if i + j + k != n:
                ar.append([])
                ar[p] = [i, j, k]
                p += 1
```
For each combination of i, j, and k, the program checks if the sum <mark>i + j + k</mark> is not equal to n.<br>
If <mark>i + j + k != n</mark>, then the combination [i, j, k] is appended to the list ar.<br>
<br>
Appending Combinations to ar:

>_Each time the condition if i + j + k != n is True, the code appends an empty list [] to ar and then fills the list at index p with [i, j, k].
>The index p is then incremented by 1 after each combination is added to ar._


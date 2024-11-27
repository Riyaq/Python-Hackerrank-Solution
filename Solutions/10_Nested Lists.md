## [Nested Lists](https://www.hackerrank.com/challenges/nested-list/problem?isFullScreen=true)
--------
Given the names and grades for each student in a class of N students, store them in a <mark>nested list</mark> and print the name(s) of <br>
any student(s) having the second lowest grade.<br>

Note: If there are multiple students with the second lowest grade, order their names alphabetically and print each name on a new line.<br>
<br>
**Input Format** <br>

The N first line contains an integer, , the number of students.<br>
The 2N subsequent lines describe each student over 2 lines.<br>
- The first line contains a student's name.<br>
- The second line contains their grade.<br>

**Constraints** <br>
2<=N<=5 <br>
There will always be one or more students having the second lowest grade.<br>
<br>
**Output Format** <br>

Print the name(s) of any student(s) having the second lowest grade in. If there are multiple students, order their names alphabetically and print each one on a new line.<br>
<br>
<br>
```
Sample Input
5
Harry
37.21
Berry
37.21
Tina
37.2
Akriti
41
Harsh
39
```
```
sample Output
Berry
Harry
```
**Explanation**

There are 5 students in this class whose names and grades are assembled to build the following list:

>python students = [['Harry', 37.21], ['Berry', 37.21], ['Tina', 37.2], ['Akriti', 41], ['Harsh', 39]]

The lowest grade of  belongs to Tina. The second lowest grade of  belongs to both Harry and Berry,<br>
so we order their names alphabetically and print each name on a new line.

-----------------------------------------
### Given code
```python
if __name__ == '__main__':
    for _ in range(int(input())): # Inside this loop you are asking the ser how many students do you have.
        name = input()            # Once user input the number how many then loop stats to take name and score input that many time.If you have 10 students this loop will run 10 times. In each round it will get a name and a score.
        score = float(input())
```
-----------------------------------------
### Solution
```python


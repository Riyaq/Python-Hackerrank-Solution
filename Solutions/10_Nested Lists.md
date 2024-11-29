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
### Solution 1
```python
def sort_student(names_scores):
    # Create an empty set to store unique scores (using a normal loop)
    scores = set()
    for student in names_scores:
        scores.add(student[1])  # Add the score to the set (automatically ensures uniqueness)
    
    # Convert the set to a sorted list
    sorted_scores = sorted(scores)
    
    # The second-lowest score is at index 1
    second_lowest = sorted_scores[1]
    
    # Create an empty list to store names of students with the second-lowest score
    names_second_lowest = []
    for student in names_scores:
        if student[1] == second_lowest:
            names_second_lowest.append(student[0])  # Add the name to the list
    
    # Sort the names alphabetically
    names_second_lowest.sort()
    
    # Print the names of students with the second-lowest score
    for name in names_second_lowest:
        print(name)

# Execution
if __name__ == '__main__':
    names_scores = []
    for _ in range(int(input())):
        name = input()
        score = float(input())
        names_scores.append([name, score])
    
    sort_student(names_scores)


```
### Solution 2 
Using list comprehension &  set comprehension.
```python
def sort_student(names_scores):
    # Create a set of unique scores
    scores = {student[1] for student in names_scores}
    
    # Sort the scores and find the second lowest score
    sorted_scores = sorted(scores)
    second_lowest = sorted_scores[1]
    
    # Collect names of students who have the second lowest score
    names_second_lowest = [student[0] for student in names_scores if student[1] == second_lowest]
    
    # Sort the names alphabetically
    names_second_lowest.sort()
    
    # Print the names of students with the second lowest score
    for name in names_second_lowest:
        print(name)

# Execution
if __name__ == '__main__':
    names_scores = []
    for _ in range(int(input())):
        name = input()
        score = float(input())
        names_scores.append([name, score])
    
    sort_student(names_scores)
```
More details - python/List Nested list/NestedloopJupyter.ipynb

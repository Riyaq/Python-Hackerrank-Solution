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
def sort_students(names_scores):
    # Create a list to store all the scores
    scores = []
    
    # Extract scores from each student's data and append to scores list
    for student in names_scores:
        scores.append(student[1])

    # Sort the scores and remove duplicates by converting to a set
    sorted_scores = sorted(set(scores))

    # If there are fewer than two distinct scores, return nothing (no second lowest score)
    if len(sorted_scores) < 2:
        return

    # The second lowest score will be the second element in the sorted unique scores list
    second_lowest = sorted_scores[1]

    # Create a list to store the names of students who have the second lowest score
    name_second_lowest = []

    # Iterate over the students to find those with the second lowest score
    for student in names_scores:
        if student[1] == second_lowest:
            name_second_lowest.append(student[0])

    # Sort the names alphabetically
    name_second_lowest = sorted(name_second_lowest)

    # Print the sorted names
    for name in name_second_lowest:
        print(name)


# Execution starts here
if __name__ == '__main__':
    # Initialize an empty list to store the students' name and score pairs
    names_scores = []
    
    # Read the number of students
    for _ in range(int(input())):  # Input number of students
        name = input()  # Input student name
        score = float(input())  # Input student score (converted to float)
        # Append the name and score as a list [name, score]
        names_scores.append([name, score])

    # Call the function to sort and print students with the second lowest score
    sort_students(names_scores)

```
More details - python/List Nested list/NestedloopJupyter.ipynb

[Given the participants' score sheet for your University Sports Day, you are required to find the runner-up score. You are given n scores.<br>
Store them in a list and find the score of the runner-up](https://www.hackerrank.com/challenges/find-second-maximum-number-in-a-list/problem?isFullScreen=true).<br>
<br>

**Input Format** <br>

The first line contains n. The second line contains an array A[] of n integers each separated by a space.<br>
<mark>2<=n<=10</mark><br>
<mark>-100<=A[i]<=100</mark><br>

**Output Format** <br>

Print the runner-up score<br>

```python
Sample Input :
5
2 3 6 6 5
```
```python
Sample Output :
5
```
---------------------------------------
### Solution 1
```python
if __name__ == '__main__':
    n = int(input("Enter how many participant: "))
    arr = map(int, input("Enter the scores here: ").split())

    print(sorted(set(arr), reverse=True)[1])
```

### Solution 2
```python
def runner_up():
    n = int(input("Enter the count of participants: "))  # This takes the number of participants remove the place holder.
    arr = list(map(int, input("Enter elements separated by spaces: ").split()))  # Convert input into a list of integers remove the place holder.

    # Step 1: Remove duplicates by converting the list to a set and sort it in descending order
    sorted_scores = sorted(set(arr), reverse=True)

    # Step 2: Ensure there are at least two unique scores
    if len(sorted_scores) > 1:
        print(f"The runner-up score is: {sorted_scores[1]}")
    else:
        print("No runner-up, all participants have the same score.")


# Call the function
runner_up()
```

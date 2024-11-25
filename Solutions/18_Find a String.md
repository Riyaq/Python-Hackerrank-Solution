[Question](https://www.hackerrank.com/challenges/find-a-string/problem?isFullScreen=true)<br>
In this challenge, the user enters a string and a substring. You have to print the number of times that the substring occurs in the given string.<br>
String traversal will take place from left to right, not from right to left.<br>

**Input**
The first line of input contains the original string. The next line contains the substring.

**Output**
Output the integer number indicating the total number of occurrences of the substring in the original string.
```
**Sample Input**
ABCDCDC
CDC
**Sample Output**
2
```

**Solution**
```python
def count_substring(string, substring):
    count = 0
    substring_length = len(substring)
    for i in range(len(string) - substring_length + 1):
        if string[i:i+substring_length] == substring:
            count += 1
    return count

# Read the input strings
original_string = input("Enter the original string: ")
substring = input("Enter the substring: ")

# Count the occurrences of the substring in the original string
occurrences = count_substring(original_string, substring)

# Print the result
print("Number of occurrences:", occurrences)
```

-------------------------------------------------------------------------------------------------------
-------------------------------------------------------------------------------------------------------
Explanation
------------
The purpose of this loop is to iterate over the indices of the string<br>
 where the **substring** can potentially be found. The loop<br>
```python
for i in range(len(string) - substring_length + 1):
```
 will iterate **len(string) - substring_length + 1** times, allowing for each possible starting position of the substring within the string

 --> 
 **len(string) - substring_length + 1**<br>
 calculates the maximum number of iterations for the loop. It represents the number of starting positions in the <br>
string where the substring can fit completely.

-------------------------------------------------------------------------------------------------------
```python
 if string[i:i+substring_length] == substring:
```
This slicing operation is a way to extract a portion of a string in Python. The syntax is 
```python
string[start:end]
```
where **start** is the index to start from (inclusive) and <br>
**end** is the index to end at (exclusive).<br>

**string[i:i+substring_length]** is a slicing operation that extracts a portion of the string starting from index i<br>
 and ending at index **i+substring_length-1** <br>
It creates a new substring from the original string.<br>
For example, if string is "Hello, world!" and i is 6, and substring_length<br>
 is 5, then string[i:i+substring_length] would evaluate to **"world"**

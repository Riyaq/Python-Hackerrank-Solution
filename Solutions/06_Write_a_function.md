We add a Leap Day on February 29, almost every four years. The leap day is an extra, or intercalary day and we add it to the shortest month of the year, February.<br>
<br>
In the Gregorian calendar three criteria must be taken into account to identify leap years:<br>
<br>
The year can be evenly divided by 4, is a leap year, unless:<br>
The year can be evenly divided by 100, it is NOT a leap year, unless:<br>
The year is also evenly divisible by 400. Then it is a leap year.<br>
This means that in the Gregorian calendar, the years 2000 and 2400 are leap years, while 1800, 1900, 2100, 2200, 2300 and 2500 are NOT leap years.<br>
<br>
You are given the year, and you have to write a function to check if the year is leap or not.<br>
<br>
Note that you have to complete the function and remaining code is given as template.<br>
[Link](https://www.hackerrank.com/challenges/write-a-function/problem?isFullScreen=true)

**Solution 1**
```python
def is_leap(year):
    return year % 4 == 0 and (year % 100 != 0 or year % 400 == 0)

year = int(input())
print(is_leap(year))
```
**Solution 2**
```python
def is_leap(year):
    leap = False
    
    # Write code here to determine if the given year is a leap year
    if year % 4 == 0 and (year % 100 != 0 or year % 400 == 0):
        leap = True
    
    return leap

year = int(input())
```
**Solution 3**
```python
def is_leap(year):
    if year % 4 == 0 and (year % 100 != 0 or year % 400 == 0):
        return True
    else:
        return False

year = int(input("Enter a year: "))
print(is_leap(year))
```

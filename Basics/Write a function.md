[Given a year, determine whether it is a leap year. If it is a leap year, return the Boolean True, otherwise return False](https://www.hackerrank.com/challenges/write-a-function/problem?isFullScreen=true).<br>

Note that the code stub provided reads from STDIN and passes arguments to the is_leap function.<br>
It is only necessary to complete the is_leap function.<br>


In the Gregorian calendar, three conditions are used to identify leap years:<br>
<br>
-The year can be evenly divided by 4, is a leap year, unless:<br>
---The year can be evenly divided by 100, it is NOT a leap year, unless:<br>
------The year is also evenly divisible by 400. Then it is a leap year.<br>

```python
def is_leap(year):
    leap = False
    
    # Write code here to determine if the given year is a leap year
    if year % 4 == 0 and (year % 100 != 0 or year % 400 == 0):
        leap = True
    
    return leap

year = int(input())
```

```python
def is_leap(year):
    if year % 4 == 0 and (year % 100 != 0 or year % 400 == 0):
        return True
    else:
        return False

year = int(input("Enter a year: "))
print(is_leap(year))
```


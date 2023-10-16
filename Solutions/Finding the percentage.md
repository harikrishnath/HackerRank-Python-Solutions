
# Finding The Percentage
## Problem

You have a record of `N` students. Each record contains the student's name, and their percent marks in Maths, Physics and Chemistry. The marks can be floating values. The user enters some integer `N` followed by the names and marks for `N` students. You are required to save the record in a dictionary data type. The user then enters a student's name. Output the average percentage marks obtained by that student, correct to two decimal places.

#### Input Format

The first line contains the integer `N`, the number of students. The next `N` lines contains the name and marks obtained by that student separated by a space. The final line contains the name of a particular student previously listed.



#### Constraints

2 <= `N` <= 10 <br />
0 <= `Marks[i]` <= 100 <br />
length of marks array = 3


#### Output Format

Print one line : The average of the marks obtained by the particular student correct to 2 decimal places.

**Sample Input 0**

```
3
Krishna 67 68 69
Arjun 70 98 63
Malika 52 56 60
Malika
```

**Sample Output 0**

```
56.00
```

**Explanation 0**

Marks for Malika are `{52,56,60}` whose average is (52+56+60)/3 = 56

<br>


**Sample Input 1**

```
2
Harsh 25 26.5 28
Anurag 26 28 30
Harsh
```

**Sample Output 1**

```
26.50
```

<br>


#### Given Code

```python
if __name__ == '__main__':
    n = int(input())
    student_marks = {}
    for _ in range(n):
        name, *line = input().split()
        scores = list(map(float, line))
        student_marks[name] = scores
    query_name = input()
```

## Solution

```python
if __name__ == '__main__':
    n = int(input())
    student_marks = {}
    for _ in range(n):
        name, *line = input().split()
        scores = list(map(float, line))
        student_marks[name] = scores
    query_name = input()
    print("%.02f" % (sum(student_marks[query_name]) / 3))
```

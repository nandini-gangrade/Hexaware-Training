# Repeat a set of steps - Loops

## DRY - Don't Repeat Yourself
The concept of DRY (Don't Repeat Yourself) emphasizes avoiding redundant code by using loops or functions to repeat a set of steps.

### Code Explanation
```python
countdown = 1
while countdown < 6:
    print(countdown)
    countdown = countdown + 1
```

### Output
```
1
2
3
4
5
```

## Task 1: Build pattern | Clue: *
In this task, we aim to build a pattern using stars (*).

### Code Explanation
```python
no_of_stars = 5
curr_star = 1
while curr_star < no_of_stars:
    print("✨" * curr_star)
    curr_star = curr_star + 1
```

### Output
```
✨
✨✨
✨✨✨
✨✨✨✨
✨✨✨✨✨
```

## Black Formatter (PEP)
Python Enhancement Proposal (PEP) 8 suggests using the black formatter for code styling. It ensures consistent code formatting.

## while vs for
While and for loops are used for iterating over sequences or executing a block of code repeatedly. The choice between them depends on the specific requirements of the task.

### Code Explanation (while loop)
```python
countdown = 1
while countdown < 6:
    print(countdown)
    countdown = countdown + 1
```

### Code Explanation (for loop)
```python
for countdown in range(1, 6):
    print(countdown)  # 1 - 5
```

### Code Explanation (for loop with step)
```python
for countdown in range(1, 6, 2):
    print(countdown)  # 1, 3, 5
```

## Task 2: Build pattern | Clue: *
In this task, we aim to build a pattern using stars (*) using a for loop.

### Code Explanation
```python
no_of_stars = 5
for curr_stars in range(1, no_of_stars + 1):
    print("✨" * curr_stars)
```

### Output
```
✨
✨✨
✨✨✨
✨✨✨✨
✨✨✨✨✨
```

## Task 3: Double Player stats
In this task, we aim to double the stats of each player.

### Code Explanation
```python
player_stats = [10, 20, 30]
powered_up_stats = []
for stat in player_stats:
    powered_up_stats.append(stat * 2)

print(powered_up_stats)  # [20, 40, 60]
print(player_stats)  # [10, 20, 30]
```

### Output
```
[20, 40, 60]
[10, 20, 30]
```

## List Comprehension
List comprehension provides a concise way to create lists in Python.

### Code Explanation
```python
powered_up_stats_1 = [stat * 2 for stat in player_stats]
print(powered_up_stats_1)
print(player_stats)
```

### Output
```
[20, 40, 60]
[10, 20, 30]
```

## Task 4: Determine Length of Avengers' Names
In this task, we aim to determine the length of each Avenger's name.

### Code Explanation (for loop)
```python
avengers_name_length = []
for avenger in avengers:
    avengers_name_length.append(len(avenger))
print(avengers_name_length)
```

### Code Explanation (list comprehension)
```python
avengers_nl = [len(avenger) for avenger in avengers]
print(avengers_nl)
```

### Output
```
[4, 8, 11, 15, 10, 4]
```

## Task 5: Select Names Longer than 10 Characters
In this task, we aim to select names of Avengers longer than 10 characters.

### Code Explanation (for loop)
```python
big_names = []
for avenger in avengers:
    if len(avenger) > 10:
        big_names.append(avenger)
print(big_names)
```

### Code Explanation (list comprehension)
```python
big_names_1 = [avenger for avenger in avengers if len(avenger) > 10]
print(big_names_1)
```

### Output
```
['Black widow', 'Captain america']
```

## Conclusion
This Markdown file provides detailed explanations and examples for each code segment, covering concepts such as loops, list comprehension, and code formatting. Understanding these concepts is essential for writing efficient and readable Python code.

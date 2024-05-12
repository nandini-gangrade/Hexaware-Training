### Multiple variable assignment
```python
a = b = c = 10
print(a, b, c)
```

**Explanation**:
- In this code snippet, the value `10` is assigned to variables `a`, `b`, and `c` simultaneously.
- This demonstrates multiple variable assignment in Python.

**Output**:
```
10 10 10
```

## Unpacking / Destructuring
```python
poojitha, shivam, samar = "Black current", "Choco chip", "Butterscotch"

print(poojitha)
print(shivam)
print(samar)

movies = ["Mission Impossible", "JJK", "Avengers Infinity War"]
mathesh, nandhini, devesh = movies
print(mathesh, nandhini, devesh)
```

**Explanation**:
- Unpacking or destructuring allows assigning values from a tuple or list to multiple variables simultaneously.
- Here, values from the tuple are assigned to variables `poojitha`, `shivam`, and `samar`.
- Similarly, values from the list `movies` are assigned to variables `mathesh`, `nandhini`, and `devesh`.

**Output**:
```
Black current
Choco chip
Butterscotch
Mission Impossible JJK Avengers Infinity War
```

### * -> Unpacking operator
```python
t1, t2, *t3 = (100, 200, 300, 400, 60, 40, 30)
print(t1, t2, t3)

t1, t2, *_, t3 = (100, 200, 300, 400, 60, 40, 30)
print(t1, t2, t3)
```

**Explanation**:
- The `*` symbol serves as an unpacking operator in Python.
- It allows assigning remaining values after unpacking to a single variable, or to skip variables using `_`.

**Output**:
```
100 200 [300, 400, 60, 40, 30]
100 200 30
```

## Task 1 - Coordinates and Distance Calculation
```python
coordinates = [(5, 4), (1, 1), (6, 10), (9, 10)]
```
### Using list comprehension
```python
distances = [round((x**2 + y**2) ** 0.5, 2) for x, y in coordinates]
print(distances)
```

**Explanation**:
- This task calculates the distance of each point from the origin using list comprehension.
- It iterates over each coordinate pair, unpacks `x` and `y`, calculates the distance, and appends it to the `distances` list.

**Output**:
```
[6.4, 1.41, 11.66, 13.45]
```

### Copying Lists and Merging
```python
marks1 = [70, 80, 60]
marks2 = [*marks1, 75, 68]
marks3 = [100, 60, *marks1, 75, 68]

print(marks2)
print(marks3)

t1 = [80, 90]
t2 = [50, 60]
t3 = [*t1, *t2]
print(t3)
```

**Explanation**:
- Lists can be copied and merged using list unpacking.
- Here, `marks1` is copied and merged into `marks2` and `marks3`.
- Similarly, `t1` and `t2` are merged into `t3`.

**Output**:
```
[70, 80, 60, 75, 68]
[100, 60, 70, 80, 60, 75, 68]
[80, 90, 50, 60]
```

## Unpacking in Dictionaries
```python
movie = {"name": "John wick", "year": 2014}

mv1 = {**movie, "actor": "Keanu Reeves"}
mv2 = {**movie, "actor": "Keanu Reeves", "year": 2015}
mv3 = {"actor": "Keanu Reeves", "year": 2015, **movie}
print(mv1)
print(mv2)
print(mv3)
```

**Explanation**:
- Unpacking can also be applied to dictionaries to copy or merge dictionaries.
- Here, dictionaries are copied and merged using dictionary unpacking.

**Output**:
```
{'name': 'John wick', 'year': 2014, 'actor': 'Keanu Reeves'}
{'name': 'John wick', 'year': 2015, 'actor': 'Keanu Reeves'}
{'actor': 'Keanu Reeves', 'year': 2015, 'name': 'John wick'}
```

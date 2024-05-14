### Finding Unique Elements in a List
#### Using `.add()`
```python
colors = ["red", "blue", "red", "green", "pink", "blue"]
unique_colors = set()

for color in colors:
    unique_colors.add(color)

print(unique_colors)
```
- **Explanation**: 
  - Here, a set `unique_colors` is initialized to store unique elements.
  - A loop iterates over each element in the `colors` list.
  - Using the `.add()` method, each element is added to the `unique_colors` set.
  - Finally, the set `unique_colors` is printed, containing only the unique elements from the `colors` list.

### Set Comprehension
```python
colors = ["red", "blue", "red", "green", "pink", "blue"]
unique_colors_1 = {clr for clr in colors}
print(unique_colors_1)
```
- **Explanation**: 
  - This is a more concise way to achieve the same result using set comprehension.
  - It iterates over each element in the `colors` list and constructs a set containing unique elements.

### Set Comprehension for Lengths of Words
```python
words = ["This", "is", "cool", "mangoes", "oranges", "apple"]
words_length = {len(word) for word in words}
print(words_length)
```
- **Explanation**: 
  - This demonstrates using set comprehension to create a set containing the lengths of words in the `words` list.
  - It iterates over each word in the `words` list and adds the length of each word to the set `words_length`.

### Dictionary Comprehension
```python
# Squares of numbers from 1 to 20
squares = {x: x**2 for x in range(1, 21)}
print(squares)
```
- **Explanation**: 
  - This showcases dictionary comprehension to create a dictionary containing squares of numbers from 1 to 20.
  - It iterates over each number `x` from 1 to 20 and constructs a dictionary where the key is the number `x` and the value is its square `x**2`.

These examples illustrate how to leverage set and dictionary comprehensions for concise and efficient code, making Python code more readable and expressive.

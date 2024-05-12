# Understanding Book Data Analysis

## Introduction
This Python script analyzes a dataset representing books. Each book is represented as a dictionary containing its title, rating, and genre. The script aims to extract titles of highly rated books, defined as those with a rating of 4.7 or higher.

```python
books = [
    {"title": "Infinite Jest", "rating": 4.5, "genre": "Fiction"},
    {"title": "The Catcher in the Rye", "rating": 3.9, "genre": "Fiction"},
    {"title": "Sapiens", "rating": 4.9, "genre": "History"},
    {"title": "A Brief History of Time", "rating": 4.8, "genre": "Science"},
    {"title": "Clean Code", "rating": 4.7, "genre": "Technology"},
]
```

## Task 1: Highly Rated Books - Using For Loop
The first task employs a traditional approach using a for loop to iterate over each book dictionary in the `books` list. For each book, it checks if the rating is 4.7 or higher and appends the title to the `top_rated_books` list.
```python
top_rated_books = []
for book in books:
    if book["rating"] >= 4.7:
        top_rated_books.append(book["title"])
print(top_rated_books)
```
### Code Explanation
- A new list `top_rated_books` is initialized to store titles of highly rated books.
- A for loop iterates over each book dictionary in the `books` list.
- Inside the loop, it checks if the rating of the current book is 4.7 or higher.
- If the condition is met, it appends the title of the book to the `top_rated_books` list.

### Expected Output
```
['Sapiens', 'A Brief History of Time', 'Clean Code']
```

## Task 2: Highly Rated Books - Using List Comprehension
The second task employs a more concise and pythonic approach using list comprehension. List comprehension allows for a more compact representation of the same logic.
```python
top_rated_books = [book["title"] for book in books if book["rating"] >= 4.7]
print(top_rated_books)
```
### Code Explanation
- List comprehension is used to create a new list `top_rated_books` in a single line.
- It iterates over each book dictionary in the `books` list.
- For each book, it checks if the rating is 4.7 or higher.
- If the condition is met, it extracts the title of the book and adds it to the `top_rated_books` list.

### Expected Output (Same as Task 1)
```
['Sapiens', 'A Brief History of Time', 'Clean Code']
```

## Conclusion
Both approaches achieve the same result, extracting titles of highly rated books. While the for loop approach is more explicit and suitable for beginners, the list comprehension approach offers a more concise and pythonic solution, enhancing readability and reducing code length.

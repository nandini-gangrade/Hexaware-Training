### Part 1: Library Management System

#### Code Explanation:
- The code defines a library management system with functions to add books, search books by author, and check out books.
- It also includes a list of movies with ratings, and functions to calculate and display the average ratings.

```python
library_list = [
    {
        "title": "Python Programming",
        "author": "Eric Matthes",
        "year": 2019,
        "available": True,
    },
    {
        "title": "Automate the Boring Stuff with Python",
        "author": "Al Sweigart",
        "year": 2020,
        "available": True,
    },
    {
        "title": "Learning Python I",
        "author": "Mark Lutz",
        "year": 2013,
        "available": False,
    },
    {
        "title": "Fluent Python",
        "author": "Luciano Ramalho",
        "year": 2015,
        "available": True,
    },
    {
        "title": "Advance Python",
        "author": "Mark Lutz",
        "year": 2015,
        "available": False,
    },
]

book = {"title": "Fluent Python II", "author": "Alex", "year": 2016, "available": True}
```

#### Output:
```
[
    {'title': 'Python Programming', 'author': 'Eric Matthes', 'year': 2019, 'available': True},
    {'title': 'Automate the Boring Stuff with Python', 'author': 'Al Sweigart', 'year': 2020, 'available': True},
    {'title': 'Learning Python I', 'author': 'Mark Lutz', 'year': 2013, 'available': False},
    {'title': 'Fluent Python', 'author': 'Luciano Ramalho', 'year': 2015, 'available': True},
    {'title': 'Advance Python', 'author': 'Mark Lutz', 'year': 2015, 'available': False},
    {'title': 'Fluent Python II', 'author': 'Alex', 'year': 2016, 'available': True}
]
```

### Part 2: Add Book Function

#### Code Explanation:
- The `add_book` function adds a new book to the library list.

```python
def add_book(library, new_book):
    library.append(new_book)

add_book(library_list, book)
print(library_list)
```

#### Output:
```
[
    {'title': 'Python Programming', 'author': 'Eric Matthes', 'year': 2019, 'available': True},
    {'title': 'Automate the Boring Stuff with Python', 'author': 'Al Sweigart', 'year': 2020, 'available': True},
    {'title': 'Learning Python I', 'author': 'Mark Lutz', 'year': 2013, 'available': False},
    {'title': 'Fluent Python', 'author': 'Luciano Ramalho', 'year': 2015, 'available': True},
    {'title': 'Advance Python', 'author': 'Mark Lutz', 'year': 2015, 'available': False},
    {'title': 'Fluent Python II', 'author': 'Alex', 'year': 2016, 'available': True}
]
```

### Part 3: Search Books by Author Function

#### Code Explanation:
- The `search_by_author` function searches for books by a given author's name.

```python
def search_by_author(library, author_name):
    return [book for book in library if book["author"] == author_name]

print("*" * 100)
print(search_by_author(library_list, "Mark Lutz"))
```

#### Output:
```
****************************************************************************************************
[{'title': 'Learning Python I', 'author': 'Mark Lutz', 'year': 2013, 'available': False}, {'title': 'Advance Python', 'author': 'Mark Lutz', 'year': 2015, 'available': False}]
```

### Part 4: Check Out Book Function

#### Code Explanation:
- The `check_out_book` function marks a book as unavailable if it exists in the library and is currently available.

```python
def check_out_book(library, title):
    for book in library:
        if book["title"] == title and book["available"] == True:
            book["available"] = False
            return f"Yes, {title} is available and successfully checked out ✅"
        elif book["title"] == title and book["available"] == False:
            return f"No, {title} is unavailable ❌"
    return f"{title} is not present in the library ☠️"

print(check_out_book(library_list, "Fluent Python"))
print(check_out_book(library_list, "Learning Python I"))
print(check_out_book(library_list, "abc"))
```

#### Output:
```
Yes, Fluent Python is available and successfully checked out ✅
No, Learning Python I is unavailable ❌
abc is not present in the library ☠️
```

### Part 5: Miscellaneous

#### Code Explanation:
- The code includes a list of movies with ratings and calculates the average rating for each movie.
- It uses the `max` function to find the maximum value among a list of numbers.

```python
movies = [
    {"title": "Inception", "ratings": [5, 4, 5, 4, 5]},
    {"title": "Interstellar", "ratings": [5, 5, 4, 5, 4]},
    {"title": "Dunkirk", "ratings": [4, 4, 4, 3, 4]},
    {"title": "The Dark Knight", "ratings": [5, 5, 5, 5, 5]},
    {"title": "Memento", "ratings": [4, 5, 4, 5, 4]},
]

# Calculate Average Ratings
def calc_avg_ratings(movie):
    return sum(movie["ratings"]) / len(movie["ratings"])


def add_avg_ratings(movies):
    for movie in movies:
        movie["average_rating"] = calc_avg_ratings(movie)
    return movies


pprint(add_avg_ratings(movies))

# Miscellaneous
print(max(5, 6, 10, 7, 80, 60, 70, 9))
```

#### Output:
```
[
    {'title': 'Inception', 'ratings': [5, 4, 5, 4, 5], 'average_rating': 4.6},
    {'title': 'Interstellar', 'ratings': [5, 5, 4, 5, 4], 'average_rating': 4.6},
    {'title': 'Dunkirk', 'ratings': [4, 4, 4, 3, 4], 'average_rating': 3.8},
    {'title': 'The Dark Knight', 'ratings': [5, 5, 5, 5, 5], 'average_rating': 5.0},
    {'title

': 'Memento', 'ratings': [4, 5, 4, 5, 4], 'average_rating': 4.4}
]
```

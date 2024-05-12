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

<br>

# DAY10 : Dict Exercise

## Updating Employee Experiences and Determining Status

```python
employees = [
    {"name": "Sneha", "experience": 2},
    {"name": "Manju"},
    {"name": "Sai Subash", "experience": 4},
    {"name": "Manasa"},
]
```

### Task 1: Update Employee Experiences
```python
for employee in employees:
    employee["experience"] = employee.get("experience", 0) + 1

print(employees)

# Output:
# [
#     {"name": "Sneha", "experience": 3},
#     {"name": "Manju", "experience": 1},
#     {"name": "Sai Subash", "experience": 5},
#     {"name": "Manasa", "experience": 1},
# ]
```
In this task, we iterate through each employee in the `employees` list. For each employee, we use the `.get()` method to retrieve their current experience. If the experience is not present (`None`), we default it to 0. Then, we increment the experience by 1 and update the employee's dictionary with the new experience value. Finally, we print the modified `employees` list, showing the updated experience for each employee.

### Task 2: Determine Employee Status
```python
for employee in employees:
    employee["experience"] = employee.get("experience", 0) + 1

    if employee["experience"] >= 5:
        employee["status"] = "Senior"
    elif 3 <= employee["experience"] < 5:
        employee["status"] = "Mid-Level"
    else:
        employee["status"] = "Junior"

print(employees)

# Output:
# [
#     {"name": "Sneha", "experience": 3, "status": "Mid-Level"},
#     {"name": "Manju", "experience": 1, "status": "Junior"},
#     {"name": "Sai Subash", "experience": 5, "status": "Senior"},
#     {"name": "Manasa", "experience": 1, "status": "Junior"},
# ]

```
Here, we again iterate through each employee in the `employees` list. Similar to Task 1, we update each employee's experience by 1. After that, we use conditional statements to determine the status of each employee based on their experience level:
- If an employee has 5 or more years of experience, they are labeled as "Senior".
- If an employee has between 3 and 5 years of experience, they are labeled as "Mid-Level".
- Otherwise, if an employee has less than 3 years of experience, they are labeled as "Junior".
We update the `status` key in each employee's dictionary accordingly. Finally, we print the modified `employees` list, which now includes the status of each employee.

> These tasks demonstrate how to update and manipulate dictionaries within a list comprehensively, ensuring that each employee's information is correctly updated and labeled according to their experience level.

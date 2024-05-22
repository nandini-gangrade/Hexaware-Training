# Control Flow in Python

Control flow statements like `break` and `continue` are essential for managing the execution of loops. Multiline strings allow you to include longer text blocks in your code. This guide explains these concepts and provides examples.

## `break` and `continue` Statements

### `break` Statement

The `break` statement terminates the loop immediately and exits the loop.

#### Example: Print Numbers Until 5
```python
for i in range(1, 10):
    if i == 6:
        break
    print(i)
```
- **Explanation**: The loop iterates from 1 to 9, but it stops when `i` equals 6, so it prints numbers from 1 to 5.

### `continue` Statement

The `continue` statement skips the current iteration and moves to the next iteration of the loop.

#### Example: Print Odd Numbers
```python
for i in range(1, 10):
    if i % 2 == 0:
        continue
    print(i)
```
- **Explanation**: The loop iterates from 1 to 9, but it skips even numbers, so it prints only the odd numbers (1, 3, 5, 7, 9).

## Task Examples

### Task 1: Find the First Negative Value
```python
def first_negative(l):
    for i in l:
        if i < 0:
            print(i)
            break
```
- **Explanation**: This function iterates through the list `l` and prints the first negative value it encounters, then stops further iteration.

### Task 2: Process Until Duplicate
```python
def process_until_duplicate(s):
    set1 = set()
    for i in s:
        if i in set1:
            print("Duplicate is Found")
            break
        else:
            set1.add(i)
            print(f"Processed {i}")
```
- **Explanation**: This function processes each item in the list `s`. If it finds a duplicate item, it prints a message and stops processing further.

### Task 3: Censorship Bot
```python
def censorship_bot(messages, banned_words):
    messages2 = set()
    for message in messages:
        for word in banned_words:
            if word in message:
                break
        else:
            messages2.add(f"Approved Message: {message}")
    print(list(messages2))
```
- **Explanation**: This function checks each message against a list of banned words. If a banned word is found in the message, it skips to the next message. Otherwise, it adds the message to the approved list.

#### Example Messages and Banned Words
```python
messages = [
    "Hello everyone!",
    "This is a bad word example!",
    "Let's keep our chat clean!",
    "Oops another bad content!",
    "Have a nice day!"
]

banned_words = ["bad", "oops"]

# Expected output:
# Approved message: Hello everyone!
# Approved message: Let's keep our chat clean!
# Approved message: Have a nice day!

if __name__ == '__main__':
    process_until_duplicate(["apple", "banana", "carrot", "apple", "date", "banana"])
    censorship_bot(messages, banned_words)
```

## Summary

- **`break`**: Stops the loop immediately.
- **`continue`**: Skips the current iteration and proceeds to the next iteration.


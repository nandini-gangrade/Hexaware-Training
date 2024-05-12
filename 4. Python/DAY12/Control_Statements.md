# Introduction to Control Statements

Control statements in Python allow you to alter the flow of execution in your program based on certain conditions. They include `break`, `continue`, and `return`, each serving a different purpose.

## break Statement
The `break` statement is used to terminate the execution of a loop prematurely. It allows you to exit the loop based on a specific condition.

## continue Statement
The `continue` statement is used to skip the remaining code inside a loop for the current iteration and move to the next iteration. It is useful when you want to skip certain iterations based on a condition.

## return Statement
The `return` statement is used to exit a function and return a value. It allows you to pass back a value from a function to the caller.

<br>

```python
def print_nums():
    for num in range(1, 10):
        if num == 6:
            break  # Exit the loop when num equals 6

        print(num)
    print("Execution continues 🎊")  # Execution continues after the loop


def skip_even():
    for num in range(1, 10):
        if num % 2 == 0:
            continue  # Skip even numbers
        print(num)
    print("Execution continues 🎊")  # Execution continues after the loop


# Task 1: Find the first negative value
def first_negative(numbers):
    result = "No negative number is in the list"
    for num in numbers:
        if num < 0:
            result = f"The first negative number is {num}"
            break  # Exit loop when the first negative number is found
    return result

if __name__ == "__main__":
    # print_nums()
    # skip_even()
    # Test case
    print(first_negative([3, 5, 7, -1, 9, -3]))  # Output: The first negative number is -1


def process_until_duplicate(fruits):
    fruitSet = set()
    for fruit in fruits:
        if fruit in fruitSet:
            print(f"Already Processed {fruit}")
            break  # Exit loop when a duplicate fruit is found
        else:
            fruitSet.add(fruit)
            print(f"Processed {fruit}")

if __name__ == "__main__":
    # print_nums()
    # skip_even()
    # Test case
    # print(first_negative([3, 5, 7, -1, 9, -3]))  # Output: -1
    process_until_duplicate(["apple", "banana", "carrot", "apple", "date", "banana"])


# Task 3: Censorship Bot
def censorship_bot(messages, banned_words):
    censored_messages = []
    x, y = banned_words  # Extracting the banned words
    for message in messages:
        message = message.split()
        if x in message or y in message:
            continue  # Skip messages containing banned words
        message = " ".join(message)
        censored_messages.append(message)
    return censored_messages

# Sample Messages and Banned Words
messages = [
    "Hello everyone!",
    "This is a bad word example!",
    "Let's keep our chat clean!",
    "Oops another bad content!",
    "Have a nice day!",
    "Tumbad is a nice movie"
]
banned_words = ["bad", "oops"]

print(censorship_bot(messages, banned_words))
```

### Expected Output:
```bash
['Hello everyone!', "Let's keep our chat clean!", 'Have a nice day!', 'Tumbad is a nice movie']
```

This script demonstrates the usage of `break`, `continue`, and `return` statements within various contexts, along with their generated output.

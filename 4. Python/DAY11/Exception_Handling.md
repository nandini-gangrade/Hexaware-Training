# Explanation of Exception Handling in Python

## Overview
Exception handling in Python allows you to deal with errors or exceptional situations that may occur during the execution of a program. It provides a structured way to manage errors and prevent them from causing the program to crash.

## Syntax
The basic syntax for exception handling in Python involves the `try`, `except`, `else`, and `finally` blocks.

### try block
The `try` block is used to enclose the code that might raise an exception. If an exception occurs within this block, Python searches for an appropriate `except` block to handle it.

### except block
The `except` block catches and handles exceptions raised in the corresponding `try` block. You can specify the type of exception to catch, or you can use a generic `except` block to catch all types of exceptions.

### else block
The `else` block is executed if no exceptions occur in the preceding `try` block. It is usually used to execute code that should run only if the `try` block does not raise an exception.

### finally block
The `finally` block is optional and is always executed, regardless of whether an exception occurred or not. It is typically used to perform cleanup tasks, such as closing files or releasing resources.

```python
from datetime import datetime
```

## Example
```python
# Compile-time error (Syntax error)
def math_divide(n1, n2):
    try:
        result = n1 / n2
        return result
    except:
        return "Oops. 🤭 An Error happened"
```
In this example, a function `math_divide` is defined to perform division. However, it contains a syntax error (`n1 / n2`) that would cause a runtime error if executed. This is an example of a compile-time error that can be caught during development.

### Output:

## Types of Errors
There are various types of errors that can occur during program execution. Some common types include:
- `SyntaxError`: Occurs due to invalid syntax in the code.
- `NameError`: Raised when a variable or function name is not found.
- `TypeError`: Occurs when an operation is performed on an object of inappropriate type.
- `ValueError`: Raised when a function receives an argument of correct type but with an inappropriate value.
- `ZeroDivisionError`: Raised when division or modulo by zero is performed.

## Custom Exceptions
Python allows you to define custom exception classes by subclassing from the built-in `Exception` class. Custom exceptions can be raised and caught just like built-in exceptions, allowing you to create more meaningful error messages and handle specific error conditions in your code.

## Best Practices
- Use specific `except` blocks to catch different types of exceptions.
- Handle exceptions gracefully by providing meaningful error messages or taking appropriate corrective actions.
- Use the `finally` block for cleanup tasks that should always be performed, such as closing files or releasing resources.
- Avoid catching generic exceptions (`except:`) unless necessary, as it may hide unexpected errors in your code.
- Use custom exceptions to handle application-specific error conditions and improve code readability.

```python
from datetime import datetime

# Compile-time error (Syntax error)
def math_divide(n1, n2):
    try:
        result = n1 / n2  # Attempt division
        return result
    except:
        return "Oops. 🤭 An Error happened"  # Handle any exception with a generic message
```

```
# Errors
# 1. try: Attempts the code block that might raise an exception.
# 2. except: Catches and handles exceptions raised in the try block.
# 3. else: Executed if no exceptions occur in the preceding try block.
# 4. finally: Optional block that is always executed, regardless of whether an exception occurred or not.
```

```python
def divide_eggs(n1, n2):
    try:
        # Business logic error
        if n1 < 0:
            # Raise error for negative number of eggs
            raise ValueError("Eggs cannot be negative 🤭")
        if n2 < 0:
            # Raise error for negative number of people
            raise ValueError("People cannot be negative 🤭")

        # Code is shield 🛡️
        result = n1 / n2  # Attempt division

    # Specific message
    except ZeroDivisionError:
        return "You cannot divide by zero! 💀"  # Handle division by zero error
    except ValueError as e:
        return f"Invalid number: {e}"  # Handle ValueError with specific message
    else:
        # When no error
        print("Division was successful ✅")  # Print success message when no error occurs
    finally:
        # No matter what, always execute this block
        print("Operation done 😊✌️")  # Print message indicating operation completion

    return result
```

### Output:
```
Operation done 😊✌️
Operation done 😊✌️
Operation done 😊✌️
You cannot divide by zero! 💀
Operation done 😊✌️
```

## Task 1: Handling string in birth_year
```python
# Calculate age & Handle errors
def calculate_age():
    try:
        current_year = datetime.now().year
        birth_year = input("Please provide your birth year: ")  # Prompt user for birth year

        age = current_year - int(birth_year)  # Calculate age
        print(f"Your age is {age}")  # Print user's age
    except ValueError as err:
        print("Invalid number: ", err)  # Handle ValueError by printing error message
```

### Output:
(No specific output example provided as it depends on user input)

## Task 2: -ve value, future years (Logical Errors)
```python
def calculate_age():
    try:
        current_year = datetime.now().year
        birth_year = int(input("Please provide your birth year: "))  # Runtime error

        if birth_year < 0:
            # Handling logical error for negative birth year
            raise ValueError("Year cannot be negative")
        if birth_year > current_year:
            # Handling logical error for future birth year
            raise ValueError("You're not flash to be from the future ⚡")

        age = current_year - birth_year  # Calculate age
        print(f"Your age is {age}")  # Print user's age
    except ValueError as err:
        print("Invalid number: ", err)  # Handle ValueError by printing error message
    except Exception as err:
        print("This catch all!", err)  # Catch any other exceptions and print error message
```

```python
def main():
    # Runtime error
    print(divide_eggs(10, -5))
    print(divide_eggs(-10, 5))
    print(divide_eggs(10, 5))
    print(divide_eggs(10, 0))  # Execution stops due to division by zero
    print(divide_eggs(15, 3))
    print(datetime.now().weekday())
    print(datetime.now().day)
```

### Output:
```
Operation done 😊✌️
Operation done 😊✌️
Operation done 😊✌️
You cannot divide by zero! 💀
Operation done 😊✌️
```

### Every has the same base class -> Exception
```python
class NegativeNumberError(Exception):
    def __init__(self, value):
        self.value = value
        self.message = "Negative numbers are not allowed"
        super().__init__(self.message)

    # Overriding Base class __str__
    def __str__(self):
        return f"{self.value} -> {self.message}"
```

### Create your own Error Class
```python
def only_positive_num():
    try:
        x = -10
        if x < 0:
            raise NegativeNumberError(x)  # Raise custom exception for negative number
    except NegativeNumberError as err:
        print(err)  # Print custom exception message


if __name__ == "__main__":
   

 only_positive_num()  # Call function to demonstrate custom exception handling
```

### Output:
```
-10 -> Negative numbers are not allowed
```

In this way, each part of the code is explained with comments added directly within the code itself.

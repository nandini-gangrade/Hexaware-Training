
## Conditionals

### Age Comparison Program

This Python code prompts the user to enter the ages of two individuals, A and B. It then compares their ages and prints a message indicating which person is older, or if they are of the same age.

```python
a = int(input("Enter A's age: "))
b = int(input("Enter B's age: "))

if a > b:
    print("A is older")
elif a == b:
    print("Both are of the same age")
else:
    print("B is older")
```

### Relational Operators

This code snippet demonstrates the use of relational operators (`>`, `<`, `>=`, `<=`, `==`, `!=`) in Python. It compares the numbers 174 and 111111 and prints `True` if the comparison is true, otherwise prints `False`.

```python
if 174 > 111111:
    print("True")
else:
    print("False")
```

### Task 1: Flavour Check

In this task, the user is asked to input their favorite flavor. The code then checks if the flavor is in stock (`vanilla`, `lime`, `chocolate`). If the flavor is in stock, it prints "Yes, we do have it"; otherwise, it prints "No, we ran out of stock".

```python
stock1 = "vanilla"
stock2 = "lime"
stock3 = "chocolate"

c = input("Enter your favorite flavor: ")

if c == stock1 or c == stock2 or c == stock3:
    print("Yes, we do have it")
else:
    print("No, we ran out of stock")
```

### Ternary Operator

The ternary operator `x if condition else y` is a concise way to express conditional statements. Here, it's used to print different messages based on whether the user's favorite flavor is in stock.

```python
print("Yes, we do have it!" if c in (stock1, stock2, stock3) else "No, we ran out of stock.")
```

### Code Debt

Code debt refers to the accumulation of technical debt in software development, often resulting from taking shortcuts or implementing temporary solutions. It can lead to decreased code quality and increased difficulty in maintaining, extending, and testing the codebase.

### 5 Factors of Code Quality:
1. **Readability**: Code should be easy to read and understand.
2. **Maintainability**: Code should be easy to modify and update.
3. **Extensibility**: Code should be designed to support future enhancements and new features.
4. **Testability**: Code should be written in a way that facilitates testing, ensuring that potential issues can be detected and addressed effectively.
5. **Performance**: Code should be efficient in terms of execution time and resource usage.

------------------------

## String Methods

### Slicing:
- Slicing is a technique used to extract a portion of a string based on specified indices.
- In Python, slicing syntax is `[start:stop:step]`, where `start` is the starting index, `stop` is the stopping index (exclusive), and `step` is the step size.

```python
# Initializing the variable with the quote
quote = "Dream is something "

# Printing substring from index 1 to 3 (excluding 3)
# Output: "re"
# Reason: Slicing starts from index 1 ('r') and ends at index 3 ('e'), but 'e' is excluded from the result.
print("Substring from index 1 to 3:", quote[1:3])

# Printing the last character of the string
# Output: " "
# Reason: Negative indexing allows accessing characters from the end of the string. '-1' refers to the last character.
print("Last character of the string:", quote[-1])

# Printing substring from the fourth character from the end to the second character from the end (excluding the second character from the end)
# Output: "hin"
# Reason: Negative indexing is used to access characters from the end of the string. '-4' refers to the fourth character from the end, and '-1' refers to the second character from the end. The substring includes characters from '-4' up to, but not including, '-1'.
print("Substring from the fourth character from the end to the second character from the end:", quote[-4:-1])

# Printing characters from index 1 to 10 (excluding 10) with a step of 2
# Output: "rmisos"
# Reason: Slicing starts from index 1 ('r') and ends at index 10 ('g'), but 'g' is excluded from the result. A step of 2 is used, so every second character within the specified range is included in the output.
print("Characters from index 1 to 10 with a step of 2:", quote[1:10:2])

# Printing the string in reverse order
# Output: " gnihtemos si maerD"
# Reason: Negative step (-1) is used, which iterates over the string in reverse order.
print("String in reverse order:", quote[::-1])

# Printing substring from the last character to the fourth character from the end (excluding the fourth character from the end) in reverse order
# Output: "gni"
# Reason: Negative indexing is used to access characters from the end of the string. '-1' refers to the last character, and '-4' refers to the fourth character from the end. The substring is printed in reverse order.
print("Substring from the last character to the fourth character from the end in reverse order:", quote[-1:-4:-1])
```

```python
msg = "Hi, all"
print(msg[0:2])  # Output: "Hi"
```

### Case Methods:
- Case methods are used to change the case of characters in a string.
- They include `upper()`, `lower()`, `title()`, and `capitalize()` methods.

```python
print(msg.upper())     # Output: "HI, ALL"
print(msg.lower())     # Output: "hi, all"
print(msg.title())     # Output: "Hi, All"
print(msg.capitalize())# Output: "Hi, all"
```

### Quote Handling:
- `strip()`, `lstrip()`, and `rstrip()` methods are used to remove leading and trailing characters from a string.
- These methods are helpful for cleaning up whitespace or other characters from strings.

```python
quote = "      Dream is not something that you see in sleep, Dream is something that does not let you sleep"
print(quote.strip())  # Output: "Dream is not something that you see in sleep, Dream is something that does not let you sleep"

quote1 = "----Dream is not something-that you see in sleep, Dream is something that does not let you sleep----"
print(quote1.strip("-"))  # Output: "Dream is not something-that you see in sleep, Dream is something that does not let you sleep"
print(quote1.lstrip("-")) # Output: "Dream is not something-that you see in sleep, Dream is something that does not let you sleep----"
print(quote1.rstrip("-")) # Output: "----Dream is not something-that you see in sleep, Dream is something that does not let you sleep"

quote3 = "Dream is not something that you see in sleep, Dream is something that does not let you sleep"
print(quote3.replace("Dream","🤦‍♀️")) # Output: "🤦‍♀️ is not something that you see in sleep, 🤦‍♀️ is something that does not let you sleep"
print(quote3)  # Output: "Dream is not something that you see in sleep, Dream is something that does not let you sleep"
```

----------

## Exercise

```python
# After the 🔑

# Initializing variables with secret message and code
message = "    🚨🔍📱🔑secret_code✌️"  # The original message containing the secret code
code = "SECRET_CODE✌️"  # The secret code to match against

# To decode the secret message, we need to skip the emojis at the beginning and compare the remaining substring with the provided code.

# Output: "you are an hacker" (if matched)
#         "Try again" (if not matched)

# Extracting the substring after the '🔑' and converting to lowercase for case-insensitive comparison
# Usage of the 'split' method: It splits the string based on the provided delimiter (in this case, "🔑") and returns a list of substrings.
# Here, message.split("🔑") returns ['    🚨🔍📱', 'secret_code✌️'].
# We select the second element (index 1) of the list, which contains the secret message.
# Usage of the 'lower' method: It converts the string to lowercase to ensure case-insensitive comparison.
# The final value of 'secret' is the lowercase version of the secret message.
secret = message.split("🔑")[1].lower()

# Using a ternary operator to compare the secret message and the code
# Usage of the ternary operator: It provides a concise way to write conditional expressions in a single line.
# Syntax: <expression_if_true> if <condition> else <expression_if_false>
# In this case, if the secret message matches the code (ignoring letter casing), it prints "you are an hacker"; otherwise, it prints "Try again".
output = "you are an hacker" if secret == code.lower() else "Try again"

# Outputting the final result
print("Final Output:", output)

```

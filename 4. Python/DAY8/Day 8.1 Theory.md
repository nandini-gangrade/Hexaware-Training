## Intro to Python

| Feature            | Description                                                                                                                                                          |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Inventor          | Guido van Rossum, a Dutch programmer, created Python in the late 1980s. He named the language after the British comedy show "Monty Python's Flying Circus," showing his appreciation for its humor and to make the name memorable. |
| BDFL              | Guido van Rossum was affectionately known as Python's "Benevolent Dictator For Life" (BDFL) due to his influential leadership and decision-making role in the Python community.                                                 |
| High-level        | Python is designed to be easy to read and write, with a syntax that resembles natural language, making it accessible to beginners and experts alike.              |
| Interpreted        | Python code is executed line by line by an interpreter, which means you can run your code without needing to compile it first, making the development process faster.  |
| General-purpose   | Python is a versatile language that can be used for a wide range of applications, including web development, data analysis, scientific computing, automation, and more. |
| Dynamically-typed | Python is dynamically-typed, meaning you don't need to declare the type of a variable explicitly. Instead, Python infers the type of variables based on the assigned value. |
| Object-oriented   | Python supports object-oriented programming paradigms, allowing developers to create classes and objects, encapsulate data, and implement inheritance and polymorphism. |
| Extensive libraries | Python has a vast ecosystem of libraries and frameworks that provide pre-written code for various tasks, saving time and effort in development.                           |
| Community-driven  | Python has a large and active community of developers who contribute to its growth and provide support through forums, tutorials, and open-source projects.                |
| Portable          | Python code can run on different operating systems, including Windows, macOS, and Linux, making it portable and platform-independent.                                     |
| Scalable          | Python is scalable, meaning it can be used for small scripts as well as large-scale applications, thanks to its performance optimizations and support for parallelism.       |
| Language Diversity | Despite Python's popularity and versatility, other programming languages exist to address specific needs, preferences, and technical requirements. Different languages may offer better performance, lower-level system access, stronger static typing, or specialized domain-specific features. Additionally, historical factors, community preferences, and evolving technology trends contribute to the continued development and adoption of new programming languages. |


## Python's design philosophy

| Design Philosophy Point  | Main Description                                                                                                                                                               |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Successor to ABC Language | Python aimed to build upon the ideas of the ABC language, aiming to appeal to Unix/C hackers by providing a language that is both powerful and easy to use.                   |
| Readability and Simplicity ("Pythonic" code) | Python prioritizes readability and simplicity in code, encouraging developers to write code that is easy to understand and maintain. This philosophy is sometimes referred to as writing "Pythonic" code. |
| Concise Syntax            | Python's syntax allows developers to express concepts in fewer lines of code compared to other languages. This leads to more concise and expressive programs, improving readability and reducing complexity.                 |

These points encapsulate Guido van Rossum's vision for Python and highlight its key principles of simplicity, readability, and expressiveness.

## Milestone

| Milestone                           | Description                                                                                                                                                                                                                                                                                               |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Python 2.0 (2000)                  | Introduced list comprehensions and garbage collection (GC).                                                                                                                                                                                                                                              |
| Python 3 (2008)                    | Major revision with emphasis on Unicode support, not fully backward compatible with Python 2.                                                                                                                                                                                                              |

**Python 2.0 (2000)**
- *Introduced list comprehensions*: List comprehensions provide a concise and expressive way to create lists in Python. Instead of writing multiple lines of code to create and populate a list, developers can use a single line of code, improving readability and reducing code verbosity.
- *Garbage collection (GC)*: Garbage collection is a memory management technique that automatically deallocates memory that is no longer in use, preventing memory leaks and improving overall memory efficiency. Python 2.0 introduced garbage collection to automate memory management tasks, reducing the burden on developers and improving the reliability of Python programs.

**Python 3 (2008)**
- *Major revision*: Python 3 was a significant update to the language, addressing various design flaws and inconsistencies present in Python 2. It introduced several new features and improvements aimed at making Python a more robust and modern programming language.
- *Emphasis on Unicode support*: Python 3 placed a strong emphasis on Unicode support, making it easier to work with international text and characters. Unicode support ensures that Python can handle a wide range of characters and symbols from different languages and writing systems, improving compatibility and usability for global audiences.
- *Not fully backward compatible with Python 2*: While Python 3 brought many enhancements, it also introduced changes that were not backward compatible with Python 2. This meant that existing Python 2 codebases required modifications to work with Python 3, leading to challenges and slower adoption initially. However, the benefits of Python 3, such as improved Unicode support and language consistency, ultimately outweighed the migration challenges, leading to widespread adoption over time.


## Python 3 Transition

| Transition Stage       | Description                                                                                                                                                                                                                                                |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Addressing Design Flaws and Enhancements | - Python 3 addressed fundamental design flaws in Python 2. <br>- Introduced improvements and new features. <br>- Emphasized Unicode support for better handling of international text. <br>- Enhanced syntax and language refinements for improved readability and maintainability. |
| Community Adoption     | - Transition to Python 3 was gradual. <br>- Community gradually embraced Python 3 supported by its enhancements. <br>- Active contribution from the Python community to update libraries and frameworks for Python 3 compatibility.                                        |
| Official End of Python 2 Support       | - Python 2 support officially ended in 2020. <br>- Deadline accelerated migration to Python 3. <br>- Developers encouraged to update codebases for continued updates, security patches, and community support.                                                           |

These points succinctly describe the Python 3 transition process, covering the reasons for transition, community involvement, and the impact of the official end of Python 2 support.


## Differences between declaration and assignment

| Aspect        | Declaration                                                                                                                                                                    | Assignment                                                                                                                                |
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Definition    | Declaration introduces the existence of a variable to the compiler/interpreter without allocating memory or assigning a value.                                               | Assignment assigns a value to a variable, allocating memory if necessary.                                                                |
| Example       | ```python int num;``` (declares a variable named "num" of type integer in languages like C/C++)                                                                                | ```python num = 10;``` (assigns the value 10 to the variable "num" in Python)                                                            |
| Purpose       | Allows the compiler/interpreter to recognize the variable's name and type for subsequent use in the program.                                                                  | Assigns a value to a variable, allowing it to hold data that can be manipulated or referenced throughout the program.                    |
| Memory Usage  | Does not allocate memory.                                                                                                                                                      | Allocates memory to store the assigned value.                                                                                            |
| Usage         | Necessary in statically-typed languages like C/C++ where variable types must be explicitly declared before use. Not required in dynamically-typed languages like Python. | Essential in all programming languages to store data and perform operations on variables.                                               |


## Type conversion with examples for different data types:

| Data Type          | Example                              | Description                                                                                                                                                      |
|--------------------|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Integer to Float  | `int_num = 10`<br>`float_num = float(int_num)` | Converts an integer to a floating-point number, preserving the integer value and adding a decimal point.                                                      |
| Float to Integer  | `float_num = 10.5`<br>`int_num = int(float_num)` | Converts a floating-point number to an integer, truncating the decimal part and keeping only the integer portion.                                             |
| Integer to String | `int_num = 10`<br>`str_num = str(int_num)`     | Converts an integer to a string, representing the numerical value as a sequence of characters.                                                                |
| Float to String   | `float_num = 10.5`<br>`str_num = str(float_num)` | Converts a floating-point number to a string, representing the numerical value as a sequence of characters.                                                  |
| String to Integer | `str_num = "10"`<br>`int_num = int(str_num)`     | Converts a string containing digits to an integer, extracting and converting the numerical value represented by the characters.                                |
| String to Float   | `str_num = "10.5"`<br>`float_num = float(str_num)` | Converts a string representing a floating-point number to a float, extracting and converting the numerical value represented by the characters, including the decimal point. |
| Boolean to Integer | `bool_val = True`<br>`int_val = int(bool_val)`   | Converts a boolean value to an integer, where `True` is converted to `1` and `False` is converted to `0`.                                                     |
| Integer to Boolean | `int_val = 1`<br>`bool_val = bool(int_val)`     | Converts an integer to a boolean value, where `0` is converted to `False`, and any non-zero value is converted to `True`.                                      |

These examples demonstrate how different data types can be converted to one another in Python. Type conversion is a common operation in programming, allowing flexibility and compatibility between different types of data.


## Difference between implicit and explicit type conversion

**Implicit Type Conversion:**

In implicit type conversion, the Python interpreter automatically converts one data type to another when required. This conversion occurs when data types are compatible, and one type can be safely promoted to another without losing information.

| Conversion Type          | Description                                                                                                                                                        | Example                                                                                                                                                     |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Float to Integer        | Converts a floating-point number to an integer by truncating the decimal part.                                                                                     | `float_num = 10.5`<br>`int_num = float_num`<br>`print(int_num)`<br>Output: `10`                                                                         |
| Integer to Float        | Converts an integer to a floating-point number, adding a decimal point to represent the fractional part.                                                           | `int_num = 10`<br>`float_num = int_num`<br>`print(float_num)`<br>Output: `10.0`                                                                       |
| String to Integer/Float | Converts a string representing a numerical value to an integer or a float.                                                                                         | `num_str = "10"`<br>`num_int = num_str`<br>`num_float = num_str`<br>`print(num_int)`<br>Output: `10`<br>`print(num_float)`<br>Output: `10.0` |
| Boolean to Integer/Float | Converts a boolean value (`True` or `False`) to an integer or a float, where `True` is converted to `1` and `False` is converted to `0`.                             | `bool_val = True`<br>`int_val = bool_val`<br>`float_val = bool_val`<br>`print(int_val)`<br>Output: `1`<br>`print(float_val)`<br>Output: `1.0` |

**Explicit Type Conversion (Type Casting):**

In explicit type conversion, the user explicitly converts the data type of an object to the required data type using predefined functions like `int()`, `float()`, `str()`, etc.

| Conversion Type          | Description                                                                                                                                                 | Example                                                                                                                     |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| String to Integer/Float | Converts a string representing a numerical value to an integer or a float using predefined functions like `int()` or `float()`.                              | `num_str = "10"`<br>`num_int = int(num_str)`<br>`num_float = float(num_str)`<br>`print(num_int)`<br>Output: `10`<br>`print(num_float)`<br>Output: `10.0` |
| Integer/Float to String | Converts an integer or a float to a string using predefined function `str()`.                                                                               | `int_num = 10`<br>`float_num = 10.5`<br>`str_num_int = str(int_num)`<br>`str_num_float = str(float_num)`<br>`print(str_num_int)`<br>Output: `"10"`<br>`print(str_num_float)`<br>Output: `"10.5"` |
| Boolean to Integer/Float | Converts a boolean value (`True` or `False`) to an integer or a float explicitly using `int()` or `float()` functions.                           | `bool_val = True`<br>`int_val = int(bool_val)`<br>`float_val = float(bool_val)`<br>`print(int_val)`<br>Output: `1`<br>`print(float_val)`<br>Output: `1.0` |


## Data Type

| Data Type | Description                                                 | Example                   |
|-----------|-------------------------------------------------------------|---------------------------|
| int       | Integer: whole numbers without any decimal points          | `x = 10`                  |
| float     | Float: numbers with a decimal point                        | `y = 10.5`                |
| complex   | Complex: numbers with a real and imaginary part            | `z = 5 + 2j`              |
| str       | String: ordered sequence of characters enclosed in quotes  | `text = "Hello, World!"`  |
| bool      | Boolean: represents truth values True or False             | `is_true = True`          |
| list      | List: ordered, mutable collection of items                 | `numbers = [1, 2, 3]`     |
| tuple     | Tuple: ordered, immutable collection of items              | `coordinates = (10, 20)`  |
| dict      | Dictionary: collection of key-value pairs                  | `person = {'name': 'John', 'age': 30}` |
| set       | Set: unordered collection of unique items                  | `unique_numbers = {1, 2, 3}` |
| frozenset | Frozenset: immutable set                                    | `frozen_numbers = frozenset({1, 2, 3})` |
| bytes     | Bytes: immutable sequence of bytes                         | `binary_data = b'hello'`  |
| bytearray | Bytearray: mutable sequence of bytes                       | `byte_data = bytearray(b'hello')` |
| None      | None: represents the absence of a value                    | `x = None`                |


## Taking Input From User

| Scenario                                           | Code Example                                        |
|----------------------------------------------------|-----------------------------------------------------|
| Taking input as integer                           | ```python x = int(input("Enter an integer: "))```  |
| Taking input as float                             | ```python y = float(input("Enter a float: "))```   |
| Taking input as string                            | ```python text = input("Enter a string: ")```      |
| Taking multiple inputs separated by whitespace    | ```python numbers = input("Enter numbers: ").split()``` |
| Taking multiple integer inputs separated by space | ```python integers = map(int, input("Enter integers separated by space: ").split())``` |
| Taking input with a prompt message                | ```python name = input("Enter your name: ")```     |
| Taking input without any prompt message           | ```python x = input()```                           |


## Formatted String

| Scenario                                   | Code Example                                                                      | Description                                                                                                                                                           |
|--------------------------------------------|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Basic formatted string (f-string)         | ```python name = "Alice"```<br>```python age = 30```<br>```python print(f"My name is {name} and I am {age} years old.")``` | Using f-string to insert variables directly into a string.                                                                                                           |
| Arithmetic operations in f-string          | ```python num1 = 10```<br>```python num2 = 5```<br>```python print(f"The sum of {num1} and {num2} is {num1 + num2}.")```    | Performing arithmetic operations inside an f-string.                                                                                                                 |
| Formatted string with function call        | ```python def greet(name):```<br>```python     return f"Hello, {name}!"```<br>```python print(greet("Bob"))```                 | Calling a function inside an f-string to generate formatted output.                                                                                                   |
| Accessing attributes with f-string         | ```python class Person:```<br>```python     def __init__(self, name, age):```<br>```python         self.name = name```<br>```python         self.age = age```<br>```python person = Person("Alice", 30)```<br>```python print(f"Name: {person.name}, Age: {person.age}")``` | Accessing attributes of an object using dot notation within an f-string.                                                                                               |
| Nesting f-strings within f-strings        | ```python name = "Alice"```<br>```python age = 30```<br>```python print(f"Hello, {name.upper()}! You are {age} years old.")```    | Embedding one f-string inside another f-string to perform additional formatting or operations.                                                                         |
| Formatting numbers with f-string          | ```python pi = 3.14159```<br>```python print(f"The value of pi is {pi:.2f}.")```  | Formatting numerical values with specified precision using f-string's format specifier.                                                                               |
| Using expressions with f-string            | ```python num1 = 10```<br>```python num2 = 5```<br>```python print(f"The sum of {num1} and {num2} is {num1 + num2}.")```    | Using expressions directly inside an f-string to compute values or perform operations.                                                                                  |
| Formatted string with str.format() method | ```python name = "Alice"```<br>```python age = 30```<br>```python print("My name is {} and I am {} years old.".format(name, age))``` | Using `str.format()` method to insert variables into a string.                                                                                                         |
| Formatted string with % operator          | ```python name = "Alice"```<br>```python age = 30```<br>```python print("My name is %s and I am %d years old." % (name, age))```       | Using `%` operator for string formatting where `%s` represents a string and `%d` represents an integer placeholder.                                                  |

**Explanation:**

In simple terms, interpolation means putting something in the middle of something else. In Python, f-strings allow us to easily insert variables, expressions, or even function calls into a string. Think of f-strings as templates with placeholders (`{}`) that get replaced with the actual values when the code runs.

For instance, in the "Basic formatted string" scenario, the f-string `f"My name is {name} and I am {age} years old."` contains placeholders `{name}` and `{age}`. When the code is executed, these placeholders are replaced with the actual values of the variables `name` and `age`, resulting in a complete sentence.

Similarly, in the "Arithmetic operations in f-string" scenario, expressions like `{num1 + num2}` are evaluated inside the f-string, and the result is inserted into the string.

In addition to f-strings, there are other methods for string formatting in Python:

1. **`str.format()` Method:**
   - The `str.format()` method allows us to insert variables into a string using curly braces `{}` as placeholders.
   - We provide the variables as arguments to the `format()` method, and they are replaced in the order they appear in the string.
   - Example: `"My name is {} and I am {} years old.".format(name, age)`

2. **`%` Operator (Old-style formatting):**
   - The `%` operator is an older method for string formatting, where placeholders `%s` (string) and `%d` (integer) are used in the string.
   - We provide the values as a tuple after the `%` operator, and they are replaced in the order they appear in the string.
   - Example: `"My name is %s and I am %d years old." % (name, age)`

These methods offer alternatives to f-strings for string formatting, although f-strings are generally preferred due to their simplicity and readability.

In summary, f-strings make it easy to create dynamic strings by allowing us to insert variables, expressions, or function results directly into a string using placeholders. This helps in making our code more readable and concise.


## Operators

| Operator    | Symbol | Example                         | Definition                                                                                                                      |
|-------------|--------|---------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Arithmetic  | `+`    | `x = 5 + 3`                     | Adds two operands.                                                                                                              |
| Arithmetic  | `-`    | `x = 5 - 3`                     | Subtracts right operand from left operand.                                                                                      |
| Arithmetic  | `*`    | `x = 5 * 3`                     | Multiplies two operands.                                                                                                        |
| Arithmetic  | `/`    | `x = 6 / 3`                     | Divides left operand by right operand (always results in a float).                                                              |
| Arithmetic  | `//`   | `x = 6 // 3`                    | Floor division - divides left operand by right operand and returns the largest integer that is less than or equal to the quotient. |
| Arithmetic  | `%`    | `x = 7 % 3`                     | Modulus - returns the remainder of the division of left operand by right operand.                                               |
| Arithmetic  | `**`   | `x = 2 ** 3`                    | Exponentiation - raises left operand to the power of right operand.                                                              |
| Comparison  | `==`   | `x = (5 == 3)`                  | Equal to - checks if the values of two operands are equal.                                                                      |
| Comparison  | `!=`   | `x = (5 != 3)`                  | Not equal to - checks if the values of two operands are not equal.                                                              |
| Comparison  | `>`    | `x = (5 > 3)`                   | Greater than - checks if the value of left operand is greater than the value of right operand.                                  |
| Comparison  | `<`    | `x = (5 < 3)`                   | Less than - checks if the value of left operand is less than the value of right operand.                                        |
| Comparison  | `>=`   | `x = (5 >= 3)`                  | Greater than or equal to - checks if the value of left operand is greater than or equal to the value of right operand.          |
| Comparison  | `<=`   | `x = (5 <= 3)`                  | Less than or equal to - checks if the value of left operand is less than or equal to the value of right operand.                |
| Logical     | `and`  | `x = True and False`            | Logical AND - returns True if both operands are True.                                                                           |
| Logical     | `or`   | `x = True or False`             | Logical OR - returns True if either operand is True.                                                                            |
| Logical     | `not`  | `x = not True`                  | Logical NOT - returns True if operand is False, and vice versa.                                                                  |
| Assignment  | `=`    | `x = 5`                         | Assigns the value on the right to the variable on the left.                                                                     |
| Assignment  | `+=`   | `x += 3`                        | Adds right operand to the left operand and assigns the result to the left operand.                                               |
| Assignment  | `-=`   | `x -= 3`                        | Subtracts right operand from the left operand and assigns the result to the left operand.                                        |
| Assignment  | `*=`   | `x *= 3`                        | Multiplies left operand by the right operand and assigns the result to the left operand.                                         |
| Assignment  | `/=`   | `x /= 3`                        | Divides left operand by the right operand and assigns the result to the left operand.                                            |
| Membership  | `in`   | `x = 3 in [1, 2, 3, 4]`         | Membership - evaluates to True if it finds a variable in the specified sequence, otherwise False.                               |
| Membership  | `not in`| `x = 5 not in [1, 2, 3, 4]`   | Membership - evaluates to True if it does not finds a variable in the specified sequence, otherwise False.                     |
| Identity    | `is`   | `x = 5 is 5`                    | Identity - evaluates to True if the variables on either side of the operator point to the same object, otherwise False.         |
| Identity    | `is not`| `x = 5 is not '5'`             | Identity - evaluates to True if the variables on either side of the operator do not point to the same object, otherwise False.  |
| Bitwise     | `&`    | `x = 5 & 3`                     | Bitwise AND - performs bitwise AND operation on corresponding bits of the operands.                                             |
| Bitwise     | `|`    | `x = 5 \| 3`                    | Bitwise OR - performs bitwise OR operation on corresponding bits of the operands.                                               |
| Bitwise     | `^`    | `x = 5 ^ 3`                     | Bitwise XOR - performs bitwise XOR operation on corresponding bits of the operands.                                             |
| Bitwise     | `~`    | `x = ~5`                        | Bitwise NOT - inverts all the bits of the operand.                                                                              |
| Bitwise     | `<<`   | `x = 5 << 1`                    | Bitwise left shift - shifts the bits of the left operand to the left by the number of positions specified by the right operand. |
| Bitwise     | `>>`   | `x = 5 >> 1`                    | Bitwise right shift - shifts the bits of the left operand to the right by the number of positions specified by the right operand.|
| Ternary Conditional    | `x if condition else y` | `result = "Even" if num % 2 == 0 else "Odd"` | Evaluates the condition and returns `x` if the condition is true, else returns `y`. Useful for concise conditional expressions.                                           |
**Explanation:**

- **Arithmetic Operators**: Perform mathematical operations like addition, subtraction, multiplication, division, etc.
- **Comparison Operators**: Compare values and return a Boolean result based on the comparison.
- **Logical Operators**: Combine Boolean expressions and return a Boolean result.
- **Assignment Operators**: Assign values to variables and perform arithmetic operations in a concise way.
- **Membership Operators**: Check for membership in a sequence (e.g., lists, tuples, strings).
- **Identity Operators**: Check if two variables refer to the same object in memory.
- **Bitwise Operators**: Perform bitwise operations on integers.
- **Ternary Conditional Operator**: Also known as the conditional expression, it is a concise way to express conditional statements in a single line. 


## Read-Eval-Print Loop (REPL)

| Aspect                  | Description                                                                                                                                                            |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Name                    | REPL (Read-Eval-Print Loop)                                                                                                                                            |
| Purpose                 | Provides an interactive programming environment where commands can be entered, executed, and results immediately displayed.                                          |
| Functionality           | 1. **Read**: Accepts user input or commands entered into the prompt. <br> 2. **Eval**: Interprets and evaluates the input as Python code. <br> 3. **Print**: Displays the result of the evaluation. <br> 4. **Loop**: Repeats the process until terminated by the user. |
| Usage                   | 1. Quick testing of small code snippets. <br> 2. Experimentation with language features and APIs. <br> 3. Debugging and exploration of Python libraries.            |
| Accessibility           | Accessible from the command line or terminal by running the `python` or `python3` command without specifying a script file.                                         |
| Features                | 1. Tab completion: Provides suggestions for completing commands or identifiers. <br> 2. History: Allows access to previously entered commands using the arrow keys. |
| Advantages              | 1. Immediate feedback: Results are displayed instantly after each command execution. <br> 2. Learning aid: Facilitates learning and understanding of Python syntax and features. |
| Disadvantages           | 1. Limited history: Some REPL environments may have a limited command history. <br> 2. No persistent state: Variables and definitions are not saved between sessions. |

**Additional Information:**
- REPLs are commonly used for interactive exploration, debugging, and learning in various programming languages, not just Python.
- REPL environments often provide additional features such as syntax highlighting, code formatting, and integration with external tools and libraries.
- In Python, popular REPL environments include the standard Python REPL accessed from the command line, as well as enhanced alternatives like IPython and Jupyter notebooks.


## Rules and Best Practices for Naming Variables in Python

1. Start with a letter or an underscore (`_`).
2. No reserved keywords or built-in function names.
3. No spaces; use underscores (`_`), camelCase, or snake_case.
4. Use descriptive names for better code readability.
5. Use lowercase letters and snake_case for variable names.
6. Maintain consistency throughout the code.
7. Avoid shadowing built-in functions.
8. Strike a balance between short and long names.


## Operators that yield Boolean results in Python

| Operator    | Symbol | Example                         | Description                                                                                                                      |
|-------------|--------|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| Comparison  | `==`   | `x == y`                        | Returns `True` if x is equal to y, else `False`.                                                                                 |
| Comparison  | `!=`   | `x != y`                        | Returns `True` if x is not equal to y, else `False`.                                                                             |
| Comparison  | `>`    | `x > y`                         | Returns `True` if x is greater than y, else `False`.                                                                             |
| Comparison  | `<`    | `x < y`                         | Returns `True` if x is less than y, else `False`.                                                                                |
| Comparison  | `>=`   | `x >= y`                        | Returns `True` if x is greater than or equal to y, else `False`.                                                                 |
| Comparison  | `<=`   | `x <= y`                        | Returns `True` if x is less than or equal to y, else `False`.                                                                    |
| Logical     | `and`  | `x and y`                       | Returns `True` if both x and y are true, else `False`.                                                                           |
| Logical     | `or`   | `x or y`                        | Returns `True` if either x or y is true, else `False`.                                                                           |
| Logical     | `not`  | `not x`                         | Returns `True` if x is false, else `False`.                                                                                      |
| Identity    | `is`   | `x is y`                        | Returns `True` if both variables refer to the same object, else `False`.                                                         |
| Identity    | `is not`| `x is not y`                  | Returns `True` if both variables do not refer to the same object, else `False`.                                                  |
| Membership  | `in`   | `x in y`                        | Returns `True` if x is a member of the container y, else `False`.                                                                |
| Membership  | `not in`| `x not in y`                  | Returns `True` if x is not a member of the container y, else `False`.                                                            |

These operators are fundamental for creating conditional statements, Boolean expressions, and for logical operations in Python.


## Conditional Statements 

| Aspect               | Definition                                                                                                                                                                                                                      | Syntax                                                  | Explanation                                                                                                                                                                                        |
|----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Conditional Statements | Conditional statements in Python allow you to execute different blocks of code based on whether a condition is evaluated as true or false.                                                                                   | ```python if condition:```<br>&nbsp;&nbsp;&nbsp;&nbsp;```statement```<br>```python elif condition:```<br>&nbsp;&nbsp;&nbsp;&nbsp;```statement```<br>```python else:```<br>&nbsp;&nbsp;&nbsp;&nbsp;```statement``` | Conditional statements consist of an `if` statement followed by zero or more `elif` (else if) statements and an optional `else` statement. Each condition is evaluated in order, and the corresponding block of code is executed if the condition is true. If none of the conditions are true and an `else` statement is present, its block of code is executed. |


## 5 Factors Of Code Quality

| Factor           | Description                                                                                                                                                           |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Readability      | Code should be easy to read and understand, making it accessible to developers and maintainers.                                                                      |
| Maintainability | Code should be easy to modify and update, reducing the time and effort required to make changes or fix issues.                                                        |
| Extensibility   | Code should be designed to support future enhancements and new features, allowing for seamless expansion of functionality without significant restructuring.         |
| Testability     | Code should be written in a way that facilitates testing, ensuring that potential issues can be detected and addressed effectively through automated tests.           |
| Performance     | Code should be efficient in terms of execution time and resource usage, delivering optimal performance to users while minimizing resource consumption.              |
| Code Debt       | Code debt, also known as technical debt, refers to the accumulated cost of deferred work needed to fix problems or implement improvements in code. It arises from shortcuts or compromises made during development that may result in increased maintenance effort or reduced quality over time. |


## String Method

### Case Methods:

| Method           | Description                                                                                                                                                                    | Example                                      |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| `capitalize()`   | Returns a copy of the string with the first character capitalized and the rest lowercased.                                                                                     | `"hello".capitalize()` → `"Hello"`           |
| `casefold()`     | Returns a lowercase version of the string. More aggressive than `lower()` as it removes all case distinctions for comparison.                                                 | `"HELLO".casefold()` → `"hello"`            |
| `lower()`        | Returns a lowercase version of the string.                                                                                                                                     | `"Hello".lower()` → `"hello"`               |
| `upper()`        | Returns an uppercase version of the string.                                                                                                                                     | `"hello".upper()` → `"HELLO"`               |
| `title()`        | Returns a titlecased version of the string where the first character of each word is capitalized.                                                                             | `"hello world".title()` → `"Hello World"`   |
| `swapcase()`     | Returns a string where uppercase characters are converted to lowercase and vice versa.                                                                                       | `"Hello World".swapcase()` → `"hELLO wORLD"`|

### Format Method:

| Method           | Description                                                                                                                                                                    | Example                                      |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| `center(width)` | Returns a centered string of length `width`, padding with spaces on either side as needed.                                                                                    | `"hello".center(10)` → `"  hello   "`      |
| `count(sub)`     | Returns the number of occurrences of substring `sub` in the string.                                                                                                           | `"hello hello".count("hello")` → `2`       |
| `startswith(prefix)` | Returns `True` if the string starts with the specified prefix, otherwise `False`.                                                                                             | `"hello".startswith("he")` → `True`        |
| `endswith(suffix)`   | Returns `True` if the string ends with the specified suffix, otherwise `False`.                                                                                               | `"hello".endswith("lo")` → `True`          |
| `find(sub)`      | Returns the lowest index of substring `sub` in the string, or `-1` if not found.                                                                                              | `"hello".find("l")` → `2`                   |
| `rfind(sub)`     | Returns the highest index of substring `sub` in the string, or `-1` if not found.                                                                                             | `"hello".rfind("l")` → `3`                  |
| `index(sub)`     | Returns the lowest index of substring `sub` in the string, or raises a `ValueError` if not found.                                                                             | `"hello".index("l")` → `2`                  |
| `rindex(sub)`    | Returns the highest index of substring `sub` in the string, or raises a `ValueError` if not found.                                                                            | `"hello".rindex("l")` → `3`                 |
| `replace(old, new)` | Returns a copy of the string with all occurrences of substring `old` replaced by `new`.                                                                                      | `"hello".replace("l", "X")` → `"heXXo"`    |
| `split(sep)`     | Returns a list of substrings separated by `sep`.                                                                                                                               | `"hello world".split(" ")` → `["hello", "world"]` |
| `rsplit(sep)`    | Returns a list of substrings separated by `sep`, starting from the right.                                                                                                     | `"hello world".rsplit(" ")` → `["hello", "world"]`|
| `join(iterable)` | Concatenates the strings in `iterable`, using the string as a separator.                                                                                                       | `" ".join(["hello", "world"])` → `"hello world"`    |

### Additional Methods:

| Method           | Description                                                                                                                                                                    | Example                                      |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| `strip()`        | Returns a copy of the string with leading and trailing whitespace removed.                                                                                                     | `"  hello  ".strip()` → `"hello"`           |
| `rstrip()`       | Returns a copy of the string with trailing whitespace removed.                                                                                                                 | `"  hello  ".rstrip()` → `"  hello"`       |
| `lstrip()`       | Returns a copy of the string with leading whitespace removed.                                                                                                                  | `"  hello  ".lstrip()` → `"hello  "`       |
| `partition(sep)` | Splits the string at the first occurrence of `sep`, and returns a tuple containing the part before the separator, the separator itself, and the part after the separator. | `"hello world".partition(" ")` → `("hello", " ", "world")` |
| `rpartition(sep)`| Splits the string at the last occurrence of `sep`, and returns a tuple containing the part before the separator, the separator itself, and the part after the separator.  | `"hello world".rpartition(" ")` → `("hello", " ", "world")`|

These methods provide a comprehensive set of tools for working with and manipulating strings in Python.


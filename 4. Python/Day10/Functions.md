# Introduction to Functions and Code Redundancy

### Motivation for Using Functions

```python
# Why?: Motivation of function
a = 8
b = 10

print("The sum is: ", a + b)

a1 = 60
b1 = 70

print("The sum is: ", a1 + b1)

a2 = 600
b2 = 70

print("The sum is: ", a2 + b2)
```

**Explanation:**
- This section demonstrates a scenario where the same operation, i.e., addition, is repeated multiple times with different values.
- Despite the slight variations in values, the code structure remains the same, leading to redundancy.
- Such redundancy increases the likelihood of errors, reduces maintainability, and violates the principle of Don't Repeat Yourself (DRY).

#### Output:
```
The sum is:  18
The sum is:  130
The sum is:  670
```

### Function Declaration and Invocation

#### Introduction to Functions

```
# Function
# 1. Declaration / Definition
# 2. Function name
# 3. Parameters - 2
# 4. Function body
```
```python
def add(a, b):
    return round(a + b, 2)

# Function call
print("The sum is: ", add(8, 10))
print("The sum is: ", add(60, 70))
print("The sum is: ", add(600, 70))  # arguments
print("The sum is: ", add(60.748494, 70.89898))
print("The sum is: ", add(160.748494, 170.89898))
```

**Explanation:**
- This section introduces the concept of functions in Python.
- The function `add` is declared with two parameters `a` and `b`.
- Inside the function, `a` and `b` are added, and the result is rounded to two decimal places before being returned.
- The function is then invoked multiple times with different arguments to demonstrate its reusability and flexibility.

#### Output:
```
The sum is:  18
The sum is:  130
The sum is:  670
The sum is:  131.65
The sum is:  331.65
```

### Default Parameter Values and Function Flexibility

#### Default Parameter Values in Functions

```python
# Default values
def driving_test(name, age, car="Dezire"):
    if age >= 18:
        return f"{name} eligible for driving. You will be tested in {car}"
    else:
        return "Try again after few years 👶🍼"

print(driving_test("Sai Subash", 20, "Creata"))
print(driving_test("Sai Ganesh", 20))
```

**Explanation:**
- In this section, a function `driving_test` is defined to determine if a person is eligible for a driving test.
- The function takes two required parameters: `name` and `age`, and an optional parameter `car` with a default value of "Dezire".
- If the age is 18 or above, it returns a message indicating eligibility for driving and specifies the car for the test.
- If the age is below 18, it returns a message suggesting to try again after a few years.
- We demonstrate calling this function with different arguments, including cases where the default value for `car` is used.

#### Output:
```
Sai Subash eligible for driving. You will be tested in Creata
Sai Ganesh eligible for driving. You will be tested in Dezire
```
> In summary, functions are essential for promoting code reuse, enhancing modularity, and improving code readability. Default parameter values add flexibility to functions, allowing them to accommodate different scenarios. By using functions effectively, programmers can write cleaner, more maintainable code.

### Types of Function Arguments and Inbuilt Functions

#### Positional and Keyword Arguments

```python
# Types of argument
# 1. Position argument
# 2. Keyword argument

# Position argument - first
# print(driving_test(20, "Poojitha"))

# Keyword argument - last
print(driving_test(age=20, name="Poojitha"))
print(driving_test("Abishek", car="Honda city", age=20))
```

**Explanation:**
- This section illustrates the difference between positional and keyword arguments in function calls.
- In the first commented line, `driving_test(20, "Poojitha")`, positional arguments are used, where the order of arguments corresponds to the order of parameters in the function definition.
- In the subsequent lines, keyword arguments are used, where arguments are specified by parameter names, allowing for a more explicit and readable function call.

#### Output:
```
Poojitha eligible for driving. You will be tested in Dezire
Abishek eligible for driving. You will be tested in Honda city
```

### Introduction to Inbuilt Functions

#### Commonly Used Inbuilt Functions

```python
# Inbuilt functions
# 1. sum
# 2. max
# 3. min
# 4. len
# 5. round

print(sum([5, 6, 7, 10]))
print(max([5, 6, 10, 7]))
print(min([6, 10, 5, 7]))
print(max("abzcd"))
print(min("bzcd"))
print(max(6, 90, 8, 190, 8, 4))
```

**Explanation:**
- This section showcases some commonly used inbuilt functions in Python and their usage.
- The `sum`, `max`, `min`, `len`, and `round` functions are demonstrated with various data types such as lists and strings.
- These functions provide convenient ways to perform common operations without needing to write custom code.

#### Output:
```
28
10
5
d
b
190
```
> Inbuilt functions are powerful tools provided by Python to perform various operations efficiently. Understanding their usage is essential for writing concise and effective code. By leveraging inbuilt functions, developers can simplify their code and improve productivity.


### Flexible Function Parameters and Lambda Functions

#### Arbitrary Positional Arguments

```python
# Arbitrary Positional Arguments
def own_max(*nums):
    curr_max = nums[0]
    for n in nums:
        if n > curr_max:
            curr_max = n
    return curr_max

print(own_max(5, 6, 10))
print(own_max(5, 6, 10, 7, 80, 60))
```

**Explanation:**
- This section introduces the concept of arbitrary positional arguments in Python functions, denoted by the `*` symbol before the parameter name (`*nums`).
- The function `own_max` is defined to find the maximum value among a variable number of arguments passed to it.
- Inside the function, `nums` becomes a tuple containing all the positional arguments passed to the function.
- The function then iterates through the tuple to find the maximum value.

#### Output:
```
10
80
```

#### Arbitrary Keyword Arguments

```python
# Arbitrary Keyword Arguments
def party(**people):
    return ", ".join(people.values())

print(party(p1="Abishek", p2="Amisha", p3="Sai Ganesh", p4="Poojitha"))
```

**Explanation:**
- This section demonstrates the use of arbitrary keyword arguments in Python functions, denoted by the `**` symbol before the parameter name (`**people`).
- The function `party` is defined to accept an arbitrary number of keyword arguments, where the parameter `people` becomes a dictionary containing the keyword arguments passed to the function.
- Inside the function, `people.values()` retrieves the values from the dictionary, which are then joined into a single string separated by commas.

#### Output:
```
Abishek, Amisha, Sai Ganesh, Poojitha
```

### Lambda Functions

#### Introduction to Lambda Functions

```python
# Lambda functions
add = lambda a, b: a + b
```

**Explanation:**
- Lambda functions, also known as anonymous functions, are concise ways of defining small, one-line functions in Python.
- In this example, a lambda function `add` is defined to calculate the sum of two numbers `a` and `b`.
- The syntax of a lambda function is `lambda parameters: expression`, where `parameters` are the input parameters and `expression` is the operation to be performed.

> Flexible function parameters, including arbitrary positional and keyword arguments, enhance the versatility and usability of functions by allowing them to accept varying numbers of arguments. Lambda functions provide a concise way to define small, simple functions, particularly useful in scenarios where a function is needed for a short-lived operation. Understanding these concepts expands the programmer's toolkit and enables the development of more flexible and expressive code.

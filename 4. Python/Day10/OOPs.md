# Object Oriented Programming (OOP) Concept: Car Example

## Idea
Object-Oriented Programming (OOP) involves modeling real-world objects as classes and creating instances of those classes, known as objects. In this example, we'll model a car as a class.

## Car Class Definition
- A car has attributes such as name, engine type, number of wheels, and number of doors.
- We define a class named `Car` with an `__init__` method (constructor) to initialize the car object with these attributes.
- The `horn` method is an instance method that returns a string representing the sound of the car horn.

```python
class Car:
    def __init__(self, name, engine, wheels, doors):
        self.name = name
        self.engine = engine
        self.wheels = wheels
        self.doors = doors

    def horn(self):
        return f"{self.name} says Vroom Vroom!!!"
```
- **Class Definition**: The `class` keyword is used to define a class. Here, we define a class named `Car`.
- **Constructor Method (`__init__`)**: This method is called when an object of the class is created. It initializes the object's attributes (`name`, `engine`, `wheels`, `doors`) with the provided values.
- **Instance Variables (`self`)**: `self` refers to the instance of the class. It is used to access instance variables within the class.
- **Instance Method (`horn`)**: This method is defined to simulate the car horn sound. It takes `self` as a parameter to access the object's attributes.

## Car Instances
- We create instances of the `Car` class, representing different cars with specific attributes.
- For example, a Ferrari with a V8 engine, 4 wheels, and 2 doors.

```python
ferrari = Car("Ferrari", "V8", 4, 2)
```

## Output
- We print the type of the car instance (`ferrari`) and access its attributes (`name` and `wheels`). We also invoke the `horn` method.

```python
print(type(ferrari))  # <class '__main__.Car'>
print(ferrari.name, ferrari.wheels)  # Ferrari 4
print(ferrari.horn())  # Ferrari says Vroom Vroom!!!
```

## Task 1: Bank Account Class
- We define a class named `Bank` to represent a bank account.
- It has attributes such as account number, name, and balance.
- The `display_balance` method displays the current balance of the account.

```python
class Bank:
    def __init__(self, acc_no, name, balance):
        self.acc_no = acc_no
        self.name = name
        self.balance = balance

    def display_balance(self):
        return f"Your balance is: ₹{self.balance}"
```
- **Class Definition**: Similar to the Car class, we define a class named `Bank`.
- **Constructor Method (`__init__`)**: This method initializes the account's attributes (`acc_no`, `name`, `balance`) with the provided values.
- **Instance Method (`display_balance`)**: This method displays the account balance.

## Task 2: Bank Account Instances
- We create instances of the `Bank` class, representing different bank accounts with specific details.

```python
amisha = Bank(123, "Amisha", 50000)
```

## Output
- We print the name of the account holder and display their balance using the `display_balance` method.

```python
print(amisha.name)  # Amisha
print(amisha.display_balance())  # Your balance is: ₹50,000
```

> Object-Oriented Programming allows us to model real-world entities as objects with attributes and behaviors. Classes serve as blueprints for creating objects, and each object encapsulates its data and functionality. OOP promotes code reusability, modularity, and better organization of code.

----------

### Syntax Explanation:

1. **Class Declaration:**
   - Syntax: `class ClassName:`
   - Explanation: Defines a new class with the name `ClassName`.
   - Example: `class Car:`

2. **Constructor (Initializer) Method:**
   - Syntax: `def __init__(self, arg1, arg2, ...):`
   - Explanation: Special method used to initialize objects of the class. It automatically gets called when a new object is created.
   - Example: 
     ```python
     def __init__(self, name, engine, wheels, doors):
         self.name = name
         self.engine = engine
         self.wheels = wheels
         self.doors = doors
     ```

3. **Instance Method:**
   - Syntax: `def method_name(self, arg1, arg2, ...):`
   - Explanation: Defines a method that operates on instances of the class. The `self` parameter refers to the current instance of the class.
   - Example:
     ```python
     def horn(self):
         return f"{self.name} says Vroom Vroom!!!"
     ```

4. **Creating Instance (Object):**
   - Syntax: `object_name = ClassName(arg1, arg2, ...)`
   - Explanation: Instantiates an object of the class with the specified attributes.
   - Example:
     ```python
     ferrari = Car("Ferrari", "V8", 4, 2)
     ```

5. **Accessing Attributes:**
   - Syntax: `object_name.attribute_name`
   - Explanation: Accesses the attribute of an object.
   - Example:
     ```python
     print(ferrari.name)  # Output: Ferrari
     ```

6. **Method Invocation:**
   - Syntax: `object_name.method_name()`
   - Explanation: Calls an instance method of an object.
   - Example:
     ```python
     print(ferrari.horn())  # Output: Ferrari says Vroom Vroom!!!
     ```

### OOPs Concepts Table:

| Concept         | Explanation                                                                                                    | Example                                       |
|-----------------|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| Class           | A blueprint for creating objects with defined properties and behaviors.                                         | `class Car:`                                  |
| Object          | An instance of a class that encapsulates data and methods.                                                       | `ferrari = Car("Ferrari", "V8", 4, 2)`       |
| Constructor     | A special method (`__init__`) used for initializing objects when they are created.                               | `def __init__(self, name, engine, wheels, doors):` |
| Instance Method | A function that is defined within a class and operates on instances of the class.                                 | `def horn(self):`                             |
| Attribute       | A piece of data attached to a class or object.                                                                   | `self.name`, `self.engine`, etc.             |
| Encapsulation   | Bundling of data and methods that operate on the data, restricting access from outside the class's definition.  | `class Bank:`, `def display_balance(self):`   |
| Inheritance     | A mechanism where a new class inherits properties and behaviors from an existing class.                          | `class SavingsAccount(Bank):`                 |
| Polymorphism    | The ability to present the same interface for different types of data.                                           | Method overriding, method overloading, etc.  |
| Abstraction     | The concept of hiding the complex implementation details and showing only the necessary features of the object.  | Interfaces, abstract classes, etc.           |

Understanding these concepts and their syntax helps in creating robust and maintainable object-oriented Python programs.

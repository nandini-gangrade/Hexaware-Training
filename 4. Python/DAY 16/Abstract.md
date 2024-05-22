# Abstract Classes and Interfaces in Python

In object-oriented programming, abstract classes and interfaces allow you to define methods that must be created within any child classes built from the abstract class. Python provides this functionality with the `abc` module.

## Definition and Use

### Abstract Classes

- **Abstract Class**: A class that cannot be instantiated and often includes one or more abstract methods.
- **Abstract Method**: A method that is declared but contains no implementation. Child classes are forced to provide an implementation for these methods.

Abstract classes are used to ensure that certain methods are implemented in any derived class. They can also provide a common interface for all the derived classes.

### Syntax and Example

#### Step-by-Step Explanation:

1. **Importing the abc Module**
   ```python
   from abc import ABC, abstractmethod
   ```
   - **Explanation**: The `abc` module provides the infrastructure for defining abstract base classes in Python. `ABC` is a helper class that can be used to define abstract classes. `abstractmethod` is a decorator indicating abstract methods.

2. **Defining an Abstract Class**
   ```python
   class Animal(ABC):
       @abstractmethod
       def make_sound(self):
           pass

       @abstractmethod
       def move(self):
           pass
   ```
   - **Explanation**: The `Animal` class is an abstract class inheriting from `ABC`. It defines two abstract methods: `make_sound` and `move`. The `@abstractmethod` decorator indicates that these methods must be overridden in any subclass of `Animal`.

3. **Implementing the Abstract Class in Derived Classes**
   ```python
   class Dog(Animal):
       def make_sound(self):
           print("Woof Woof")

       def move(self):
           print("Running... 🐕")

       def jump(self):
           print("Jumps 🦘")
   ```
   - **Explanation**: The `Dog` class inherits from `Animal` and provides implementations for the `make_sound` and `move` methods. The `jump` method is specific to the `Dog` class.

4. **Creating an Instance of the Derived Class**
   ```python
   maxy = Dog()
   maxy.move()
   ```
   - **Explanation**: An instance of the `Dog` class is created, and the `move` method is called, which prints "Running... 🐕".

5. **Another Derived Class Example**
   ```python
   class Bird(Animal):
       def make_sound(self):
           print("Kiii Kiiii")

       def move(self):
           print("Flying.......")

       def eat(self):
           print("Eatingg...🪱")
   ```
   - **Explanation**: The `Bird` class also inherits from `Animal` and implements the `make_sound` and `move` methods. The `eat` method is specific to the `Bird` class.

6. **Creating an Instance of the Bird Class**
   ```python
   sparrow = Bird()
   sparrow.make_sound()
   sparrow.move()
   sparrow.eat()
   ```
   - **Explanation**: An instance of the `Bird` class is created, and the `make_sound`, `move`, and `eat` methods are called, printing their respective outputs.

### Complete Example

```python
from abc import ABC, abstractmethod

# Abstract class / Interface
class Animal(ABC):
    @abstractmethod
    def make_sound(self):
        pass

    @abstractmethod
    def move(self):
        pass

class Dog(Animal):
    def make_sound(self):
        print("Woof Woof")

    def move(self):
        print("Running... 🐕")

    def jump(self):
        print("Jumps 🦘")

maxy = Dog()
maxy.move()

class Bird(Animal):
    def make_sound(self):
        print("Kiii Kiiii")

    def move(self):
        print("Flying.......")

    def eat(self):
        print("Eatingg...🪱")

sparrow = Bird()
sparrow.make_sound()
sparrow.move()
sparrow.eat()
```

### Summary

- **Abstract Class (`Animal`)**: Defines a template for other classes, with abstract methods `make_sound` and `move` that must be implemented by any subclass.
- **Concrete Classes (`Dog` and `Bird`)**: Implement the abstract methods from the `Animal` class. They can also have additional methods specific to them.

Abstract classes and interfaces enforce a contract for subclasses, ensuring consistency across different implementations while allowing for flexibility and reuse of code.

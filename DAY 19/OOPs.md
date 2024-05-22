# Object-Oriented Programming (OOP) concepts 
### 1. Class

**Definition**: A class is a blueprint for creating objects with predefined properties and methods.

**Syntax**:
```javascript
class ClassName {
    constructor(parameters) { // Constructor for initializing objects
        // Constructor code
    }

    method1(parameters) { // Method definition
        // Method 1 code
    }

    method2(parameters) { // Another method definition
        // Method 2 code
    }
}
```

**Example**:
```javascript
// Define a class called Person
class Person {
    constructor(name, age) { // Constructor with parameters
        this.name = name; // Initializing name property
        this.age = age; // Initializing age property
    }

    greet() { // Method to greet
        return `Hello, my name is ${this.name} and I am ${this.age} years old.`;
    }
}
```

**Keywords**:
- `class`: Declares a new class.
- `constructor`: Defines a special method for initializing class instances.
- `this`: Refers to the current instance of the class within which it is used.

### 2. Constructor

**Definition**: A constructor is a special method within a class that is automatically called when a new instance of the class is created.

**Syntax**:
```javascript
constructor(parameters) {
    // Constructor code
}
```

**Example**:
```javascript
constructor(name, age) { // Constructor with parameters
    this.name = name; // Initializing name property
    this.age = age; // Initializing age property
}
```

**Keywords**:
- `constructor`: Defines the constructor method within a class.
- `this`: Refers to the current instance of the class within the constructor.

### 3. Property

**Definition**: A property is a key-value pair associated with an object that defines its characteristics or attributes.

**Syntax**:
```javascript
this.propertyName = value;
```

**Example**:
```javascript
this.name = name; // Initializing name property
this.age = age; // Initializing age property
```

**Keywords**:
- `this`: Refers to the current instance of the class within which it is used.

### 4. Method

**Definition**: A method is a function defined within a class that can be called to perform actions or manipulate object data.

**Syntax**:
```javascript
methodName(parameters) {
    // Method code
}
```

**Example**:
```javascript
greet() { // Method to greet
    return `Hello, my name is ${this.name} and I am ${this.age} years old.`;
}
```

**Keywords**:
- `this`: Refers to the current instance of the class within the method.

### 5. Inheritance

**Definition**: Inheritance is a mechanism by which a class (subclass) can inherit properties and methods from another class (superclass).

**Syntax**:
```javascript
class SubClassName extends SuperClassName {
    // Subclass code
}
```

**Example**:
```javascript
class Dog extends Animal { // Dog inherits from Animal
    bark() {
        return "Woof!";
    }
}
```

**Keywords**:
- `extends`: Specifies the superclass from which a subclass inherits.
- `super`: Calls methods of the superclass within the subclass constructor.

### 6. Encapsulation

**Definition**: Encapsulation is the bundling of data (properties) and methods that operate on that data within a single unit (class).

**Syntax**: 
```javascript
// Use of access modifiers (not natively supported in JavaScript, but can be emulated using conventions)
```

**Example**:
```javascript
class Person {
    constructor(name, age) {
        this._name = name; // Private property
        this._age = age; // Private property
    }

    get name() {
        return this._name; // Getter method
    }

    set name(value) {
        this._name = value; // Setter method
    }
}
```

**Keywords**:
- None (use of conventions like `_` for private properties).

### 7. Abstraction

**Definition**: Abstraction is the concept of hiding complex implementation details and showing only the essential features of an object.

**Syntax**: 
```javascript
// Use of interfaces (not natively supported in JavaScript, but can be emulated using conventions)
```

**Example**:
```javascript
// Interface
class Shape {
    calculateArea() { // Abstract method
        throw new Error("Method 'calculateArea()' must be implemented.");
    }
}

// Concrete implementation
class Rectangle extends Shape {
    constructor(width, height) {
        super();
        this.width = width;
        this.height = height;
    }

    calculateArea() { // Implementation of abstract method
        return this.width * this.height;
    }
}
```

**Keywords**:
- None (use of interfaces).

### 8. Polymorphism

**Definition**: Polymorphism is the ability of different objects to respond to the same method or message in different ways.

**Syntax**:
```javascript
// Method overriding
```

**Example**:
```javascript
class Animal {
    speak() {
        return "Animal speaks";
    }
}

class Dog extends Animal {
    speak() { // Method overriding
        return "Dog barks";
    }
}
```

**Keywords**:
- None.


# JavaScript and Python Exercise Explanations


## JavaScript Function for Age Checking

### Function Definition

The function `checkForAge()` is designed to check the eligibility of a person based on their age. Here's a breakdown of its components:

```javascript
function checkForAge() {
    const age = document.getElementById("age").value;
    console.log("Checking...", age);

    let msg;
    if (age >= 18) {
        msg = "Your are eligible";
    } else {
        msg = "Your are not eligible. Try again after few years 👶";
    }

    document.getElementById("result").innerText = msg;
}
```

#### Syntax Explanation

- **`function checkForAge()`**: This line declares a function named `checkForAge`.
- **`const age = document.getElementById("age").value;`**: Retrieves the value of the element with the ID "age" from the HTML document, which is presumably an input field where the user inputs their age.
- **`console.log("Checking...", age);`**: Outputs a message to the browser's console along with the entered age, for debugging purposes.
- **`if (age >= 18) { ... } else { ... }`**: Checks if the entered age is greater than or equal to 18. If it is, a message indicating eligibility is assigned to the `msg` variable; otherwise, a message indicating ineligibility is assigned.
- **`document.getElementById("result").innerText = msg;`**: Sets the text content of the HTML element with the ID "result" to the message determined by the age check.

#### Usage

This function is typically invoked when a user interacts with a form on a webpage. When the user inputs their age and triggers an event (such as clicking a button or pressing Enter), this function is called to evaluate their eligibility based on the entered age.

## JavaScript Class Inheritance

### Mall and Shop Classes

#### Mall Class

```javascript
class Mall {
    constructor(shopName) {
        this.shopName = shopName;
    }
    shopIsPresent() {
        return this.shopName + " is present in the ";
    }
}
```

#### Shop Class

```javascript
class Shop extends Mall {
    constructor(name, mallName) {
        super(name); // Base class constructor
        this.mallName = mallName;
    }
    showShop() {
        return this.shopIsPresent() + this.mallName;
    }
}
```

##### Syntax Explanation

- **`class Mall { ... }`**: Defines a class named `Mall`, which serves as the base class for representing shopping malls.
- **`constructor(shopName) { ... }`**: Defines a constructor method for the `Mall` class, which initializes the `shopName` property.
- **`this.shopName = shopName;`**: Assigns the `shopName` property of the instance to the value passed to the constructor.
- **`shopIsPresent() { ... }`**: Defines a method within the `Mall` class to check if a specific shop is present within the mall.
- **`class Shop extends Mall { ... }`**: Defines a class named `Shop` that extends the `Mall` class, inheriting its properties and methods.
- **`super(name);`**: Calls the constructor of the base class (`Mall`) with the `name` parameter passed to the `Shop` constructor.
- **`this.mallName = mallName;`**: Initializes the `mallName` property specific to the `Shop` class.
- **`showShop() { ... }`**: Defines a method within the `Shop` class to display information about the shop and the mall it belongs to.

##### Usage

The `Mall` and `Shop` classes are typically used in applications that simulate or manage shopping malls and stores. Instances of these classes can be created to represent individual malls and shops within those malls. The `showShop()` method of the `Shop` class, in particular, can be called to display information about a specific shop and its location within a mall.

#### Creating an Instance and Displaying the Result

```javascript
let newMall = new Shop("Domino", "Select City Walk Mall");
document.getElementById("demo").innerHTML = newMall.showShop();
```

##### Explanation

- **`let newMall = new Shop("Domino", "Select City Walk Mall");`**: This line creates a new instance of the `Shop` class named `newMall`, representing a shop named "Domino" located in the "Select City Walk Mall".
- **`document.getElementById("demo").innerHTML = newMall.showShop();`**: This line sets the inner HTML content of an element with the ID "demo" to the result of the `showShop()` method called on the `newMall` instance. This typically results in displaying information about the shop and its location within the mall on a web page.

## JavaScript Class Inheritance

### Animal and Dog Classes

#### Animal Class

```javascript
class Animal {
    constructor(name) {
        this.name = name;
    }
    speak() {
        return "Some sound";
    }
}
```

#### Dog Class

```javascript
class Dog extends Animal {
    constructor(name, speed) {
        super(name); // Base class constructor
        this.speed = speed;
    }
    run() {
        return "🐶 wags tail!!";
    }
    speak() {
        return "Woof!! 🐕";
    }
    speed_bonus() {
        return `${this.name} is running at ${this.speed * 2}Km/hr`;
    }
```javascript
}

```

##### Syntax Explanation

- **`class Animal { ... }`**: Defines a class named `Animal`, which serves as the base class for representing animals.
- **`constructor(name) { ... }`**: Defines a constructor method for the `Animal` class, which initializes the `name` property.
- **`this.name = name;`**: Assigns the `name` property of the instance to the value passed to the constructor.
- **`speak() { ... }`**: Defines a method within the `Animal` class to produce a generic sound.
- **`class Dog extends Animal { ... }`**: Defines a class named `Dog` that extends the `Animal` class, inheriting its properties and methods.
- **`super(name);`**: Calls the constructor of the base class (`Animal`) with the `name` parameter passed to the `Dog` constructor.
- **`this.speed = speed;`**: Initializes the `speed` property specific to the `Dog` class.
- **`run() { ... }`**: Defines a method within the `Dog` class to indicate that the dog is running.
- **`speak() { ... }`**: Defines a method within the `Dog` class to produce a sound specific to dogs.
- **`speed_bonus() { ... }`**: Defines a method within the `Dog` class to calculate a speed bonus based on the dog's speed.

##### Usage

The `Animal` and `Dog` classes are typically used in applications that simulate or model animals and dogs specifically. Instances of these classes can be created to represent individual animals and dogs with various properties and behaviors. Methods such as `speak()` and `run()` can be called on instances of the `Animal` and `Dog` classes to produce sounds and behaviors specific to each animal or dog.

#### Creating Instances and Logging Results

```javascript
let toby = new Animal("toby");
console.log(toby.speak());

let maxy = new Dog("maxy", 20);
console.log(maxy.run());
console.log(maxy.speak());
console.log(maxy.speed_bonus());
```

##### Explanation

- **`let toby = new Animal("toby");`**: This line creates a new instance of the `Animal` class named `toby`, representing an animal named "toby". The `speak()` method is then called on the `toby` instance to produce a generic sound.
- **`let maxy = new Dog("maxy", 20);`**: This line creates a new instance of the `Dog` class named `maxy`, representing a dog named "maxy" with a speed of 20. The `run()`, `speak()`, and `speed_bonus()` methods are then called on the `maxy` instance to indicate that the dog is running, produce a dog-specific sound, and calculate a speed bonus, respectively.

## JavaScript Set and Map Examples

### Using Set

A `Set` is a built-in object in JavaScript that allows you to store unique values of any type, whether primitive values or object references.

```javascript
const set = new Set();
set.add(10);
set.add(20);
set.add(30);

set.add(10); // Duplicate, will not be added

// unique
console.log(set); // Output: Set { 10, 20, 30 }

// has
console.log(set.has(20)); // Output: true

// delete
set.delete(20);
console.log(set, set.size); // Output: Set { 10, 30 } 2

// clear
set.clear();
console.log(set); // Output: Set {}
```

#### Explanation

- **`const set = new Set();`**: Creates a new `Set` object named `set`.
- **`set.add(10); set.add(20); set.add(30);`**: Adds three elements (10, 20, and 30) to the set. Since sets only store unique values, duplicates are automatically ignored.
- **`set.has(20);`**: Checks if the set contains the value 20. Returns `true`.
- **`set.delete(20);`**: Deletes the element 20 from the set.
- **`set.clear();`**: Clears all elements from the set.

#### Usage

Sets are commonly used when working with collections of unique values or when you need to perform operations like checking for existence, adding, deleting, or clearing elements efficiently without worrying about duplicates.

### Using Map

A `Map` is a built-in object in JavaScript that allows you to store key-value pairs where both the keys and the values can be of any type.

```javascript
let student = new Map();
student.set("name", "Manju");
student.set("age", 20);
student.set("company", "Hexaware");

console.log(student); // Output: Map { 'name' => 'Manju', 'age' => 20, 'company' => 'Hexaware' }
```

#### Explanation

- **`let student = new Map();`**: Creates a new `Map` object named `student`.
- **`student.set("name", "Manju"); student.set("age", 20); student.set("company", "Hexaware");`**: Sets key-value pairs in the map, where the keys are strings ("name", "age", "company") and the values can be of any type ("Manju", 20, "Hexaware").

#### Usage

Maps are useful for scenarios where you need to associate keys with values and efficiently perform operations like setting, getting, checking for existence, or deleting key-value pairs.


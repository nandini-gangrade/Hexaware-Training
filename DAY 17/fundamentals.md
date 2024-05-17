# JavaScript Basics

JavaScript is a versatile programming language used primarily for web development. Below are some fundamental concepts categorized into different topics with examples and explanations.

## 1. Arithmetic Operations

Arithmetic operations in JavaScript include addition, subtraction, multiplication, division, and exponentiation.

### Addition

```javascript
2 + 3
// Output: 5
```

### Explanation:
- `2 + 3` performs addition and returns `5`.

## 2. Variables and Data Types

Variables in JavaScript can store different types of data, including strings, numbers, and booleans. JavaScript provides three ways to declare variables: `var`, `let`, and `const`.

### 2.1 Variable Declarations

| Declaration Type | Syntax                     | Scope           | Redeclaration | Reassignment | Hoisting                                 | Example Usage                    |
|------------------|----------------------------|-----------------|---------------|--------------|------------------------------------------|----------------------------------|
| `var`            | `var name = "abc";`        | Function-scoped | Yes           | Yes          | Yes (initializes with `undefined`)       | `var name = "Sai subash";`       |
| `let`            | `let name = "abc";`        | Block-scoped    | No            | Yes          | No                                       | `let age = 25;`                  |
| `const`          | `const name = "abc";`      | Block-scoped    | No            | No           | No                                       | `const country = "India";`       |

#### Explanation:

- `var`: Function-scoped. Can be redeclared and updated. Variables are hoisted and initialized with `undefined`.

  ```javascript
  var name = "Sai subash";
  // Output: undefined
  name
  // Output: 'Sai subash'
  ```

- `let`: Block-scoped. Can be updated but not redeclared. Not hoisted in the same way as `var`.

  ```javascript
  let age = 25;
  // Output: undefined
  age
  // Output: 25
  ```

- `const`: Block-scoped. Cannot be updated or redeclared. Must be initialized at the time of declaration. Not hoisted in the same way as `var`.

  ```javascript
  const country = "India";
  // Output: undefined
  country
  // Output: 'India'
  ```

### 2.2 Type Checking

```javascript
typeof(name)
// Output: 'string'
typeof(9)
// Output: 'number'
typeof(true)
// Output: 'boolean'
typeof(false)
// Output: 'boolean'
```

### Explanation:
- `typeof` operator is used to check the data type of a variable or value.

## 3. Comments

Comments are used to explain code and are ignored during execution.

### Single-line Comments

```javascript
// This is a single-line comment
```

### Explanation:
- `//` starts a single-line comment.

## 4. Division and Exponentiation

### Division (Incorrect Syntax Example)

```javascript
2 // 3
// Output: 2
```

### Explanation:
- `2 // 3` is not valid JavaScript syntax for division; correct division would use `/`.

### Exponentiation

```javascript
3 ** 2
// Output: 9
```

### Explanation:
- `3 ** 2` performs exponentiation, equivalent to `3^2`, and returns `9`.

## 5. Arrays

Arrays store multiple values in a single variable.

### Declaring and Accessing Arrays

```javascript
var marks = [70, 80, 90, 100];
// Output: undefined
marks
// Output: [70, 80, 90, 100]
marks[0]
// Output: 70
```

### Explanation:
- `var marks = [70, 80, 90, 100]` declares an array `marks` with four elements.
- Accessing `marks` returns the array `[70, 80, 90, 100]`.
- `marks[0]` accesses the first element of the array, returning `70`.

## 6. Objects

Objects store data in key-value pairs.

### Declaring and Accessing Objects

```javascript
var student = {
    "name": "Tonika",
    "batch": 3
};
// Output: undefined
typeof(student)
// Output: 'object'
student["name"]
// Output: 'Tonika'
student.name
// Output: 'Tonika'
student.name + ' is in ' + student.batch
// Output: 'Tonika is in 3'
student.name + ' is in batch ' + student.batch
// Output: 'Tonika is in batch 3'
```

### Explanation:
- `var student = { "name": "Tonika", "batch": 3 }` declares an object `student`.
- `typeof(student)` returns `'object'`.
- Accessing properties of an object can be done using dot notation (`student.name`) or bracket notation (`student["name"]`).

## 7. Type Coercion

Type coercion is the automatic or implicit conversion of values from one data type to another.

### Examples of Type Coercion

```javascript
[] + []
// Output: ''
[5, 6, 10] + " nice"
// Output: '5,6,10 nice'
[5, 6, 10].toString()
// Output: '5,6,10'
```

### Explanation:
- `[] + []` results in an empty string `''` due to type coercion.
- `[5, 6, 10] + " nice"` results in the string `'5,6,10 nice'` because the array is converted to a string.
- `[5, 6, 10].toString()` explicitly converts the array to the string `'5,6,10'`.

This `.md` file provides an organized overview of JavaScript basics with explanations, syntax, and examples under appropriate categories.

-----

# ES6 Features

ES6, also known as ECMAScript 2015, introduced several new features to JavaScript, making it more powerful and easier to work with. Below is a table summarizing these features with examples and explanations.

| Feature                  | Description                                                  | Syntax Example                                                                                             |
|--------------------------|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| `let` & `const`          | New variable declaration keywords with block scope           | ```javascript<br>let age = 25;<br>const country = "India";<br>```                                          |
| Template Literals        | Allows embedded expressions in strings                       | ```javascript<br>let name = "John";<br>let greeting = `Hello, ${name}!`;<br>```                            |
| Spread Operator (`...`)  | Expands an array or object                                   | ```javascript<br>let arr = [1, 2, 3];<br>let newArr = [...arr, 4, 5];<br>```                               |
| Rest Operator (`...`)    | Collects multiple elements into an array                     | ```javascript<br>function sum(...numbers) { return numbers.reduce((a, b) => a + b, 0); }<br>```            |
| Destructuring            | Extracts values from arrays or properties from objects       | ```javascript<br>let [a, b] = [1, 2];<br>let {name, age} = {name: "John", age: 25};<br>```                 |
| Classes                  | Syntactic sugar for defining constructor functions           | ```javascript<br>class Person {<br>  constructor(name) {<br>    this.name = name;<br>  }<br>}<br>```       |
| Arrow Functions          | Shorter syntax for function expressions                      | ```javascript<br>let add = (a, b) => a + b;<br>```                                                         |
| Promises                 | Used for asynchronous operations                             | ```javascript<br>let promise = new Promise((resolve, reject) => {<br>  // async code<br>});<br>```         |
| Numeric Separators       | Improves readability of large numbers                        | ```javascript<br>let largeNumber = 1_000_000;<br>```                                                       |
| Nullish Coalescing (`??`)| Provides a default value if the first value is `null` or `undefined` | ```javascript<br>let name = null;<br>let defaultName = name ?? "Guest";<br>```                             |
| Optional Chaining (`?.`) | Allows safe access to deeply nested properties               | ```javascript<br>let user = {};<br>let street = user?.address?.street;<br>```                              |

## Explanation of Features

### `let` & `const`

- **Description:**
  - `let` and `const` are new variable declaration keywords introduced in ES6 that provide block scope.
  - `let` allows for variable reassignment but not redeclaration within the same scope.
  - `const` prevents reassignment and redeclaration. Variables declared with `const` must be initialized at the time of declaration.

- **Example:**
  ```javascript
  let age = 25;
  const country = "India";
  ```

- **Details:**
  - `let` and `const` help avoid issues related to variable hoisting and provide a clearer, more predictable scope for variables.
  - Unlike `var`, `let` and `const` do not hoist variables to the top of their block.

### Template Literals

- **Description:**
  - Template literals allow for embedded expressions within strings using backticks (`` ` ``).
  - They provide an easier way to create multi-line strings and perform string interpolation.

- **Example:**
  ```javascript
  let name = "John";
  let greeting = `Hello, ${name}!`;
  ```

- **Details:**
  - Template literals support placeholders indicated by `${}` for embedding expressions.
  - They simplify string concatenation and make code more readable.

### Spread Operator (`...`)

- **Description:**
  - The spread operator expands elements of an array or object into individual elements.

- **Example:**
  ```javascript
  let arr = [1, 2, 3];
  let newArr = [...arr, 4, 5];
  ```

- **Details:**
  - The spread operator can be used for array concatenation, copying arrays, and spreading elements in function arguments.

### Rest Operator (`...`)

- **Description:**
  - The rest operator collects multiple elements into an array, usually used in function parameters.

- **Example:**
  ```javascript
  function sum(...numbers) {
    return numbers.reduce((a, b) => a + b, 0);
  }
  ```

- **Details:**
  - The rest operator allows functions to accept an indefinite number of arguments as an array.

### Destructuring

- **Description:**
  - Destructuring syntax allows for unpacking values from arrays or properties from objects into distinct variables.

- **Example:**
  ```javascript
  let [a, b] = [1, 2];
  let {name, age} = {name: "John", age: 25};
  ```

- **Details:**
  - Destructuring provides a convenient way to extract values and assign them to variables in a single statement.

### Classes

- **Description:**
  - ES6 classes are syntactic sugar over JavaScript’s existing prototype-based inheritance.
  - They provide a cleaner and more concise way to create constructor functions and handle inheritance.

- **Example:**
  ```javascript
  class Person {
    constructor(name) {
      this.name = name;
    }
  }
  ```

- **Details:**
  - Classes support inheritance, static methods, and other features to facilitate object-oriented programming.

### Arrow Functions

- **Description:**
  - Arrow functions provide a shorter syntax for writing function expressions.
  - They lexically bind the `this` value, meaning the value of `this` inside an arrow function is the same as the value of `this` outside the function.

- **Example:**
  ```javascript
  let add = (a, b) => a + b;
  ```

- **Details:**
  - Arrow functions do not have their own `this`, `arguments`, `super`, or `new.target`.

### Promises

- **Description:**
  - Promises are used to handle asynchronous operations.
  - A promise represents a value which may be available now, or in the future, or never.

- **Example:**
  ```javascript
  let promise = new Promise((resolve, reject) => {
    // async code
  });
  ```

- **Details:**
  - Promises have three states: pending, fulfilled, and rejected.
  - They provide methods like `then()`, `catch()`, and `finally()` to handle asynchronous results.

### Numeric Separators

- **Description:**
  - Numeric separators improve the readability of large numeric literals by allowing underscores (`_`) to be placed between digits.

- **Example:**
  ```javascript
  let largeNumber = 1_000_000;
  ```

- **Details:**
  - Numeric separators can be used in any numeric literal (e.g., binary, octal, hexadecimal).

### Nullish Coalescing (`??`)

- **Description:**
  - The nullish coalescing operator provides a default value when the first value is `null` or `undefined`.

- **Example:**
  ```javascript
  let name = null;
  let defaultName = name ?? "Guest";
  ```

- **Details:**
  - This operator is useful for setting default values in variables without accidentally overriding values like `0` or `""`.

### Optional Chaining (`?.`)

- **Description:**
  - Optional chaining allows safe access to deeply nested object properties without having to check if each reference in the chain is valid.

- **Example:**
  ```javascript
  let user = {};
  let street = user?.address?.street;
  ```

- **Details:**
  - Optional chaining prevents runtime errors by returning `undefined` if any part of the chain is `null` or `undefined`.

This `.md` file provides a detailed explanation of each ES6 feature with examples and detailed points to help understand each feature's use and benefits.

## Spread Operator

The spread operator (...) is used to expand elements of an iterable (like an array or a string) into individual elements.

### Example 1: Spread Operator with Arrays

```javascript
let t1 = [80, 90];
let t2 = [50, 60];
let t3 = [...t1, ...t2];
console.log(t3); // [80, 90, 50, 60]
```

In this example, `t3` is assigned a new array containing elements from both `t1` and `t2` using the spread operator.

## Differences between `undefined`, `null`, and not defined in JavaScript:

| Term          | Description                                             | Example                               |
|---------------|---------------------------------------------------------|---------------------------------------|
| `undefined`   | Represents a variable that has been declared but not assigned a value, or a value that does not exist. | `let x; console.log(x); // Output: undefined` |
| `null`        | Represents an intentional absence of any value or object. It must be assigned explicitly. | `let y = null; console.log(y); // Output: null` |
| Not Defined   | Refers to a variable that has been neither declared nor assigned a value. Accessing such a variable results in a ReferenceError. | `console.log(z); // ReferenceError: z is not defined` |

- **Explanation:**
  - `undefined`: Indicates that a variable has been declared but has not been assigned any value, or a value that doesn't exist.
  - `null`: Represents an explicitly assigned absence of a value or object.
  - Not Defined: Refers to attempting to access a variable that has neither been declared nor assigned any value. This results in a ReferenceError.

## Math Operation

JavaScript's `Math.max()` function returns the largest of zero or more numbers.

### Example 2: Using Math.max()

```javascript
console.log(Math.max(6, 7, 4)); // Accepts n no. of arguments
```

This example demonstrates using `Math.max()` with multiple arguments. It accepts any number of arguments and returns the maximum value among them.

## Rest Parameter

The rest parameter (...) allows a function to accept any number of arguments as an array.

### Example 3: Using Rest Parameter in a Function

```javascript
function own_max(...nums) {
  return nums;
}

console.log(own_max(5, 6, 10));              // Output: [5, 6, 10]
console.log(own_max(5, 6, 10, 7, 80, 60));   // Output: [5, 6, 10, 7, 80, 60]
```


----

# JavaScript Loops

In JavaScript, loops are used to execute a block of code repeatedly until a specified condition is met. Here, we'll discuss the different types of loops and provide examples of each.

## Types of Loops

| Loop Type      | Description                                                                                        | Syntax                                                     | Use Case |
|----------------|----------------------------------------------------------------------------------------------------|------------------------------------------------------------|----------|
| `for` Loop     | Runs a block of code a certain number of times.                                                    | `for (initialization; condition; increment/decrement) { ... }` | When the number of iterations is known beforehand. |
| `while` Loop   | Executes a block of code as long as a specified condition is true.                                 | `while (condition) { ... }`                                | When the number of iterations is not known beforehand. |
| `do...while` Loop | Similar to a while loop, but executes the block of code once before checking the condition.     | `do { ... } while (condition);`                            | When you need to ensure the code runs at least once. |
| `for...in` Loop| Iterates over the properties of an object or the indices of an array.                               | `for (variable in object/array) { ... }`                   | When you want to loop through an object's properties or array indices. |
| `for...of` Loop| Iterates over the values of an iterable object (like arrays or strings).                           | `for (variable of iterable) { ... }`                       | When you want to loop through an iterable's values. |

## Examples of Loops

### 1. `for` Loop

```javascript
console.log("Normal for loop");
const marks = [40, 50, 60, 70, 40];
for (let i = 0; i < marks.length; i++) {
  console.log(marks[i]);
}
```

### 2. `for...in` Loop

```javascript
console.log("for...in");
for (let idx in marks) {
  console.log(marks[idx]);
}
```

The `for...in` loop is useful for iterating over the properties of an object or the indices of an array.

```javascript
const avenger = {
  name: "Tony Stark",
  house: "🏘️",
  networth: "💰💰💰",
  power: "🤖",
  phrase: "❤️ you 3000",
};

console.log("for...in with object");
for (let key in avenger) {
  console.log(key, avenger[key]);
}

console.log(Object.keys(avenger)); // ['name', 'house', 'networth', 'power', 'phrase']
console.log(Object.values(avenger)); // ['Tony Stark', '🏘️', '💰💰💰', '🤖', '❤️ you 3000']
```

### 3. `for...of` Loop

```javascript
console.log("for...of");
for (let mark of marks) {
  console.log(mark);
}
```

The `for...of` loop is useful for iterating over the values of an iterable object like arrays or strings.

### Merging Objects Using the Spread Operator

You can merge objects using the spread operator (`...`). This is useful when you want to combine properties from multiple objects.

```javascript
const details = {
  age: 40,
  power: "💿",
};

// Merging objects
console.log({ ...avenger, ...details }); // { name: 'Tony Stark', house: '🏘️', networth: '💰💰💰', power: '💿', phrase: '❤️ you 3000', age: 40 }
console.log({ ...details, ...avenger }); // { age: 40, power: '🤖', name: 'Tony Stark', house: '🏘️', networth: '💰💰💰', phrase: '❤️ you 3000' }
```

In the first `console.log`, the `avenger` object is merged with the `details` object, and the `power` property from `details` overrides the one from `avenger`. In the second `console.log`, the order is reversed, so the `power` property from `avenger` overrides the one from `details`.

Using these examples, you can understand how different loops work in JavaScript and how to use the spread operator for merging objects.

----

# JavaScript Type Casting / Coercion

Type casting (or type coercion) in JavaScript is the process of converting one data type to another. JavaScript performs type coercion automatically in some cases, especially when using operators with mixed data types.

## Examples of Type Casting

### Example 1: Automatic Type Coercion with `+` (Concatenation)

When you use the `+` operator with a number and a string, JavaScript converts the number to a string and concatenates them.

```javascript
var x1 = 3;
var x2 = "5";
console.log(x1 + x2); // Output: '35'
```

In this example, `x1` (which is a number) is coerced into a string, and then concatenated with `x2`, resulting in the string `'35'`.

### Example 2: Automatic Type Coercion with `-` (Subtraction)

When you use the `-` operator with a number and a string, JavaScript tries to convert the string to a number and then performs the subtraction.

```javascript
console.log(x1 - x2); // Output: -2
```

In this example, `x2` (which is a string) is coerced into a number, and then subtracted from `x1`, resulting in the number `-2`.

## Explicit Type Casting

You can also explicitly convert data types in JavaScript using functions like `Number()`, `String()`, `Boolean()`, `parseInt()`, and `parseFloat()`.

### Example 3: Explicit Type Conversion Using `Number()` and `String()`

```javascript
var x1 = 3;
var x2 = "5";

var x2AsNumber = Number(x2);
console.log(x1 + x2AsNumber); // Output: 8

var x1AsString = String(x1);
console.log(x1AsString + x2); // Output: '35'
```

In this example, `Number(x2)` explicitly converts `x2` from a string to a number, allowing for numerical addition. Similarly, `String(x1)` converts `x1` from a number to a string for concatenation.

### Example 4: Explicit Type Conversion Using `parseInt()` and `parseFloat()`

`parseInt()` and `parseFloat()` are used to convert strings to integers and floating-point numbers, respectively.

```javascript
var x3 = "10.5";
var x4 = "20px"; // `parseInt` will stop at the first non-digit character

var intResult = parseInt(x3); // Converts to integer, ignoring the decimal part
console.log(intResult); // Output: 10

var floatResult = parseFloat(x3); // Converts to floating-point number
console.log(floatResult); // Output: 10.5

var intFromString = parseInt(x4); // Stops at the first non-digit character
console.log(intFromString); // Output: 20
```

In this example:
- `parseInt(x3)` converts the string `"10.5"` to the integer `10`.
- `parseFloat(x3)` converts the string `"10.5"` to the floating-point number `10.5`.
- `parseInt(x4)` converts the string `"20px"` to the integer `20`, stopping at the first non-digit character.

## Summary of Type Coercion Rules

- **`+` Operator (Concatenation)**: If either operand is a string, the other operand is converted to a string, and the result is their concatenation.
- **Arithmetic Operators (`-`, `*`, `/`, `%`)**: If either operand is a string that can be converted to a number, JavaScript will convert it to a number and perform the operation.
- **`parseInt()` and `parseFloat()`**: Use these functions to explicitly convert strings to integers and floating-point numbers, respectively.

## Practical Use Cases

Understanding type coercion is important for avoiding unexpected results in your code. Here are a few practical tips:

- Always be mindful of the data types you are working with.
- Use explicit type conversion when necessary to ensure your code behaves as expected.
- Remember that JavaScript tries to be flexible with types, but this can sometimes lead to unintended consequences.

By understanding and using type coercion properly, you can write more predictable and bug-free JavaScript code.

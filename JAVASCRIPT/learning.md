# Introduction to JavaScript Syntax Rules

JavaScript is a dynamic, high-level, object-oriented programming language commonly used to create interactive web pages. In this session, we’ll explore the basic syntax rules that govern how JavaScript code is written and interpreted.

---

## 🧠 Core Concepts

- **Case Sensitivity**  
  JavaScript is case-sensitive.  
  Example: `myVar` and `myvar` are treated as different variables.

- **Statements**  
  Most instructions (statements) end with a semicolon `;`. While optional in many cases, using it consistently helps avoid unexpected behavior.

- **Comments**  
  Comments are ignored by the JavaScript engine and used to explain code:
  ```js
  // This is a single-line comment

  /*
    This is a multi-line comment
    useful for longer explanations
  */
  ```

- **Whitespace**  
  Spaces, tabs, and line breaks improve readability but don’t affect execution.

---

## 💡 Key Notes

- Always use meaningful variable and function names.
- Variable names must not start with a number or contain special characters like `@`, `#`, `%`.
- Semicolons are optional but recommended for clarity and consistency.

---

## 🧪 Simple Examples

```js
let name = "Ali"; // Declaring a variable
console.log(name); // Outputting the value to the console

let age = 25
console.log(age) // Works without semicolon, but not recommended
```
---
# JavaScript Data Types

In JavaScript, **data types** define the kind of value a variable can hold. Understanding data types is essential for writing reliable and predictable code.

---

## 🧠 Primitive Data Types

JavaScript has **seven** primitive data types:

- **String**  
  Represents textual data.  
  Example:
  ```js
  let name = "Ali";
  ```

- **Number**  
  Represents both integers and floating-point numbers.  
  Example:
  ```js
  let age = 25;
  let price = 19.99;
  ```

- **Boolean**  
  Represents logical values: `true` or `false`.  
  Example:
  ```js
  let isOnline = true;
  ```

- **Undefined**  
  A variable declared but not assigned a value.  
  Example:
  ```js
  let score;
  console.log(score); // undefined
  ```

- **Null**  
  Represents an intentional absence of value.  
  Example:
  ```js
  let result = null;
  ```

- **Symbol** (ES6)  
  Used to create unique identifiers.  
  Example:
  ```js
  let id = Symbol("userID");
  ```

- **BigInt** (ES2020)  
  Used for very large integers beyond the safe range of `Number`.  
  Example:
  ```js
  let bigNumber = 123456789012345678901234567890n;
  ```

---

## 🧠 Non-Primitive (Reference) Data Types

These types store **collections of values** or more complex structures:

- **Object**  
  A collection of key-value pairs.  
  Example:
  ```js
  let user = {
    name: "Ali",
    age: 25
  };
  ```

- **Array**  
  A list-like structure.  
  Example:
  ```js
  let colors = ["red", "green", "blue"];
  ```

- **Function**  
  A block of reusable code.  
  Example:
  ```js
  function greet() {
    console.log("Hello!");
  }
  ```

---

## 💡 Notes

- Use `typeof` to check the type of a value:
  ```js
  console.log(typeof "Ali"); // "string"
  console.log(typeof 42);    // "number"
  ```

- JavaScript is **dynamically typed**, meaning variables can change type:
  ```js
  let data = "hello";
  data = 123; // valid
  ```

---
# JavaScript Arrays

An **array** is a special type of object used to store multiple values in a single variable. Arrays are ordered, zero-indexed, and can hold any type of data—even mixed types.

---

## 🧠 Creating Arrays

You can create arrays using square brackets `[]` or the `Array` constructor.

```js
let fruits = ["apple", "banana", "cherry"];
let numbers = [1, 2, 3, 4, 5];
let mixed = ["Ali", 25, true];

let emptyArray = new Array(); // creates an empty array
```

---

## 🧠 Accessing Elements

Use **index numbers** to access array elements. Indexing starts from `0`.

```js
console.log(fruits[0]); // "apple"
console.log(fruits[2]); // "cherry"
```

---

## 🧠 Modifying Arrays

You can change values, add new ones, or remove elements.

```js
fruits[1] = "orange"; // replaces "banana" with "orange"
fruits.push("grape"); // adds "grape" to the end
fruits.pop();         // removes the last element
```

---

## 🧠 Array Properties and Methods

- `length`: Returns the number of elements.
  ```js
  console.log(fruits.length); // 3
  ```

- `push()`: Adds an element to the end.
- `pop()`: Removes the last element.
- `shift()`: Removes the first element.
- `unshift()`: Adds an element to the beginning.
- `includes()`: Checks if an element exists.
- `indexOf()`: Returns the index of an element.
- `join()`: Converts array to string.
- `slice()`: Returns a portion of the array.
- `splice()`: Adds/removes elements at specific positions.

Example:
```js
let colors = ["red", "green", "blue"];
colors.splice(1, 1, "yellow"); // replaces "green" with "yellow"
```

---

## 💡 Notes

- Arrays can hold any type of data, including other arrays or objects.
- JavaScript arrays are dynamic—you don’t need to define their size.
- You can loop through arrays using `for`, `for...of`, or `forEach`.

```js
colors.forEach(function(color) {
  console.log(color);
});
```

---
# JavaScript Conditional Statement: `if`

The `if` statement is used to execute a block of code **only if** a specified condition is true. It’s one of the most essential control structures in JavaScript.

---

## 🧠 Basic Syntax

```js
if (condition) {
  // code to run if condition is true
}
```

If the condition evaluates to `true`, the code inside the block runs. Otherwise, it’s skipped.

---

## 🧠 Example

```js
let score = 85;

if (score >= 80) {
  console.log("You passed!");
}
```

---

## 🧠 `if...else` Statement

Use `else` to define an alternative block if the condition is false.

```js
let age = 17;

if (age >= 18) {
  console.log("Access granted");
} else {
  console.log("Access denied");
}
```

---

## 🧠 `if...else if...else` Chain

Use multiple conditions in sequence:

```js
let grade = 75;

if (grade >= 90) {
  console.log("Excellent");
} else if (grade >= 70) {
  console.log("Good");
} else {
  console.log("Needs improvement");
}
```

---

## 💡 Notes

- Conditions are usually comparisons using operators like `==`, `===`, `>`, `<`, `>=`, `<=`.
- Always use `===` for strict comparison (checks both value and type).
- You can nest `if` statements inside each other, but keep it readable.

---
# JavaScript `switch` Statement

The `switch` statement is used to perform **different actions based on different conditions**. It’s a cleaner alternative to multiple `if...else if` statements when checking a single value.

---

## 🧠 Basic Syntax

```js
switch (expression) {
  case value1:
    // code block
    break;
  case value2:
    // code block
    break;
  default:
    // default code block
}
```

- `expression` is evaluated once.
- The value is compared with each `case`.
- `break` stops the execution after a match.
- `default` runs if no case matches.

---

## 🧠 Example

```js
let day = "Monday";

switch (day) {
  case "Monday":
    console.log("Start of the week");
    break;
  case "Friday":
    console.log("Weekend is near");
    break;
  case "Sunday":
    console.log("Rest day");
    break;
  default:
    console.log("Just another day");
}
```

---

## 💡 Notes

- Without `break`, JavaScript will continue to execute the next cases (called **fall-through**).
- You can group multiple cases:
  ```js
  switch (day) {
    case "Saturday":
    case "Sunday":
      console.log("Weekend");
      break;
  }
  ```

- `switch` works best when comparing a single value against multiple possible matches.

---
```markdown
# 📘 Chapter: Functions in JavaScript

## 🧠 What Is a Function?
A function is a reusable block of code that performs a specific task when called.

```js
function greet(name) {
  console.log("Hello " + name + "!");
}

greet("Ali"); // Output: Hello Ali!
```

---

## 🛠️ Ways to Define Functions

### 1. Function Declaration
```js
function sum(a, b) {
  return a + b;
}
```

### 2. Function Expression
```js
const multiply = function(a, b) {
  return a * b;
};
```

### 3. Arrow Function
```js
const divide = (a, b) => a / b;
```

> ⚠️ Arrow functions don’t have their own `this`. Avoid using them as object methods or class methods.

---

## 🎯 Parameters and Arguments

### Default Parameters
```js
function greet(name = "Guest") {
  console.log("Hello " + name);
}
```

### Rest Parameters
```js
function total(...nums) {
  return nums.reduce((acc, val) => acc + val, 0);
}
```

---

## 🔁 Recursive Functions

Functions that call themselves to solve problems step-by-step.

```js
function factorial(n) {
  if (n === 0) return 1;
  return n * factorial(n - 1);
}
```

---

## 🧩 Functions as First-Class Citizens

Functions can be:

- Assigned to variables
- Passed as arguments
- Returned from other functions

```js
function operate(fn, a, b) {
  return fn(a, b);
}

const add = (x, y) => x + y;

operate(add, 5, 3); // Output: 8
```

---

## 🧠 Key Notes

- A function with no `return` returns `undefined`.
- Arrow functions don’t bind their own `this`.
- Functions can be nested inside other functions.
- Functions can form **closures**, retaining access to outer variables even after execution.

## 🧠 Advanced Concepts in JavaScript Functions

### 🔒 Closures

A **closure** happens when a function “remembers” variables from its outer scope, even after that outer function has finished executing.

```js
function makeCounter() {
  let count = 0;
  return function() {
    count++;
    return count;
  };
}

const counter = makeCounter();
counter(); // 1
counter(); // 2
```

> ✅ Useful for encapsulation, private variables, and stateful logic.

---

### 🧭 Scope and Hoisting

- **Function declarations** are hoisted: you can call them before they’re defined.
- **Function expressions** and **arrow functions** are *not* hoisted.

```js
sayHi(); // Works

function sayHi() {
  console.log("Hi!");
}
```

```js
sayBye(); // ❌ Error

const sayBye = function() {
  console.log("Bye!");
};
```

---

### 🧵 Callback Functions

A **callback** is a function passed into another function to be executed later.

```js
function fetchData(callback) {
  setTimeout(() => {
    callback("Data loaded");
  }, 1000);
}

fetchData((msg) => console.log(msg));
```

> 🔁 Used heavily in asynchronous code, especially before Promises and async/await.

---

### 🧪 IIFE (Immediately Invoked Function Expression)

A function that runs immediately after it’s defined.

```js
(function() {
  console.log("I run instantly!");
})();
```

> ✅ Useful for creating isolated scopes and avoiding global pollution.

---

### 🧠 Pure vs Impure Functions

- **Pure Function**: Same input → same output, no side effects.
- **Impure Function**: May depend on or modify external state.

```js
// Pure
function add(a, b) {
  return a + b;
}

// Impure
let total = 0;
function addToTotal(x) {
  total += x;
}
```

> ✅ Pure functions are easier to test and debug.

---

### 🧬 Higher-Order Functions

Functions that take other functions as arguments or return them.

```js
function repeat(fn, times) {
  for (let i = 0; i < times; i++) {
    fn();
  }
}

repeat(() => console.log("Hello"), 3);
```

> 🔥 Used in array methods like `.map()`, `.filter()`, `.reduce()`.

## 📘 Chapter: Variable Types in ES6 (`var`, `let`, `const`)

### 🧠 Overview

JavaScript (ES6) introduced `let` and `const` to replace the older `var`.  
Each has different **scope**, **hoisting behavior**, and **mutability**.

---

### 🔸 `var`

- **Function-scoped**
- **Hoisted** (but initialized as `undefined`)
- Can be **redeclared** and **updated**

```js
function testVar() {
  console.log(x); // undefined
  var x = 5;
  console.log(x); // 5
}
```

> ⚠️ Avoid using `var` in modern code—it can cause unexpected bugs due to hoisting and scope leakage.

---

### 🔹 `let`

- **Block-scoped** (`{ }`)
- **Hoisted**, but not initialized (ReferenceError if accessed before declaration)
- Can be **updated**, but **not redeclared** in the same scope

```js
let count = 1;
count = 2; // ✅ OK

let count = 3; // ❌ SyntaxError (in same scope)
```

> ✅ Use `let` when the value will change over time (e.g., loop counters, state updates)

---

### 🔸 `const`

- **Block-scoped**
- Must be **initialized** at declaration
- Cannot be **reassigned**, but **can mutate** if it's an object or array

```js
const name = "Ali";
name = "Reza"; // ❌ TypeError

const user = { age: 20 };
user.age = 21; // ✅ Allowed (object mutated)
```

> ✅ Use `const` for values that should never be reassigned—great for constants, config, and function references.

---

### 🧪 Comparison Table

| Feature         | `var`           | `let`           | `const`         |
|----------------|------------------|------------------|------------------|
| Scope          | Function          | Block            | Block            |
| Hoisting       | Yes (undefined)   | Yes (TDZ*)       | Yes (TDZ*)       |
| Redeclaration  | ✅ Yes            | ❌ No            | ❌ No            |
| Reassignment   | ✅ Yes            | ✅ Yes           | ❌ No            |
| Mutation       | ✅ Yes            | ✅ Yes           | ✅ Yes (if object/array) |

> *TDZ = Temporal Dead Zone: accessing before declaration causes error

---

### 🧠 Best Practices

- 🔒 Use `const` by default. Only switch to `let` if you need to reassign.
- 🚫 Avoid `var` unless you're working in legacy code.
- 🧼 Keep scopes clean—block scoping with `let`/`const` prevents accidental leaks.
- 🧠 Use descriptive names for `const` values, especially if they’re config or constants.

---
# 📘 Chapter: Objects in JavaScript

## 🧠 What Is an Object?

An object is a collection of **key-value pairs**. Keys are called **properties**, and values can be any data type—including functions.

```js
const user = {
  name: "Ali",
  age: 25,
  isAdmin: true
};
```

---

## 🛠️ Creating Objects

### 1. Object Literal
```js
const car = {
  brand: "BMW",
  year: 2020
};
```

### 2. Using `new Object()`
```js
const book = new Object();
book.title = "JS Guide";
book.pages = 300;
```

### 3. Using a Constructor Function
```js
function Person(name, age) {
  this.name = name;
  this.age = age;
}

const p1 = new Person("Ali", 25);
```

---

## 🔍 Accessing Properties

### Dot Notation
```js
console.log(user.name); // "Ali"
```

### Bracket Notation
```js
console.log(user["age"]); // 25
```

> ✅ Use bracket notation when the key is dynamic or contains special characters.

---

## ✏️ Modifying Objects

```js
user.age = 26;           // update
user.city = "Kassel";    // add new property
delete user.isAdmin;     // remove property
```

---

## 🧩 Nested Objects

Objects can contain other objects:

```js
const profile = {
  name: "Ali",
  contact: {
    email: "ali@example.com",
    phone: "123456789"
  }
};

console.log(profile.contact.email); // "ali@example.com"
```

---

## 🧠 Methods (Functions Inside Objects)

```js
const calculator = {
  add: function(a, b) {
    return a + b;
  }
};

calculator.add(2, 3); // 5
```

Or using shorthand:

```js
const calculator = {
  add(a, b) {
    return a + b;
  }
};
```

---

## 🔁 Looping Through Object Properties

Use `for...in` to iterate over keys:

```js
for (let key in user) {
  console.log(key + ": " + user[key]);
}
```

---

## 🧠 Built-in Object Methods

- `Object.keys(obj)` → returns array of keys  
- `Object.values(obj)` → returns array of values  
- `Object.entries(obj)` → returns array of `[key, value]` pairs  
- `Object.hasOwnProperty(key)` → checks if key exists

```js
Object.keys(user); // ["name", "age"]
```

---

## 🧠 Notes

- Objects are **reference types**—assigning them to another variable copies the reference, not the value.
- You can use `const` for objects and still modify their properties.
- Objects are the foundation of JSON, APIs, and most JS frameworks.

```
---
```
# 📘 Advanced JavaScript Object Concepts

## 1️⃣ Property Shorthand

If the variable name and the key are the same, you can use shorthand:

```js
const name = "Ali";
const age = 25;

const user = { name, age }; // same as { name: name, age: age }
```

---

## 2️⃣ Computed Property Names

You can use dynamic keys inside objects:

```js
const key = "email";
const user = {
  name: "Ali",
  [key]: "ali@example.com"
};
```

---

## 3️⃣ Object Destructuring

Extract values from an object easily:

```js
const user = { name: "Ali", age: 25 };
const { name, age } = user;

console.log(name); // "Ali"
```

---

## 4️⃣ Spread Operator in Objects

Clone or merge objects:

```js
const user = { name: "Ali", age: 25 };
const updatedUser = { ...user, age: 26, city: "Kassel" };
```

---

## 5️⃣ Optional Chaining

Avoid errors when accessing nested properties:

```js
const user = {};
console.log(user.address?.city); // undefined (no error)
```

---

## 6️⃣ Object.freeze() vs Object.seal()

- `Object.freeze(obj)` → makes the object completely immutable.
- `Object.seal(obj)` → allows value changes but prevents adding/removing properties.

```js
const user = { name: "Ali" };
Object.freeze(user);
user.name = "Reza"; // won't change
```

---

## 7️⃣ Deep vs Shallow Copy

Shallow copy only copies the first level:

```js
const original = { name: "Ali", contact: { email: "ali@example.com" } };
const copy = { ...original };

copy.contact.email = "new@example.com";
console.log(original.contact.email); // "new@example.com"
```

For deep copy, use `structuredClone()` or JSON methods:

```js
const deepCopy = structuredClone(original);
```

---

## 8️⃣ JSON.stringify() and JSON.parse()

Convert objects to strings and back:

```js
const user = { name: "Ali", age: 25 };
const str = JSON.stringify(user); // '{"name":"Ali","age":25}'
const obj = JSON.parse(str);      // { name: "Ali", age: 25 }
```

---

## 🧠 Bonus Tips

- Objects are reference types—assigning them copies the reference, not the value.
- You can use `const` with objects and still modify their properties.
- Most APIs and data formats (like JSON) are based on objects.
---
🔁 Loops in JavaScript: From Zero to Hero

📘 Introduction
Loops in JavaScript allow you to execute a block of code repeatedly, making your programs more efficient and dynamic. Whether you're iterating over arrays, objects, or performing repetitive tasks, loops are essential.

---

🌀 Types of Loops in JavaScript

1. for Loop
Used when the number of iterations is known.

```javascript
for (let i = 0; i < 5; i++) {
  console.log("Iteration:", i);
}
```

2. while Loop
Executes as long as the condition is true.

```javascript
let i = 0;
while (i < 5) {
  console.log("Iteration:", i);
  i++;
}
```

3. do...while Loop
Executes the block at least once before checking the condition.

```javascript
let i = 0;
do {
  console.log("Iteration:", i);
  i++;
} while (i < 5);
```

---

🔍 Loop Control Statements

✅ break
Stops the loop immediately.

```javascript
for (let i = 0; i < 10; i++) {
  if (i === 5) break;
  console.log(i);
}
```

🔄 continue
Skips the current iteration.

```javascript
for (let i = 0; i < 5; i++) {
  if (i === 2) continue;
  console.log(i);
}
```

---

🧩 Looping Over Data Structures

🔁 for...of (Arrays, Strings, etc.)

```javascript
const fruits = ["apple", "banana", "cherry"];
for (const fruit of fruits) {
  console.log(fruit);
}
```

🔁 for...in (Objects)

```javascript
const person = { name: "Ali", age: 21 };
for (const key in person) {
  console.log(${key}: ${person[key]});
}
```

---

🧠 Advanced Looping

🔄 Array Methods (Functional Loops)

forEach

```javascript
[1, 2, 3].forEach(num => console.log(num));
```

map

```javascript
const doubled = [1, 2, 3].map(num => num * 2);
console.log(doubled);
```

filter

```javascript
const evens = [1, 2, 3, 4].filter(num => num % 2 === 0);
console.log(evens);
```

---

⚠️ Common Mistakes

- Forgetting to update loop variables (infinite loop)
- Using for...in on arrays (can lead to unexpected behavior)
- Modifying the array while looping over it

---
🚀 Final Thoughts
Loops are a core part of JavaScript and mastering them will make you a more powerful developer. Whether you're building dynamic UIs, handling data, or writing algorithms—loops are everywhere.
---
🔁 Advanced JavaScript Loops

This guide covers not only the basic loop types but also advanced techniques and patterns used in real-world JavaScript.

---

1. 🔄 Nested Loops

A loop inside another loop.

```javascript
for (let i = 0; i < 3; i++) {
  for (let j = 0; j < 2; j++) {
    console.log(i = ${i}, j = ${j});
  }
}
```

---

2. 🧹 Infinite Loops

Loops that never end unless manually broken.

```javascript
while (true) {
  console.log("This will run forever!");
  // Use break to stop it
}
```

> ⚠️ Be careful—this can crash your browser or app!

---

3. 🧪 Looping with .forEach()

A method for iterating over arrays.

```javascript
const numbers = [1, 2, 3];
numbers.forEach((num, index) => {
  console.log(Index ${index}: ${num});
});
```

---

4. 🧵 Looping with .map(), .filter(), .reduce()

These aren't traditional loops, but they’re powerful for transforming arrays.

```javascript
const doubled = [1, 2, 3].map(n => n * 2); // [2, 4, 6]
const evens = [1, 2, 3, 4].filter(n => n % 2 === 0); // [2, 4]
const sum = [1, 2, 3].reduce((acc, val) => acc + val, 0); // 6
```

---

5. 🛑 Labeled Loops

Used to break out of nested loops more precisely.

```javascript
outerLoop:
for (let i = 0; i < 3; i++) {
  for (let j = 0; j < 3; j++) {
    if (i === 1 && j === 1) break outerLoop;
    console.log(i = ${i}, j = ${j});
  }
}
```

---

✅ Summary

| Loop Type       | Use Case                        |
|----------------|----------------------------------|
| for          | Known number of iterations       |
| while        | Unknown condition-based loop     |
| do...while   | At least one guaranteed run      |
| for...of     | Iterating over arrays/iterables  |
| for...in     | Iterating over object keys       |
| .forEach()   | Array iteration with callback    |
| .map()       | Transforming array elements      |
| .filter()    | Filtering array elements         |
| .reduce()    | Aggregating array values         |
| Labeled Loops  | Breaking out of nested loops     |

---

`

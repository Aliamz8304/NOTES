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

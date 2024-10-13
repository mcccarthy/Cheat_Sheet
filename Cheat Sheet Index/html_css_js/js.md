# JavaScript Cheat Sheet

## Basic Syntax and Operators

| Operator        | Description                                       | Example                     |
|------------------|---------------------------------------------------|-----------------------------|
| `=`              | Assignment operator.                             | `let x = 5;`                |
| `==`             | Equality operator (type coercion).              | `x == '5';`                 |
| `===`            | Strict equality operator (no type coercion).    | `x === 5;`                  |
| `!=`             | Inequality operator (type coercion).            | `x != '5';`                 |
| `!==`            | Strict inequality operator.                      | `x !== 5;`                  |
| `+`              | Addition operator (also concatenation).          | `let sum = 5 + 10;`         |
| `-`              | Subtraction operator.                            | `let difference = 10 - 5;`  |
| `*`              | Multiplication operator.                         | `let product = 5 * 10;`     |
| `/`              | Division operator.                               | `let quotient = 10 / 5;`    |
| `%`              | Modulus operator.                                | `let remainder = 10 % 3;`   |
| `++`             | Increment operator.                              | `x++;`                       |
| `--`             | Decrement operator.                              | `x--;`                       |

* * *

## Data Types and Structures

| Data Type       | Description                                       | Example                     |
|------------------|---------------------------------------------------|-----------------------------|
| `String`         | Represents text.                                 | `let name = "John";`       |
| `Number`         | Represents numeric values.                       | `let age = 30;`            |
| `Boolean`        | Represents true/false values.                   | `let isActive = true;`     |
| `Object`         | Represents a collection of key-value pairs.     | `let person = {name: "John", age: 30};` |
| `Array`          | Represents an ordered list of values.           | `let fruits = ["apple", "banana", "cherry"];` |
| `Null`           | Represents an intentional absence of any object value. | `let data = null;`      |
| `Undefined`      | Represents a variable that has been declared but not assigned a value. | `let result;`            |

* * *

## Common Methods

### Array Methods

| Method               | Description                                       | Example                     |
|----------------------|---------------------------------------------------|-----------------------------|
| `push()`             | Adds one or more elements to the end.            | `fruits.push("orange");`   |
| `pop()`              | Removes the last element.                         | `fruits.pop();`            |
| `shift()`            | Removes the first element.                        | `fruits.shift();`          |
| `unshift()`          | Adds one or more elements to the beginning.      | `fruits.unshift("grape");` |
| `slice()`            | Returns a shallow copy of a portion of an array. | `fruits.slice(1, 3);`      |
| `splice()`           | Adds/removes items to/from an array.             | `fruits.splice(1, 1, "kiwi");` |
| `map()`              | Creates a new array with results from calling a function on every element. | `let lengths = fruits.map(fruit => fruit.length);` |
| `filter()`           | Creates a new array with elements that pass the test of a provided function. | `let longFruits = fruits.filter(fruit => fruit.length > 5);` |
| `reduce()`           | Executes a reducer function on each element of the array, resulting in a single value. | `let total = numbers.reduce((acc, num) => acc + num, 0);` |

### String Methods

| Method               | Description                                       | Example                     |
|----------------------|---------------------------------------------------|-----------------------------|
| `length`             | Returns the length of the string.                | `let len = name.length;`   |
| `toUpperCase()`      | Converts a string to uppercase.                  | `name.toUpperCase();`      |
| `toLowerCase()`      | Converts a string to lowercase.                  | `name.toLowerCase();`      |
| `charAt()`           | Returns the character at a specified index.      | `name.charAt(0);`          |
| `includes()`         | Determines whether a string contains a specified substring. | `name.includes("oh");` |
| `indexOf()`          | Returns the index of the first occurrence of a specified value. | `name.indexOf("o");`  |
| `slice()`            | Extracts a section of a string and returns it as a new string. | `name.slice(1, 3);`     |
| `split()`            | Splits a string into an array of substrings.     | `let words = "Hello World".split(" ");` |

* * *

## ES6 Features

| Feature                | Description                                       | Example                     |
|------------------------|---------------------------------------------------|-----------------------------|
| Arrow Functions        | Shorter syntax for writing function expressions. | `const add = (a, b) => a + b;` |
| Template Literals      | Multi-line strings and string interpolation.      | `` const greeting = `Hello, ${name}`; `` |
| Destructuring          | Extracting values from arrays or objects.        | `const {name, age} = person;` |
| Promises               | Represents the eventual completion (or failure) of an asynchronous operation. | `let promise = new Promise((resolve, reject) => { ... });` |
| `async/await`         | Syntactic sugar for working with Promises.       | `const fetchData = async () => { const data = await getData(); };` |

* * *

## Event Handling

| Method                | Description                                       | Example                     |
|-----------------------|---------------------------------------------------|-----------------------------|
| `addEventListener()`  | Attaches an event handler to an element.         | `button.addEventListener('click', () => { alert('Button clicked!'); });` |
| `removeEventListener()` | Removes an event handler from an element.      | `button.removeEventListener('click', handler);` |
| `preventDefault()`     | Prevents the default action of an event.        | `event.preventDefault();`  |
| `stopPropagation()`    | Stops the event from bubbling up the DOM.       | `event.stopPropagation();`  |

---

This cheat sheet provides an overview of essential JavaScript syntax, data types, common methods, ES6 features, and event handling. You can expand it with more detailed properties or examples as you continue your JavaScript learning journey!


Key Command
Ctrl/Cmd + B Toggle bold
Ctrl/Cmd + I Toggle italic
Alt+S (on Windows) Toggle strikethrough1
Ctrl + Shift + ] Toggle heading (uplevel)
Ctrl + Shift + [ Toggle heading (downlevel)
Ctrl/Cmd + M Toggle math environment
Alt + C Check/Uncheck task list item
Ctrl/Cmd + Shift + V Toggle preview
Ctrl/Cmd + K V Toggle preview to side

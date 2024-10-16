# JavaScript Methods Cheat Sheet

## String Methods

- `charAt(index)`: Returns the character at the specified index.
- `concat(string2, ...)`: Combines two or more strings.
- `includes(substring)`: Checks if the string contains the specified substring.
- `indexOf(substring)`: Returns the index of the first occurrence of the substring.
- `slice(start, end)`: Extracts a section of a string and returns it.
- `split(separator)`: Splits the string into an array based on the separator.
- `toLowerCase()`: Converts the string to lowercase.
- `toUpperCase()`: Converts the string to uppercase.
- `trim()`: Removes whitespace from both ends of the string.
- `replace(searchValue, newValue)`: Replaces occurrences of a substring.

## Array Methods

- `push(element)`: Adds an element to the end of an array.
- `pop()`: Removes the last element from an array.
- `shift()`: Removes the first element from an array.
- `unshift(element)`: Adds an element to the beginning of an array.
- `concat(array2, ...)`: Merges two or more arrays.
- `includes(element)`: Checks if the array contains the specified element.
- `indexOf(element)`: Returns the first index of the element in the array.
- `slice(start, end)`: Returns a shallow copy of part of an array.
- `splice(start, deleteCount, items...)`: Adds or removes items from an array.
- `map(callback)`: Creates a new array with the results of calling a function for every array element.
- `filter(callback)`: Creates a new array with all elements that pass the test implemented by the callback.
- `reduce(callback, initialValue)`: Reduces the array to a single value.
- `forEach(callback)`: Executes a function on each array element.

## Object Methods

- `Object.keys(object)`: Returns an array of a given object's property names.
- `Object.values(object)`: Returns an array of a given object's property values.
- `Object.entries(object)`: Returns an array of key-value pairs.
- `hasOwnProperty(property)`: Checks if the object has the specified property.
- `assign(target, ...sources)`: Copies properties from one or more source objects to a target object.
- `freeze(object)`: Prevents the modification of existing property values.

## Math Methods

- `Math.round(number)`: Rounds a number to the nearest integer.
- `Math.floor(number)`: Rounds a number down to the nearest integer.
- `Math.ceil(number)`: Rounds a number up to the nearest integer.
- `Math.max(...numbers)`: Returns the largest of the given numbers.
- `Math.min(...numbers)`: Returns the smallest of the given numbers.
- `Math.random()`: Returns a random number between 0 and 1.
- `Math.pow(base, exponent)`: Returns the base to the power of exponent.

## Date Methods

- `Date.now()`: Returns the number of milliseconds since January 1, 1970.
- `getFullYear()`: Returns the year.
- `getMonth()`: Returns the month (0-11).
- `getDate()`: Returns the day of the month (1-31).
- `getHours()`: Returns the hour (0-23).
- `getMinutes()`: Returns the minutes (0-59).
- `getSeconds()`: Returns the seconds (0-59).
- `toDateString()`: Returns the date portion of a Date object as a human-readable string.
- `toISOString()`: Converts the date to ISO format.

## DOM Methods

- `getElementById(id)`: Returns an element with the specified ID.
- `getElementsByClassName(className)`: Returns all elements with the specified class.
- `querySelector(selector)`: Returns the first element that matches the CSS selector.
- `querySelectorAll(selector)`: Returns all elements that match the CSS selector.
- `createElement(tag)`: Creates a new HTML element.
- `appendChild(node)`: Adds a node as the last child of an element.
- `removeChild(node)`: Removes a child node from an element.
- `addEventListener(event, callback)`: Attaches an event handler to an element.

## Promise Methods

- `then(callback)`: Executes a callback when a promise is fulfilled.
- `catch(callback)`: Handles errors in promises.
- `finally(callback)`: Executes a callback when a promise is settled (fulfilled or rejected).
- `Promise.all(promises)`: Waits for all promises to resolve.
- `Promise.race(promises)`: Resolves or rejects as soon as one of the promises resolves or rejects.
- `Promise.resolve(value)`: Returns a promise that is resolved with the given value.
- `Promise.reject(reason)`: Returns a promise that is rejected with the given reason.

## Utility Methods

- `console.log(value)`: Outputs a message to the console.
- `setTimeout(callback, delay)`: Executes a function after a specified delay.
- `setInterval(callback, delay)`: Repeatedly executes a function at the specified interval.
- `clearTimeout(timeoutID)`: Cancels a timeout set with `setTimeout()`.
- `clearInterval(intervalID)`: Cancels an interval set with `setInterval()`.

---

This cheat sheet covers essential JavaScript methods for strings, arrays, objects, numbers, dates, DOM manipulation, promises, and utilities. You can copy-paste or save this as a `.md` file for quick reference!

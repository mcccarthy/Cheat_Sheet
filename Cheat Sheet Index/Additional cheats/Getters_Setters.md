
# JavaScript Cheatsheet: Destructuring, `this` Keyword, Shorthand Property Syntax, Getters, and Setters

## 1. Destructuring Assignment

The JavaScript destructuring assignment is a shorthand syntax that allows object properties to be extracted into specific variable values. It uses a pair of curly braces (`{}`) with property names on the left-hand side of an assignment to extract values from objects. The number of variables can be less than the total properties of an object.

const rubiksCubeFacts = {
possiblePermutations: '43,252,003,274,489,856,000',
invented: '1974',
largestCube: '17x17x17'
};

const { possiblePermutations, invented, largestCube } = rubiksCubeFacts;

console.log(possiblePermutations); // '43,252,003,274,489,856,000'
console.log(invented); // '1974'
console.log(largestCube); // '17x17x17'

## 2. Shorthand Property Name Syntax

The shorthand property name syntax in JavaScript allows creating objects without explicitly specifying the property names. In this process, an object is created where the property names match variables that already exist in that context. Shorthand property names populate an object with a key matching the identifier and a value matching the identifier’s value.

const activity = 'Surfing';
const beach = { activity };

console.log(beach); // { activity: 'Surfing' }

## 3. The `this` Keyword

The reserved keyword `this` refers to a method’s calling object, and it can be used to access properties belonging to that object.

Here, the `this` keyword is used inside the object function to refer to the `cat` object and access its `name` property:

const cat = {
name: 'Pipey',
age: 8,
whatName() {
return this.name;
}
};

console.log(cat.whatName());
// Output: Pipey

Every JavaScript function or method has a `this` context. For a function defined inside of an object, `this` will refer to that object itself. For a function defined outside of an object, `this` will refer to the global object (`window` in a browser, `global` in Node.js).

const restaurant = {
numCustomers: 45,
seatCapacity: 100,
availableSeats() {
return this.seatCapacity - this.numCustomers;
}
};

### Arrow Functions and `this`

JavaScript arrow functions do not have their own `this` context but use the `this` of the surrounding lexical context. This makes them a poor choice for writing object methods.

Consider this example:

const myObj = {
data: 'abc',
loggerA: () => { console.log(this.data); },
loggerB() { console.log(this.data); },
};

myObj.loggerA(); // undefined
myObj.loggerB(); // 'abc'

In the code above, `loggerA` uses arrow notation to define the function. Since `data` does not exist in the global context, accessing `this.data` returns `undefined`. `loggerB` uses method syntax, and since `this` refers to the enclosing object, the value of the `data` property is accessed correctly.

## 4. Getters and Setters

JavaScript getter and setter methods are helpful because they offer a way to intercept property access and assignment, allowing for additional actions before these changes take effect.

const myCat = {
\_name: 'Snickers',

get name() {
return this.\_name;
},

set name(newName) {
if (typeof newName === 'string' && newName.length > 0) {
this.\_name = newName;
} else {
console.log("ERROR: name must be a non-empty string");
}
}
};

### Notes

- **Getters** allow for controlled access to property values.
- **Setters** allow for validation and controlled updates of property values.
- Getters and setters also work with private properties, as shown in the example above.

This should now be ready to be indexed without the code block markers.

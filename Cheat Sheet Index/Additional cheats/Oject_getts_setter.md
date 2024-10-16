Here’s a JavaScript cheat sheet for getters, setters,
and the `this` keyword in Markdown format to help clarify
 their usage and scope:

````markdown
# JavaScript Getters, Setters, and `this` Cheat Sheet

## 1. Getters and Setters

### What are Getters and Setters?

- **Getters**: Methods that get the value of a property.
- **Setters**: Methods that set or update the value of a
property.
- They allow you to control access to an object’s
properties, enabling validation or additional logic when getting or setting values.

### Defining Getters and Setters

```js
const person = {
    firstName: 'John',
    lastName: 'Doe',

    // Getter
    get fullName() {
        return `${this.firstName} ${this.lastName}`;
    },

    // Setter
    set fullName(name) {
        const [first, last] = name.split(' ');
        this.firstName = first;
        this.lastName = last;
    }
};

// Using getter
console.log(person.fullName); // Output: John Doe

// Using setter
person.fullName = 'Jane Smith';
console.log(person.fullName); // Output: Jane Smith
```
````

### Notes

- **Getter** methods don’t take parameters.
- **Setter** methods take one parameter, representing the value you want to set.
- `this` refers to the object the getter/setter is bound to.

---

## 2. The `this` Keyword

### What is `this`?

- **`this`** refers to the object that is currently executing the code.
- Inside getters and setters, `this` refers to the object in which they are defined.

### Example

```js
const car = {
    brand: 'Tesla',
    model: 'Model S',

    get description() {
        return `This is a ${this.brand} ${this.model}.`;
    }
};

console.log(car.description); // Output: This is a Tesla Model S.
```

### Using `this` inside a method

```js
const book = {
    title: '1984',
    author: 'George Orwell',
    getDetails: function() {
        return `${this.title} by ${this.author}`;
    }
};

console.log(book.getDetails()); // Output: 1984 by George Orwell
```

---

## 3. Object Scope and Context

### Inside the Object Scope

- Getters and setters must be declared within the object where they are used.
- You can **set** properties using the setter and **access**
them using the getter within or outside the object scope.

### Example

```js
const user = {
    username: '',

    set setUsername(name) {
        this.username = name;
    },

    get getUsername() {
        return this.username;
    }
};

// Setting property value using setter
user.setUsername = 'Havoc';

// Accessing property value using getter
console.log(user.getUsername); // Output: Havoc
```

### Important Points

- **Inside object scope**: You can use `this` to access
  object properties.
- **Outside object scope**: Call getters and setters like regular properties.

---

## 4. Calling Getters and Setters

### Accessing Getters

Getters are accessed like properties, not methods:

```js
console.log(person.fullName); // No parentheses needed!
```

### Setting Values via Setters

Setters are also accessed like properties:

```js
person.fullName = 'New Name'; // No parentheses needed!
```

### Example with Multiple Methods and Properties

```js
const account = {
    balance: 0,

    get currentBalance() {
        return `Your balance is ${this.balance} dollars.`;
    },

    set depositAmount(amount) {
        this.balance += amount;
    }
};

// Depositing money
account.depositAmount = 100;

// Checking balance using getter
console.log(account.currentBalance); // Output: Your balance is 100 dollars.
```

---

## 5. Additional Notes

- **Private properties**: You can manage how properties are
  accessed and modified using getters/setters, even if
  properties are private.
- **Context**: Be cautious with `this` in different contexts (arrow functions vs. regular functions).

```js
const testObj = {
    name: 'Object',
    arrowFunc: () => {
        console.log(this); // Will not refer to testObj,
        but to the global object (or undefined in strict mode)
    },
    regularFunc() {
        console.log(this); // Will refer to testObj
    }
};

testObj.arrowFunc();   // Global object
testObj.regularFunc(); // testObj
```

```

This should help clarify the use of getters, setters,
`this`, and object scope in JavaScript!
```

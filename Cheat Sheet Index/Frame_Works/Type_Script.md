# TypeScript Cheat Sheet

## 1. **Setting up TypeScript**

| Concept                | Description                                      | Code Example |
|------------------------|--------------------------------------------------|--------------|
| **Install TypeScript**  | Install TypeScript globally using npm.           | ```bash npm install -g typescript ``` |
| **Check Version**       | Check TypeScript version.                        | ```bash tsc -v ``` |
| **Compile TypeScript**  | Compile a `.ts` file to `.js`.                   | ```bash tsc file.ts ``` |
| **tsconfig.json**       | Initialize a `tsconfig.json` file to manage project-wide TypeScript settings. | ```bash tsc --init ``` |

---

## 2. **Type Annotations**

| Concept                 | Description                                     | Code Example |
|-------------------------|-------------------------------------------------|--------------|
| **Basic Types**          | TypeScript adds types to JavaScript (`number`, `string`, `boolean`, etc.). | ```typescript let age: number = 25; let username: string = 'John'; let isAdmin: boolean = true; ``` |
| **Arrays**               | Specify types for arrays.                       | ```typescript let scores: number[] = [10, 20, 30]; ``` |
| **Tuples**               | Define an array with a fixed number of elements and types. | ```typescript let person: [string, number] = ['John', 30]; ``` |
| **Enums**                | Define a set of named constants.                | ```typescript enum Role { Admin, User, Guest } let userRole: Role = Role.Admin; ``` |
| **Any**                  | Use `any` for dynamic typing.                   | ```typescript let data: any = 'Hello'; data = 123; ``` |
| **Union Types**          | Allow multiple types for a variable.            | ```typescript let id: number | string = 123; id = 'ABC123'; ``` |
| **Type Aliases**         | Create custom types.                           | ```typescript type Point = { x: number; y: number; }; let coord: Point = { x: 10, y: 20 }; ``` |

---

## 3. **Functions**

| Concept                 | Description                                     | Code Example |
|-------------------------|-------------------------------------------------|--------------|
| **Function Types**       | Annotate function parameters and return types.  | ```typescript function add(a: number, b: number): number { return a + b; } ``` |
| **Optional Parameters**  | Define optional parameters using `?`.           | ```typescript function greet(name: string, age?: number) { console.log(name, age); } ``` |
| **Default Parameters**   | Specify default parameter values.               | ```typescript function log(message: string = 'Hello!') { console.log(message); } ``` |
| **Rest Parameters**      | Use rest parameters for variable-length arguments. | ```typescript function sum(...numbers: number[]): number { return numbers.reduce((acc, curr) => acc + curr, 0); } ``` |
| **Arrow Functions**      | Use arrow functions with type annotations.      | ```typescript const multiply = (x: number, y: number): number => x * y; ``` |

---

## 4. **Interfaces**

| Concept                 | Description                                     | Code Example |
|-------------------------|-------------------------------------------------|--------------|
| **Basic Interface**      | Define the structure of an object.              | ```typescript interface User { name: string; age: number; } let user: User = { name: 'John', age: 25 }; ``` |
| **Optional Properties**  | Use `?` to make properties optional.            | ```typescript interface User { name: string; age?: number; } ``` |
| **Readonly Properties**  | Make properties immutable with `readonly`.      | ```typescript interface User { readonly id: number; name: string; } let user: User = { id: 1, name: 'John' }; user.id = 2; // Error ``` |
| **Extending Interfaces** | Extend one interface with another.              | ```typescript interface Employee extends User { role: string; } let employee: Employee = { name: 'Jane', age: 30, role: 'Developer' }; ``` |
| **Function Interfaces**  | Define the type for a function.                 | ```typescript interface AddFn { (a: number, b: number): number; } let add: AddFn = (x, y) => x + y; ``` |

---

## 5. **Classes**

| Concept                 | Description                                     | Code Example |
|-------------------------|-------------------------------------------------|--------------|
| **Class Syntax**         | TypeScript supports classes (like ES6).         | ```typescript class Person { name: string; constructor(name: string) { this.name = name; } greet() { console.log(`Hello, ${this.name}`); } } ``` |
| **Public/Private**       | Use `public`, `private`, and `protected` to control access to properties. | ```typescript class Animal { private name: string; constructor(name: string) { this.name = name; } } ``` |
| **Readonly Properties**  | Define `readonly` properties in classes.        | ```typescript class Car { readonly brand: string; constructor(brand: string) { this.brand = brand; } } ``` |
| **Inheritance**          | Extend a class using `extends`.                 | ```typescript class Dog extends Animal { bark() { console.log('Woof!'); } } ``` |
| **Abstract Classes**     | Create abstract classes that must be implemented in child classes. | ```typescript abstract class Shape { abstract area(): number; } class Circle extends Shape { constructor(public radius: number) { super(); } area(): number { return Math.PI * this.radius ** 2; } } ``` |

---

## 6. **Generics**

| Concept                 | Description                                     | Code Example |
|-------------------------|-------------------------------------------------|--------------|
| **Generic Functions**    | Create reusable functions with generic types.   | ```typescript function identity<T>(arg: T): T { return arg; } let output = identity<string>('Hello'); ``` |
| **Generic Interfaces**   | Define interfaces with generic types.           | ```typescript interface Box<T> { contents: T; } let stringBox: Box<string> = { contents: 'Hello' }; ``` |
| **Generic Classes**      | Create classes with generic types.              | ```typescript class Box<T> { constructor(public contents: T) {} } let numberBox = new Box<number>(100); ``` |

---

## 7. **TypeScript Utility Types**

| Concept                 | Description                                     | Code Example |
|-------------------------|-------------------------------------------------|--------------|
| **Partial<T>**           | Makes all properties of `T` optional.           | ```typescript interface User { name: string; age: number; } let partialUser: Partial<User> = { name: 'John' }; ``` |
| **Pick<T, K>**           | Select a subset of properties from `T`.         | ```typescript let pickedUser: Pick<User, 'name'> = { name: 'John' }; ``` |
| **Omit<T, K>**           | Omit specific properties from `T`.              | ```typescript let omittedUser: Omit<User, 'age'> = { name: 'John' }; ``` |
| **Readonly<T>**          | Makes all properties of `T` `readonly`.         | ```typescript let readonlyUser: Readonly<User> = { name: 'John', age: 25 }; readonlyUser.age = 30; // Error ``` |

---

## 8. **Type Guards**

| Concept                 | Description                                     | Code Example |
|-------------------------|-------------------------------------------------|--------------|
| **Typeof Guards**        | Check types using `typeof`.                     | ```typescript function isNumber(value: any): value is number { return typeof value === 'number'; } ``` |
| **Instanceof Guards**    | Check if an object is an instance of a class.   | ```typescript class Dog {} class Cat {} function isDog(pet: Dog | Cat): pet is Dog { return pet instanceof Dog; } ``` |

---

## 9. **Decorators**

| Concept                 | Description                                     | Code Example |
|-------------------------|-------------------------------------------------|--------------|
| **Class Decorators**     | Decorate classes to add metadata or behavior.   | ```typescript function Logger(constructor: Function) { console.log('Logging...'); } @Logger class User { constructor(public name: string) {} } ``` |
| **Property Decorators**  | Decorate properties within a class.             | ```typescript function Log(target: any, propertyName: string) { console.log('Property: ', propertyName); } class Product { @Log title: string; } ``` |

---

## 10. **Error Handling**

| Concept                 | Description                                     | Code Example |
|-------------------------|-------------------------------------------------|--------------|
| **try/catch Block**      | Handle exceptions using `try/catch`.            | ```typescript try { let result = riskyOperation(); } catch (error) { console.log('Error:', error); } ``` |
| **Custom Errors**        | Create custom error classes.                    | ```typescript class CustomError extends Error { constructor(message: string) { super(message); this.name = 'CustomError'; } } ``` |

---

This **TypeScript Cheat Sheet** covers key topics such as type annotations, interfaces, classes, generics, utility types, decorators, and error handling. It's designed to help you quickly reference and apply TypeScript features in your projects.


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
Here’s a **TypeScript** cheat sheet covering syntax, types, interfaces,
and utility types in Markdown format.

````markdown
# TypeScript Cheat Sheet

## What is TypeScript?

**TypeScript** is a strongly typed superset of JavaScript that adds static types.
It allows you to catch errors early and provides improved tooling with autocompletion
and type checking.

---

## Basic TypeScript Syntax

### 1. Variables & Types

- **Declaring variables with types**:
  ```typescript
  let name: string = 'James';
  let age: number = 30;
  let isActive: boolean = true;
  ```
````

- **Type inference**: TypeScript automatically infers the type based on the
- assigned value.

  ```typescript
  let username = 'Havoc'; // inferred as string
  ```

### 2. Arrays

- **Array of specific types**:

  ```typescript
  let numbers: number[] = [1, 2, 3];
  let names: string[] = ['Alice', 'Bob'];
  ```

- **Array of multiple types**:

  ```typescript
  let mixedArray: (number | string)[] = [1, 'two', 3];
  ```

### 3. Tuples

- **Fixed-length array with different types**:

  ```typescript
  let person: [string, number, boolean] = ['James', 30, true];
  ```

### 4. Enums

- **Enumerations**:

  ```typescript
  enum Color {
    Red,
    Green,
    Blue
  }
  let favoriteColor: Color = Color.Green; // 1
  ```

---

## Types

### 1. Basic Types

- **Primitive types**: `string`, `number`, `boolean`, `null`, `undefined`.

  ```typescript
  let id: number = 5;
  let isPublished: boolean = true;
  let description: string = 'This is a string';
  ```

### 2. Any Type

- **Flexible type that disables type-checking**:

  ```typescript
  let data: any = 'This can be anything';
  ```

### 3. Union Types

- **Variable can hold more than one type**:

  ```typescript
  let id: string | number;
  id = '123';
  id = 123;
  ```

### 4. Literal Types

- **Restrict the variable to specific values**:

  ```typescript
  let direction: 'up' | 'down';
  direction = 'up'; // OK
  ```

### 5. Type Aliases

- **Create custom types**:

  ```typescript
  type StringOrNumber = string | number;
  let value: StringOrNumber = 42;
  ```

---

## Functions

### 1. Function Types

- **Defining function parameters and return types**:

  ```typescript
  function add(x: number, y: number): number {
    return x + y;
  }
  ```

### 2. Optional & Default Parameters

- **Optional parameters**: Use `?`.

  ```typescript
  function greet(name: string, age?: number) {
    console.log(`Hello, ${name}`);
  }
  ```

- **Default parameter values**:

  ```typescript
  function increment(value: number, incrementBy: number = 1): number {
    return value + incrementBy;
  }
  ```

### 3. Void & Never

- **Void**: For functions that do not return anything.

  ```typescript
  function logMessage(message: string): void {
    console.log(message);
  }
  ```

- **Never**: For functions that never return (e.g., throw errors or infinite loops).

  ```typescript
  function throwError(errorMsg: string): never {
    throw new Error(errorMsg);
  }
  ```

---

## Interfaces

### 1. Basic Interface

- **Defining a shape for an object**:

  ```typescript
  interface User {
    id: number;
    name: string;
    isActive?: boolean; // Optional property
  }

  let user: User = {
    id: 1,
    name: 'James',
    isActive: true
  };
  ```

### 2. Function Interface

- **Interface to define function types**:

  ```typescript
  interface MathFunc {
    (x: number, y: number): number;
  }

  const add: MathFunc = (x, y) => x + y;
  ```

### 3. Extending Interfaces

- **Interfaces can extend other interfaces**:

  ```typescript
  interface Animal {
    name: string;
    sound: string;
  }

  interface Dog extends Animal {
    breed: string;
  }

  let myDog: Dog = {
    name: 'Rex',
    sound: 'Bark',
    breed: 'German Shepherd'
  };
  ```

---

## Classes

### 1. Defining a Class

- **Basic class definition**:

  ```typescript
  class Person {
    name: string;
    age: number;

    constructor(name: string, age: number) {
      this.name = name;
      this.age = age;
    }

    greet(): string {
      return `Hello, my name is ${this.name}`;
    }
  }

  const person1 = new Person('James', 30);
  ```

### 2. Public & Private

- **Access modifiers**:

  - `public`: Accessible from anywhere (default).
  - `private`: Only accessible within the class.
  - `protected`: Accessible within the class and subclasses.

  ```typescript
  class Employee {
    private id: number;
    public name: string;

    constructor(id: number, name: string) {
      this.id = id;
      this.name = name;
    }

    private getId(): number {
      return this.id;
    }
  }
  ```

### 3. Implementing Interfaces in Classes

- **Classes can implement interfaces**:

  ```typescript
  interface Car {
    brand: string;
    drive(): void;
  }

  class Tesla implements Car {
    brand: string;

    constructor(brand: string) {
      this.brand = brand;
    }

    drive() {
      console.log(`${this.brand} is driving`);
    }
  }
  ```

---

## Utility Types

### 1. Partial

- **Makes all properties in an object optional**:

  ```typescript
  interface User {
    id: number;
    name: string;
    age: number;
  }

  let updateUser: Partial<User> = {
    name: 'John'
  };
  ```

### 2. Readonly

- **Prevents modification of object properties**:

  ```typescript
  interface User {
    id: number;
    name: string;
  }

  const user: Readonly<User> = {
    id: 1,
    name: 'James'
  };

  // user.id = 2; // Error: Cannot assign to 'id' because it is a read-only property.
  ```

### 3. Pick

- **Select a subset of properties from an interface**:

  ```typescript
  interface User {
    id: number;
    name: string;
    age: number;
  }

  type UserBasic = Pick<User, 'id' | 'name'>;

  let basicUser: UserBasic = {
    id: 1,
    name: 'Alice'
  };
  ```

### 4. Omit

- **Exclude specific properties from an interface**:

  ```typescript
  type UserWithoutAge = Omit<User, 'age'>;

  let userWithoutAge: UserWithoutAge = {
    id: 2,
    name: 'Bob'
  };
  ```

### 5. Record

- **Create a type with a specific set of keys and values**:

  ```typescript
  type PageViews = 'home' | 'about' | 'contact';

  let views: Record<PageViews, number> = {
    home: 100,
    about: 50,
    contact: 25
  };
  ```

---

This TypeScript cheat sheet gives an overview of common syntax, types, interfaces, and utility types.

This cheat sheet covers essential TypeScript topics.

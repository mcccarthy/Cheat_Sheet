# Testing Cheat Sheet

## 1. **Common Testing Frameworks and Tools**

| Framework/Tool         | Description                                   | Example Command                        |
|------------------------|-----------------------------------------------|----------------------------------------|
| **Jest**               | JavaScript testing framework.                 | ```bash npm install --save-dev jest ``` |
| **Mocha**              | Feature-rich JavaScript test framework.      | ```bash npm install --save-dev mocha ``` |
| **Cypress**            | End-to-end testing framework for web apps.   | ```bash npm install --save-dev cypress ``` |
| **Jasmine**            | Behavior-driven testing framework.            | ```bash npm install --save-dev jasmine ``` |
| **Supertest**          | HTTP assertions for testing Node.js APIs.    | ```bash npm install --save-dev supertest ``` |

---

## 2. **Testing Types**

| Type                   | Description                                   | Example Usage                          |
|------------------------|-----------------------------------------------|----------------------------------------|
| **Unit Testing**       | Testing individual components or functions.  | ```javascript test('adds 1 + 2 to equal 3', () => { expect(add(1, 2)).toBe(3); }); ``` |
| **Integration Testing**| Testing interactions between components.      | ```javascript describe('API Integration', () => { it('should fetch data', async () => { const res = await request(app).get('/api/data'); expect(res.status).toBe(200); }); }); ``` |
| **End-to-End Testing** | Testing the application flow from start to finish. | ```javascript it('should load the homepage', () => { cy.visit('/'); cy.get('h1').should('contain', 'Welcome'); }); ``` |

---

## 3. **Writing Tests**

| Aspect                 | Description                                   | Example Code                           |
|------------------------|-----------------------------------------------|----------------------------------------|
| **Test Structure**     | Organize tests in `describe` and `it` blocks.| ```javascript describe('Array', () => { it('should push an item', () => { const arr = []; arr.push(1); expect(arr).toEqual([1]); }); }); ``` |
| **Assertions**         | Verify outcomes using assertions.             | ```javascript expect(value).toBe(expectedValue); ``` |
| **Mocks and Stubs**    | Simulate dependencies in tests.               | ```javascript jest.mock('moduleName'); ``` |

---

## 4. **Organizing Tests**

| Method                 | Description                                   | Example Structure                     |
|------------------------|-----------------------------------------------|---------------------------------------|
| **Folder Structure**    | Group tests by feature or component.         | ```
/tests
  ├── unit
  │   └── componentA.test.js
  ├── integration
  │   └── api.test.js
  └── e2e
      └── userJourney.test.js
``` |
| **Naming Conventions**  | Use descriptive names for test files and cases.| ```javascript // componentA.test.js ``` |

---

## 5. **Running Tests**

| Command                | Description                                   |
|------------------------|-----------------------------------------------|
| **Run All Tests**      | Execute all tests in the project.            | ```bash npm test ```                   |
| **Run Specific Tests** | Execute tests in a specific file.            | ```bash jest path/to/test.js ```       |
| **Watch Mode**         | Run tests in watch mode for auto-reloading.  | ```bash npm test -- --watch ```       |

---

## 6. **Code Coverage**

| Feature                | Description                                   | Command                                |
|------------------------|-----------------------------------------------|----------------------------------------|
| **Generate Coverage Report** | Measure how much of your code is tested. | ```bash jest --coverage ```            |
| **View Coverage**      | View detailed coverage reports in HTML.      | Check the `coverage` folder generated after running tests. |

---

## 7. **Best Practices**

| Practice               | Description                                   |
|------------------------|-----------------------------------------------|
| **Keep Tests Fast**    | Ensure tests run quickly to encourage frequent execution. |
| **Write Descriptive Tests** | Use clear names and messages to make tests self-documenting. |
| **Test Behavior, Not Implementation** | Focus on what the code does rather than how it does it. |

---

This **Testing Cheat Sheet** provides a comprehensive overview of testing frameworks, types, writing and organizing tests, and best practices for ensuring software quality.


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
# React.js Cheat Sheet

## 1. **Basic Setup**

| Concept          | Description                                      | Code Example                                             |
|------------------|--------------------------------------------------|----------------------------------------------------------|
| **Importing React** | Import React and ReactDOM (if needed) in your project. | ```javascript import React from 'react'; import ReactDOM from 'react-dom'; ``` |
| **JSX**          | JavaScript XML syntax to write HTML in React.     | ```javascript const element = <h1>Hello, React!</h1>; ``` |
| **Functional Component** | A component defined as a function that returns JSX. | ```javascript function MyComponent() { return <h1>Hello!</h1>; } ``` |
| **Class Component** | A component defined as a class. It includes `render()` method. | ```javascript class MyComponent extends React.Component { render() { return <h1>Hello!</h1>; } } ``` |
| **Rendering Components** | Render a component to the DOM.             | ```javascript ReactDOM.render(<MyComponent />, document.getElementById('root')); ``` |

---

## 2. **Props and State**

| Concept          | Description                                      | Code Example                                             |
|------------------|--------------------------------------------------|----------------------------------------------------------|
| **Props**        | Read-only inputs passed to components from their parents. | ```javascript function Greeting(props) { return <h1>Hello, {props.name}</h1>; } ``` |
| **Using Props**  | Pass props from a parent component to a child.    | ```javascript <Greeting name="Alice" /> ``` |
| **State**        | State holds data that can change over time, used in class components or with hooks. | ```javascript this.state = { count: 0 }; ``` |
| **Updating State** | Use `setState()` to update state (in class components). | ```javascript this.setState({ count: this.state.count + 1 }); ``` |
| **useState Hook** | Declare and update state in functional components. | ```javascript const [count, setCount] = useState(0); ``` |

---

## 3. **Lifecycle Methods (Class Components)**

| Method              | Description                                    | Code Example                                             |
|---------------------|------------------------------------------------|----------------------------------------------------------|
| **componentDidMount** | Runs after the component is rendered (e.g., API calls). | ```javascript componentDidMount() { console.log('Mounted'); } ``` |
| **componentDidUpdate** | Runs after a component updates (after props/state change). | ```javascript componentDidUpdate(prevProps) { if (prevProps.data !== this.props.data) { // Do something } } ``` |
| **componentWillUnmount** | Runs before the component is removed from the DOM. | ```javascript componentWillUnmount() { console.log('Unmounting'); } ``` |

---

## 4. **Hooks (Functional Components)**

| Hook            | Description                                      | Code Example                                             |
|-----------------|--------------------------------------------------|----------------------------------------------------------|
| **useState**    | Adds state to functional components.              | ```javascript const [count, setCount] = useState(0); ``` |
| **useEffect**   | Runs side effects in functional components.       | ```javascript useEffect(() => { console.log('Effect'); }, []); ``` |
| **useContext**  | Accesses context value in a component.            | ```javascript const value = useContext(MyContext); ``` |
| **useReducer**  | Alternative to `useState` for managing complex state logic. | ```javascript const [state, dispatch] = useReducer(reducer, initialState); ``` |
| **useRef**      | Access DOM elements or persist values between renders. | ```javascript const inputRef = useRef(null); ``` |

---

## 5. **Conditional Rendering**

| Concept            | Description                                      | Code Example                                             |
|--------------------|--------------------------------------------------|----------------------------------------------------------|
| **Inline If**       | Conditionally render JSX using a ternary operator. | ```javascript {isLoggedIn ? <Dashboard /> : <Login />} ``` |
| **Logical AND**     | Render if a condition is true.                   | ```javascript {isLoggedIn && <Dashboard />} ``` |
| **Conditional Class** | Apply classes conditionally using template literals. | ```javascript <div className={`button ${isActive ? 'active' : ''}`}></div> ``` |

---

## 6. **Forms in React**

| Concept          | Description                                      | Code Example                                             |
|------------------|--------------------------------------------------|----------------------------------------------------------|
| **Controlled Component** | Form elements where the state is managed by React. | ```javascript const [value, setValue] = useState(''); <input type="text" value={value} onChange={e => setValue(e.target.value)} /> ``` |
| **Handling Submit** | Handle form submissions in React.              | ```javascript const handleSubmit = (e) => { e.preventDefault(); console.log(value); }; <form onSubmit={handleSubmit}>...</form> ``` |
| **Form Validation** | Validate form inputs using state or libraries like Formik. | ```javascript const [error, setError] = useState(''); if (!value) { setError('This field is required'); } ``` |

---

## 7. **Lists and Keys**

| Concept          | Description                                      | Code Example                                             |
|------------------|--------------------------------------------------|----------------------------------------------------------|
| **Rendering Lists** | Map over arrays to generate lists in JSX.      | ```javascript const list = items.map(item => <li key={item.id}>{item.name}</li>); ``` |
| **Keys**          | Unique keys help React identify list elements.   | ```javascript <li key={item.id}>{item.name}</li> ``` |

---

## 8. **Context API**

| Concept            | Description                                      | Code Example                                             |
|--------------------|--------------------------------------------------|----------------------------------------------------------|
| **Context Provider** | Used to create a context and pass it down the tree. | ```javascript const MyContext = React.createContext(); <MyContext.Provider value={someValue}>...</MyContext.Provider> ``` |
| **useContext Hook**  | Access context value in functional components.   | ```javascript const value = useContext(MyContext); ``` |

---

## 9. **React Router (v6)**

| Concept              | Description                                      | Code Example                                             |
|----------------------|--------------------------------------------------|----------------------------------------------------------|
| **BrowserRouter**     | Wrap your app with `BrowserRouter` to use routing. | ```javascript import { BrowserRouter as Router } from 'react-router-dom'; <Router>...</Router> ``` |
| **Route**             | Define routes to components.                     | ```javascript import { Route, Routes } from 'react-router-dom'; <Routes><Route path="/" element={<Home />} /></Routes> ``` |
| **Link**              | Use `Link` for client-side navigation.           | ```javascript <Link to="/about">About</Link> ``` |
| **useNavigate**       | Programmatically navigate to another route.      | ```javascript const navigate = useNavigate(); navigate('/home'); ``` |

---

## 10. **React Best Practices**

| Concept            | Description                                      |
|--------------------|--------------------------------------------------|
| **Component Reusability** | Break down components into smaller, reusable ones. |
| **State Management** | Manage local state in components, global state with Context API or external libraries (Redux, Zustand). |
| **Performance Optimization** | Use React.memo, useCallback, and useMemo to avoid unnecessary re-renders. |
| **Error Boundaries** | Catch JavaScript errors in components with Error Boundaries (class components only). |
| **CSS-in-JS**       | Consider libraries like styled-components or Emotion for scoped CSS in components. |

---

This cheat sheet covers the essentials of React.js for quick reference. It includes everything from basic concepts, hooks, to routing and best practices.


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

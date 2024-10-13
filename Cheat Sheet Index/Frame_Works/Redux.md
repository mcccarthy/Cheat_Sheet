# Redux Cheat Sheet

## 1. **Basic Redux Setup**

| Concept               | Description                                     | Code Example                                              |
|-----------------------|-------------------------------------------------|-----------------------------------------------------------|
| **Install Redux and React-Redux** | Install the required libraries for Redux. | ```bash npm install redux react-redux ``` |
| **Create Store**      | Create the Redux store to hold the app's state. | ```javascript import { createStore } from 'redux'; const store = createStore(reducer); ``` |
| **Store Provider**    | Use the `<Provider>` component to pass the store to React. | ```javascript import { Provider } from 'react-redux'; <Provider store={store}> <App /> </Provider> ``` |

---

## 2. **Reducers**

| Concept               | Description                                     | Code Example                                              |
|-----------------------|-------------------------------------------------|-----------------------------------------------------------|
| **Reducer Function**  | A function that takes state and action, returns new state. | ```javascript const initialState = { count: 0 }; function counterReducer(state = initialState, action) { switch(action.type) { case 'INCREMENT': return { count: state.count + 1 }; case 'DECREMENT': return { count: state.count - 1 }; default: return state; } } ``` |
| **Combine Reducers**  | Combine multiple reducers into one root reducer. | ```javascript import { combineReducers } from 'redux'; const rootReducer = combineReducers({ counter: counterReducer, user: userReducer }); const store = createStore(rootReducer); ``` |

---

## 3. **Actions and Action Creators**

| Concept               | Description                                     | Code Example                                              |
|-----------------------|-------------------------------------------------|-----------------------------------------------------------|
| **Action**            | Plain object that describes a state change.     | ```javascript const incrementAction = { type: 'INCREMENT' }; const decrementAction = { type: 'DECREMENT' }; ``` |
| **Action Creator**    | A function that returns an action.              | ```javascript function increment() { return { type: 'INCREMENT' }; } ``` |
| **Dispatching Actions** | Dispatch an action to update the store.         | ```javascript store.dispatch(increment()); ``` |

---

## 4. **Selectors**

| Concept               | Description                                     | Code Example                                              |
|-----------------------|-------------------------------------------------|-----------------------------------------------------------|
| **Selector Function** | Retrieves a specific piece of state from the store. | ```javascript const selectCount = (state) => state.counter.count; ``` |
| **Use Selectors in Components** | Access Redux state in a component using `useSelector`. | ```javascript import { useSelector } from 'react-redux'; const count = useSelector(selectCount); ``` |

---

## 5. **React-Redux Hooks**

| Concept               | Description                                     | Code Example                                              |
|-----------------------|-------------------------------------------------|-----------------------------------------------------------|
| **useDispatch Hook**  | Get access to the `dispatch` function in a component. | ```javascript import { useDispatch } from 'react-redux'; const dispatch = useDispatch(); dispatch(increment()); ``` |
| **useSelector Hook**  | Read state from the Redux store in a component.  | ```javascript import { useSelector } from 'react-redux'; const count = useSelector((state) => state.counter.count); ``` |

---

## 6. **Redux Middleware**

| Concept               | Description                                     | Code Example                                              |
|-----------------------|-------------------------------------------------|-----------------------------------------------------------|
| **Apply Middleware**  | Add middleware like `redux-thunk` for handling async actions. | ```javascript import { applyMiddleware, createStore } from 'redux'; import thunk from 'redux-thunk'; const store = createStore(reducer, applyMiddleware(thunk)); ``` |
| **Async Action with Thunk** | Thunks allow dispatching functions instead of plain actions. | ```javascript function fetchData() { return async (dispatch) => { const data = await fetch('/api'); dispatch({ type: 'FETCH_SUCCESS', payload: data }); }; } ``` |

---

## 7. **Redux DevTools**

| Concept               | Description                                     | Code Example                                              |
|-----------------------|-------------------------------------------------|-----------------------------------------------------------|
| **Enable Redux DevTools** | Integrate Redux DevTools for state debugging.  | ```javascript const store = createStore(reducer, window.__REDUX_DEVTOOLS_EXTENSION__ && window.__REDUX_DEVTOOLS_EXTENSION__()); ``` |
| **Inspect State**     | Inspect and time-travel through state changes using Redux DevTools. | Use Redux DevTools Chrome Extension |

---

## 8. **Immutable State**

| Concept               | Description                                     | Code Example                                              |
|-----------------------|-------------------------------------------------|-----------------------------------------------------------|
| **Immutable Updates** | Always return new objects, do not mutate state.  | ```javascript const newState = { ...state, count: state.count + 1 }; ``` |
| **Immutable Arrays**  | Use methods like `map`, `filter`, or `concat` to avoid mutating arrays. | ```javascript const newArray = [...state.items, newItem]; ``` |

---

## 9. **Redux Toolkit**

| Concept               | Description                                     | Code Example                                              |
|-----------------------|-------------------------------------------------|-----------------------------------------------------------|
| **Install Redux Toolkit** | Simplify Redux setup using the Redux Toolkit.  | ```bash npm install @reduxjs/toolkit ``` |
| **createSlice**       | Creates a slice of the store with reducers and actions. | ```javascript import { createSlice } from '@reduxjs/toolkit'; const counterSlice = createSlice({ name: 'counter', initialState: { count: 0 }, reducers: { increment: (state) => { state.count += 1; }, decrement: (state) => { state.count -= 1; } } }); export const { increment, decrement } = counterSlice.actions; export default counterSlice.reducer; ``` |
| **configureStore**    | Simplifies store setup with default middleware.  | ```javascript import { configureStore } from '@reduxjs/toolkit'; import counterReducer from './counterSlice'; const store = configureStore({ reducer: { counter: counterReducer } }); ``` |

---

## 10. **Redux Patterns and Best Practices**

| Concept               | Description                                     |
|-----------------------|-------------------------------------------------|
| **Action Types**      | Use constants for action types to avoid typos.  |
| **Splitting Reducers** | Use multiple reducers to manage different pieces of state (using `combineReducers`). |
| **Normalizing State** | Flatten nested state structures to make updates easier. |
| **Selector Functions** | Create reusable selector functions to read specific parts of the state. |
| **Middleware for Async** | Use `redux-thunk` or `redux-saga` for handling asynchronous actions. |
| **Use Redux Toolkit** | Leverage Redux Toolkit for easier and less boilerplate setup. |

---

This **Redux Cheat Sheet** covers the essentials of using Redux for state management in React applications, along with Redux Toolkit for simplifying Redux configuration. Let me know if you'd like more detailed examples or any specific Redux concepts expanded!



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
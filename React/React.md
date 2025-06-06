# React and Its Hooks

## Introduction to React

React is a **JavaScript library for building user interfaces**, maintained by Facebook. It's particularly well-suited for building single-page applications where dynamic data needs to be rendered efficiently.

### Key Features
- **Component-Based**: UI is built using reusable components.
- **Declarative**: Describe how the UI should look at any point in time.
- **Virtual DOM**: React uses a virtual DOM to optimize rendering performance.
- **Unidirectional Data Flow**: Data flows from parent to child components via props.

---

## React Hooks

Hooks are functions that let you "hook into" React state and lifecycle features in function components. Introduced in React 16.8, they eliminate the need for class components for most use cases.

### Commonly Used Hooks

---

### 1. `useState`
Allows you to add state to functional components.

```jsx
const [count, setCount] = useState(0);
```

- `count` is the current state.
- `setCount` is a function to update the state.

---

### 2. `useEffect`
Runs side effects in your component, like data fetching or subscriptions.

```jsx
useEffect(() => {
  console.log('Component mounted or updated');
}, [count]);
```

- Runs after every render by default.
- Dependency array controls when it runs.

---

### 3. `useContext`
Provides access to React context values in functional components.

```jsx
const theme = useContext(ThemeContext);
```

- Useful for global state like themes, user info, etc.

---

### 4. `useRef`
Provides a way to access DOM nodes or persist values across renders without triggering re-renders.

```jsx
const inputRef = useRef(null);
```

---

### 5. `useMemo`
Memoizes expensive calculations so they're only recomputed when dependencies change.

```jsx
const result = useMemo(() => computeExpensiveValue(a, b), [a, b]);
```

---

### 6. `useCallback`
Returns a memoized version of the callback function that only changes if one of the dependencies changes.

```jsx
const handleClick = useCallback(() => {
  console.log('Clicked');
}, []);
```

---

### 7. `useReducer`
An alternative to `useState` for complex state logic.

```jsx
const [state, dispatch] = useReducer(reducer, initialState);
```

---

## Custom Hooks

You can create your own hooks by prefixing a function name with `use`.

```jsx
function useCounter(initialValue = 0) {
  const [count, setCount] = useState(initialValue);
  return [count, () => setCount(count + 1)];
}
```

---

## Conclusion

React Hooks simplify component logic and make it easier to reuse stateful behavior. They are now the recommended approach for working with state and side effects in React applications.

For more, visit the official docs: [https://reactjs.org/docs/hooks-intro.html](https://reactjs.org/docs/hooks-intro.html)

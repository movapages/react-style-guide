# React Style Guide

## _Best Practices for ReactJS Development_

This style guide provides recommendations for writing React code that is clean, efficient, and easy to maintain.

> Keep in mind that the rules mentioned are fundamental guidelines, 
> and they can be expanded or in some cases overridden by ESLint plugins within specific project needs.

### 1. Structuring Your Project
- Avoid passing props through multiple component levels; instead, utilize state management or the context API to provide data where needed.
- Break down components into smaller, reusable units with clear logical boundaries.
- Use `propTypes` and `defaultProps` (or `TypeScript` if available) for type checking and preventing errors.


### 2. Component Structure
- Each component should have a single responsibility.
- Try to avoid duplicate code and create a common component to perform the repetitive task to maintain the **DRY** (Don’t Repeat Yourself) code structure.
- Try to always use **functional components** with hooks methods.
- Simplify complex conditional logic by encapsulating it within helper functions or separate components.
- Extract reusable logic into custom hooks.
- Maintain uniqueness for `key` props across your entire application.
- Use ternary operator or logical `&&` operator for simple conditional rendering.

### 3. Naming Conventions
- Use **PascalCase** for naming components.
- Use **camelCase** for naming state and prop variables.
- Use descriptive and meaningful names for variables, functions, and other identifiers to enhance code clarity and maintainability.
- Begin function names with action verbs to specify what the function does. For example, `handleClick`, `fetchData`.

### 4. State & Props
- Don't mutate state directly; use returned function provided by `useState` to update it.
- Only store values in state that are expected to change over time and affect the component's rendering or behavior.
- When updating state based on the previous state value, use the functional form of `setState`. This ensures that updates are based on the latest state and prevents race conditions in concurrent updates.
```js
const [count, setCount] = useState(0);

  const increment = () => {
    // Using the functional form of setState
    setCount(prevCount => prevCount + 1);
  };
```
- If a component has multiple pieces of state, consider splitting them into separate `useState` calls.
- Use `refs` for storing mutable values that should persist across renders without causing re-renders. It can hold references to DOM elements, previous values, or other mutable data.
- Ensure props are treated as immutable data. Components should refrain from modifying the props they receive to maintain data integrity.
- Destructure props in functional components for cleaner code.

### 5. Imports
- Maintain a structured import order.
- Suggested order for importing resources in a React project:
  - _External Imports_: Import external dependencies such as libraries and frameworks. 
  - _Internal Imports_: Import internal resources such as components, utility functions, and other modules within your project. 
  - _Stylesheets_.

### 6. Comments
- Write code that is self-explanatory and easy to understand. Use comments for complex logic or to clarify intent.

> Efficient memory management is crucial for enhancing the quality of our application. 
> Pay attention to these guidelines to optimize memory usage and improve overall performance.

### 7. Memory Optimization
- Regularly profile your code using tools like React DevTools and Chrome DevTools to identify performance bottlenecks.
- Look for opportunities to minimize unnecessary re-renders by using `React.memo`, or the `useMemo` and `useCallback` hooks.
```js
const value = useMemo(() => {
    return doComplicatedCalculations(number);
  }, [number]); // Dependency array ensures recalculation only when 'number' changes
```
- It is important to correctly subscribe and unsubscribe from events, timers, or other external resources to ensure that objects associated with these resources are properly released when no longer needed.
```js
useEffect(() => {
    // Subscribe to event
    window.addEventListener('resize', handleResize);

    // Cleanup function to unsubscribe from event
    return () => {
      window.removeEventListener('resize', handleResize);
    };
  }, []);
```
- Object pooling is a technique that involves reusing objects instead of creating new ones. By maintaining a pool of pre-allocated objects, you can reduce the frequency of garbage collection by reusing existing objects whenever possible.

## Links:
- [React Official Website](https://react.dev)
- [20 React.js Best Practices Learned from Code Reviews](https://medium.com/@techedtalkhub/20-reactjs-best-practices-learned-from-code-reviews-9f846a132e52)
- [Understanding React 18's Automatic Garbage Collection](https://borstch.com/blog/development/understanding-react-18s-automatic-garbage-collection)
- [Optimizing React Memory Optimization](https://medium.com/@nouraldin.alsweirki/optimizing-react-memory-optimization-937ab26e9e90)
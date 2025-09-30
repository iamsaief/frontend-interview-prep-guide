<div align="center">
    <img height="60" src="https://img.icons8.com/color/344/javascript.png" />
    <img height="55" src="https://svgmix.com/uploads/e86a0a-react.svg" />
  <h1>🚀 The Ultimate Frontend Interview Prep Guide</h1>
</div>

Master **React & JavaScript interview** prep with **100+ Q&A** and **cheat sheets**. Perfect guide for frontend developers to learn, revise, and crack interviews

I built this resource for **learning, sharing, and community growth** 🌱. If it helps you, a ⭐️ on the repo or a share would mean the world!

✨ Best of luck, **Happy coding!**

<p align="center">
💬 In case you want to reach out or just say hi, ↩️ <br/>
<a href="https://www.facebook.com/saiefalemon">Facebook</a> | <a href="https://www.linkedin.com/in/saiefalemon">LinkedIn</a> | <a href="https://www.iamsaief.github.io.com/">Portfolio</a>
</p>

---

**🗂️ Table of Contents**

- [✴️ 50 JavaScript Interview Q\&A](#️-50-javascript-interview-qa)
  - [🏗️ Core Concepts \& Language Fundamentals](#️-core-concepts--language-fundamentals)
  - [🗂️ Objects, Functions \& Prototypes](#️-objects-functions--prototypes)
  - [🚀 Asynchronous JavaScript](#-asynchronous-javascript)
  - [🌍 ES6+ Features](#-es6-features)
  - [⚖️ Advanced Concepts \& Performance](#️-advanced-concepts--performance)
- [⚛️ 50 React Interview Q\&A](#️-50-react-interview-qa)
  - [🏗️ Architecture \& Core Concepts](#️-architecture--core-concepts)
  - [🗂️ State Management](#️-state-management)
  - [🚀 Advanced \& Performance](#-advanced--performance)
  - [🌍 SSR, Routing \& Data](#-ssr-routing--data)
  - [⚖️ Accessibility, Testing \& UX](#️-accessibility-testing--ux)
- [🤖 Cheat Sheets](#-cheat-sheets)
  - [✴️ JavaScript Core Concepts](#️-javascript-core-concepts)
  - [⚛️ React Core Concepts](#️-react-core-concepts)

---

Available In: [🇧🇩 বাংলা](./bn-BD/README_bn-BD.md)

---

# ✴️ 50 JavaScript Interview Q&A

## 🏗️ Core Concepts & Language Fundamentals

Q1. What are the differences between var, let, and const?
A1. var is function-scoped and hoisted, let and const are block-scoped; const cannot be reassigned.

Q2. Explain hoisting in JavaScript.
A2. Variable and function declarations are moved to the top of their scope during compilation.

Q3. What is the difference between == and ===?
A3. == does type coercion, === checks both value and type strictly.

Q4. What are closures and why are they useful?
A4. A closure is a function that remembers variables from its outer scope; useful for encapsulation and state.

Q5. Explain the concept of scope in JavaScript.
A5. Scope defines variable accessibility: global, function, and block scope.

Q6. What is the difference between synchronous and asynchronous code?
A6. Synchronous executes line by line; asynchronous allows non-blocking operations via callbacks, promises, async/await.

Q7. What are higher-order functions?
A7. Functions that take other functions as arguments or return them.

Q8. What is the difference between null and undefined?
A8. undefined means a variable is declared but not assigned; null is an intentional empty value.

Q9. What are template literals?
A9. String literals with backticks that support interpolation and multiline strings.

Q10. What is the difference between primitive and reference types?
A10. Primitives are immutable and stored by value; objects/arrays/functions are reference types stored by reference.

## 🗂️ Objects, Functions & Prototypes

Q11. Explain prototypal inheritance.
A11. Objects inherit properties/methods from their prototype chain.

Q12. What is the difference between function declaration and function expression?
A12. Declarations are hoisted; expressions are not.

Q13. What is the difference between arrow functions and regular functions?
A13. Arrow functions don’t have their own this or arguments.

Q14. What is the purpose of the this keyword?
A14. Refers to the object that is executing the current function.

Q15. How does bind(), call(), and apply() differ?
A15. All set this; call and apply invoke immediately (apply takes array args), bind returns a new function.

Q16. What are IIFEs (Immediately Invoked Function Expressions)?
A16. Functions executed immediately after definition, often for scoping.

Q17. What is the difference between shallow copy and deep copy?
A17. Shallow copy copies references; deep copy duplicates nested objects.

Q18. How do you check if an object is an array?
A18. Use Array.isArray(obj).

Q19. What is the difference between Object.freeze() and Object.seal()?
A19. freeze prevents adding/removing/modifying; seal prevents adding/removing but allows modifying existing.

Q20. What is event delegation?
A20. Attaching a single event listener to a parent to handle events on child elements.

## 🚀 Asynchronous JavaScript

Q21. What are Promises?
A21. Objects representing eventual completion/failure of async operations.

Q22. What is async/await?
A22. Syntactic sugar over Promises for writing cleaner async code.

Q23. What is the event loop?
A23. Mechanism that handles async callbacks by moving tasks from the queue to the call stack.

Q24. What are microtasks and macrotasks?
A24. Microtasks (Promises, MutationObserver) run before macrotasks (setTimeout, setInterval).

Q25. What is the difference between setTimeout and setImmediate?
A25. setTimeout schedules after a delay; setImmediate executes after the current poll phase (Node.js).

Q26. How does Promise.all() differ from Promise.race()?
A26. all waits for all promises; race resolves/rejects on the first settled promise.

Q27. What is a callback hell?
A27. Nested callbacks making code unreadable; solved by Promises/async-await.

Q28. What is the difference between concurrency and parallelism?
A28. Concurrency = multiple tasks in progress; parallelism = tasks executed simultaneously.

Q29. How do you cancel a fetch request?
A29. Use AbortController with fetch.

Q30. What is debouncing vs throttling?
A30. Debounce delays execution until inactivity; throttle limits execution to once per interval.

## 🌍 ES6+ Features

Q31. What are default parameters?
A31. Function parameters with default values if not provided.

Q32. What are rest and spread operators?
A32. Rest collects arguments into an array; spread expands arrays/objects.

Q33. What are modules in JavaScript?
A33. ES6 modules use import/export for modular code.

Q34. What are generators?
A34. Functions that can pause and resume with yield.

Q35. What are symbols?
A35. Unique and immutable primitive values often used as object keys.

Q36. What is destructuring?
A36. Extracting values from arrays/objects into variables.

Q37. What are WeakMap and WeakSet?
A37. Collections holding weak references to objects, preventing memory leaks.

Q38. What is optional chaining?
A38. ?. safely accesses nested properties without throwing errors.

Q39. What is nullish coalescing?
A39. ?? returns right-hand value only if left is null or undefined.

Q40. What are tagged template literals?
A40. Functions that process template literals for custom string output.

## ⚖️ Advanced Concepts & Performance

Q41. What is currying?
A41. Transforming a function with multiple args into nested single-arg functions.

Q42. What is memoization?
A42. Caching function results to avoid recomputation.

Q43. What is tail call optimization?
A43. Reusing stack frames for recursive calls to save memory.

Q44. What are service workers?
A44. Scripts running in background for caching, offline support, push notifications.

Q45. What is the difference between localStorage, sessionStorage, and cookies?
A45. localStorage persists, sessionStorage clears on tab close, cookies are sent with requests.

Q46. What is the difference between == and Object.is()?
A46. Object.is is like === but handles NaN and -0 correctly.

Q47. How does garbage collection work in JS?
A47. Uses reachability; unreferenced objects are collected.

Q48. What is event bubbling vs capturing?
A48. Bubbling = child → parent; capturing = parent → child.

Q49. What is the difference between map(), forEach(), filter(), and reduce()?
A49. map transforms, forEach iterates, filter selects, reduce accumulates.

Q50. What are pure functions?
A50. Functions with no side effects, always returning same output for same input.

---

# ⚛️ 50 React Interview Q&A

## 🏗️ Architecture & Core Concepts

**Q1. What are the limitations of React in building large-scale applications?**
A1. React is only a view library; scaling requires external solutions for routing, state, and architecture.

Q2. How does React manage the Virtual DOM, and what are the benefits?
A2. React diffs the Virtual DOM against the previous tree and batches updates, minimizing real DOM operations.

Q3. Can React Hooks fully replace Redux for state management? Explain why or why not. A3. Hooks can replace Redux in smaller apps, but Redux (or alternatives) is better for complex, shared global state.

Q4. What are the best practices for managing state in large React applications?
A4. Use local state for UI, Context for cross-cutting concerns, and external stores for complex global state.

Q5. How would you optimize performance in a React app with large component trees?
A5. Use memoization, code-splitting, virtualization, and avoid unnecessary re-renders.

Q6. Explain React's Strict Mode and its impact on development. A6. StrictMode highlights unsafe lifecycles, double-invokes effects, and warns about legacy patterns.

Q7. How can you prevent unnecessary re-renders in React functional components?
A7. Use React.memo, useCallback, useMemo, and avoid passing new object/array references unnecessarily.

Q8. Describe the key differences between functional and class components in React. A8. Functional components are simpler, hook-based, and preferred; class components are legacy but supported.

Q9. What is the significance of the React Fiber architecture?
A9. Fiber enables incremental rendering, prioritization, and concurrency for smoother UIs.

Q10. How does React handle side effects, and how can you manage them effectively?
A10. Side effects are handled with useEffect; manage cleanup and dependencies carefully.

---

## 🗂️ State Management

Q11. Explain the differences between useMemo() and useCallback() in React.
A11. useMemo caches computed values; useCallback caches function references.

Q12. How would you implement dynamic form handling and validation in React?
A12. Use controlled inputs with libraries like React Hook Form for scalable validation.

Q13. What is lazy loading in React, and how does it improve application performance?
A13. Lazy loading splits bundles and loads components only when needed.

Q14. How would you handle errors in a React app, and what is the role of error boundaries?
A14. Error boundaries catch render errors in child components and display fallback UI.

Q15. What are the benefits of server-side rendering (SSR) in React applications?
A15. SSR improves SEO, performance, and perceived load time.

Q16. How do you handle styling in React components? Discuss different approaches. A16. Options include CSS Modules, CSS-in-JS, Tailwind, or styled-components.

Q17. How would you pass data between sibling components in React without using Redux?
A17. Lift state up or use Context for sibling communication.

Q18. Explain the use case of useEffect() for fetching data from an API. A18. useEffect is ideal for fetching data on mount or dependency change.

Q19. How do you handle asynchronous operations in React using async/await or Promises?
A19. Use async/await inside effects or event handlers, with proper cleanup.

Q20. How would you re-render a component when the window is resized?
A20. Attach a resize listener in useEffect and update state on change.

Q21. Describe how React Context API can be used for state management in an app. A21. Context API shares state globally without prop drilling.

Q22. What is the role of React Router, and how does it work with dynamic routing?
A22. React Router maps URLs to components and supports dynamic params.

Q23. Explain the concept of controlled and uncontrolled components in React. A23. Controlled components bind value to state; uncontrolled rely on refs.

Q24. How would you optimize React app performance when handling large lists or grids?
A24. Use virtualization (react-window, react-virtualized).

Q25. Explain the difference between shallow and deep comparison in React's shouldComponentUpdate. A25. Shallow compares props/state; deep compares nested structures.

Q26. How do you handle asynchronous code execution and state updates in React?
A26. State updates are batched and async; use functional updates when relying on previous state.

Q27. How would you implement custom hooks to abstract logic in React?
A27. Encapsulate reusable logic in a function starting with use.

Q28. What are higher-order components (HOCs) in React, and how are they used?
A28. HOCs wrap components to inject props or behavior.

Q29. How would you implement a search feature with debouncing in React?
A29. Debounce input changes with setTimeout or lodash.

Q30. Explain React's reconciliation process and how it updates the DOM efficiently. A30. Reconciliation matches elements by keys and updates only changed nodes.

---

## 🚀 Advanced & Performance

Q31. How would you design a scalable folder and component architecture for a large React application?
A31. Organize by feature/domain, use atomic design, and enforce separation of concerns.

Q32. Compare Redux Toolkit, Zustand, and Recoil. A32. Redux Toolkit is boilerplate-free, Zustand is lightweight, Recoil is flexible but experimental.

Q33. How do you handle global state vs. local state trade-offs in a React application?
A33. Global state for cross-cutting concerns; local state for isolated UI.

Q34. What are the pitfalls of overusing Context API, and how can you mitigate them?
A34. Overuse causes re-renders; split contexts or memoize values.

Q35. Explain how Suspense works in React. A35. Suspense lets components wait for async data with fallback UI.

Q36. How does React’s concurrent rendering improve perceived performance?
A36. It allows interruptible rendering but may reorder updates unexpectedly.

Q37. What strategies would you use to optimize bundle size in a React application?
A37. Use tree-shaking, dynamic imports, and bundle analysis.

Q38. How would you implement infinite scrolling in React?
A38. Use IntersectionObserver with virtualization for performance.

Q39. How would you debug and fix memory leaks in React?
A39. Always clean up effects (e.g., unsubscribe in useEffect).

Q40. How do you handle race conditions in React async requests?
A40. Track request IDs or cancel stale promises.

---

## 🌍 SSR, Routing & Data

Q41. What are the trade-offs between Next.js and client-side rendering?
A41. Next.js offers SSR/SSG/ISR for SEO and performance; CSR is simpler but less SEO-friendly.

Q42. How would you implement authentication and authorization in React?
A42. Use route guards, context, or HOCs for protected routes.

Q43. What are the best practices for handling forms at scale in React?
A43. Use React Hook Form for performance or Formik for features.

Q44. How would you implement optimistic UI updates in React?
A44. Update state immediately, then roll back if the server fails.

Q45. How would you integrate React with GraphQL?
A45. Use Apollo/Relay for queries, caching, and normalization.

---

## ⚖️ Accessibility, Testing & UX

Q46. How do you ensure accessibility in React components?
A46. Use semantic HTML, ARIA roles, and tools like axe or Lighthouse.

Q47. How would you implement internationalization (i18n) in React?
A47. Use i18next or react-intl with context providers.

Q48. What strategies would you use to test React components?
A48. Unit test with Jest/RTL, integration with Cypress/Playwright.

Q49. How do you handle error logging and monitoring in production React apps?
A49. Use Sentry, LogRocket, or custom logging with error boundaries.

Q50. Imagine your React app’s performance degrades at scale. How do you fix
A50. Profile with React DevTools, Lighthouse, and Chrome Profiler; fix by memoization, virtualization, and reducing bundle size.

---

# 🤖 Cheat Sheets

## ✴️ JavaScript Core Concepts

### 🧠 Functions & Scope

Functions are the backbone of JS. Understanding scope and execution context helps you avoid bugs and write cleaner code.

| 📌 **Concept**            | 📖 **Explanation**                                        |
| ------------------------- | --------------------------------------------------------- |
| 🔒 Closure                | A function that remembers variables from its outer scope. |
| 🕶️ Shadowing              | Inner variable hides outer variable with the same name.   |
| 🗂️ Scope                  | Defines where a variable can be accessed.                 |
| 📍 Lexical Scope          | Scope is determined by where code is written, not called. |
| 🧱 Block Scope            | Variables with `let`/`const` exist only inside `{}`.      |
| 🧾 Execution Context      | The environment where JS code runs.                       |
| 📚 Call Stack             | Keeps track of function calls in order.                   |
| 🧩 Higher‑Order Function  | A function that takes/returns another function.           |
| 🧮 Pure Function          | Same input → same output, no side effects.                |
| 🧩 Currying               | Splitting a function into smaller, reusable functions.    |
| 🔄 Recursion              | A function that calls itself until a base case is met.    |
| 🧮 Tail Call Optimization | Optimized recursion that avoids growing the call stack.   |

### ⚡ Async & Concurrency

JavaScript is single‑threaded, but async patterns let you handle tasks like API calls, timers, and animations smoothly.
| 📌 **Concept** | 📖 **Explanation** |
| --- | --- |
| 📞 Callback | A function passed into another to run later. |
| 🤝 Promise | A placeholder for a value that will be ready in the future. |
| ⏳ Async/Await | Cleaner way to write async code instead of chaining `.then()`. |
| 🔄 Event Loop | Handles async tasks while keeping JS single‑threaded. |
| 🧵 Microtask Queue | Queue for promises (runs before normal tasks). |
| ⏱️ Debounce | Delay a function until user stops triggering it. |
| 🚦 Throttle | Limit how often a function runs over time. |
| 🧭 setTimeout | Runs a function once after a delay. |
| 🧭 setInterval | Runs a function repeatedly at fixed intervals. |
| 🧩 clearTimeout | Cancels a scheduled timeout. |
| 🧩 clearInterval | Stops a running interval. |
| 🧩 requestAnimationFrame | Optimized way to run animations in sync with screen refresh. |

### 🏗️ Objects & Prototypes

Objects are everywhere in JS. Prototypes and inheritance explain how properties and methods are shared.

| 📌 **Concept**                | 📖 **Explanation**                                               |
| ----------------------------- | ---------------------------------------------------------------- |
| 👤 `this`                     | Refers to the object that’s currently calling the function.      |
| 🧬 Prototype                  | Objects inherit from other objects via prototypes.               |
| 🧳 Inheritance                | One object reuses properties/methods from another.               |
| 🧩 Factory Function           | A function that returns new objects without `class`/`new`.       |
| 🏗️ Constructor Function       | Special function used with `new` to create objects.              |
| 🧑‍🏫 Class                      | Syntactic sugar over prototypes for object blueprints.           |
| 🧬 Super                      | Calls parent class constructor/methods.                          |
| 🧩 Mixins                     | Reuse functionality by copying methods into objects.             |
| 🧭 Composition                | Build objects by combining smaller parts instead of inheritance. |
| 🧑‍🤝‍🧑 Object.freeze              | Prevents object properties from being changed.                   |
| 🧭 Object.keys/values/entries | Get object properties, values, or pairs.                         |
| 🧩 Object.assign/fromEntries  | Copy or rebuild objects from key‑value pairs.                    |

### 📊 Data Types & Values

JS types can be tricky. Knowing how values behave prevents subtle bugs.

| 📌 **Concept**            | 📖 **Explanation**                                     |
| ------------------------- | ------------------------------------------------------ |
| 🔄 Type Coercion          | JS auto‑converts types (`"1" + 1 → "11"`).             |
| 🔧 Type Conversion        | Manually changing types (`Number("1")`).               |
| ✅ Truthy/Falsy           | Values that act like true/false in conditions.         |
| 🚫 Null vs Undefined      | Null = intentional empty, Undefined = not assigned.    |
| ❌ NaN                    | “Not a Number” result of invalid math.                 |
| ⚖️ == vs ===              | `==` checks value only, `===` checks value + type.     |
| 🧱 Primitive vs Reference | Primitives copy by value, objects/arrays by reference. |
| 🧩 Symbol                 | Unique, immutable value often used as object keys.     |
| 🧭 BigInt                 | Handles numbers larger than `Number.MAX_SAFE_INTEGER`. |
| 🧭 WeakRef                | Holds a weak reference to an object (GC‑friendly).     |
| 🧹 Garbage Collection     | JS automatically frees unused memory.                  |

### 🧩 Arrays & Collections

Arrays and collections are the workhorses of data manipulation.

| 📌 **Concept**     | 📖 **Explanation**                                  |
| ------------------ | --------------------------------------------------- |
| 🧮 Array.map       | Transforms each array element into a new array.     |
| 🧹 Array.filter    | Returns only elements that match a condition.       |
| 🧮 Array.reduce    | Accumulates array values into a single result.      |
| 🧾 Array.forEach   | Runs a function for each element (no return).       |
| 🧭 Array.find      | Returns the first element that matches a condition. |
| 🧩 Array.some      | Checks if at least one element matches.             |
| 🧩 Array.every     | Checks if all elements match.                       |
| 🧮 Array.flat      | Flattens nested arrays into one.                    |
| 🧾 Array.includes  | Checks if an array contains a value.                |
| 🧮 Map             | Stores key‑value pairs with any type of key.        |
| 📋 Set             | Stores unique values only.                          |
| 🧭 WeakMap/WeakSet | Like Map/Set but don’t prevent garbage collection.  |

### 🌐 DOM & Events

The DOM connects JS to the browser. Event handling is key for interactivity.

| 📌 **Concept**      | 📖 **Explanation**                                        |
| ------------------- | --------------------------------------------------------- |
| 🧭 Event Delegation | Attach one listener to a parent instead of many children. |
| 🧩 Event Bubbling   | Events move from child → parent.                          |
| 🧭 Event Capturing  | Events move from parent → child.                          |
| 🧩 Stop Propagation | Prevents an event from bubbling further.                  |
| 🧭 Prevent Default  | Stops default browser behavior (like form submit).        |
| 🧩 DOMContentLoaded | Event fired when HTML is fully loaded.                    |
| 🧭 Window.onload    | Event fired when page + resources are loaded.             |

### 🛠️ Language Features & Utilities

Modern JS comes with powerful features for cleaner, safer, and more expressive code.

| 📌 **Concept**        | 📖 **Explanation**                                    |
| --------------------- | ----------------------------------------------------- |
| 🌪️ Spread Operator    | Expands arrays/objects into individual elements.      |
| 📥 Rest Operator      | Collects multiple args into an array.                 |
| 🧩 Destructuring      | Pull values from arrays/objects into variables.       |
| 📝 Template Literals  | Strings with embedded expressions `` `Hi ${name}` ``. |
| ⚡ Short Circuit      | Logical ops return first truthy/falsy value.          |
| ❓ Optional Chaining  | Safely access nested props (`obj?.prop`).             |
| 🧑‍💻 Strict Mode        | Catches silent errors, enforces cleaner code.         |
| 🧩 Polyfill           | Code that adds missing features in older browsers.    |
| 🧭 Transpiler (Babel) | Converts modern JS into older JS for compatibility.   |
| 🧮 Generators         | Functions that can pause and resume (`function*`).    |
| 🧭 Intl API           | For formatting dates, numbers, currencies.            |
| 🧩 Proxy              | Wrapper around an object to intercept operations.     |
| 🧭 Reflect            | Built‑in object with methods for object operations.   |

### 📦 Modules & Performance

Modules and performance patterns help scale apps and keep them efficient.

| 📌 **Concept**    | 📖 **Explanation**                                  |
| ----------------- | --------------------------------------------------- |
| 🧭 Module         | A file that exports/imports code for reuse.         |
| 🧭 Default Import | Import one main export from a module.               |
| 🧩 Named Import   | Import specific exports from a module.              |
| 🧭 Dynamic Import | Load modules only when needed (`import()`).         |
| 🧩 Tree Shaking   | Removing unused code during bundling.               |
| 🧭 Lazy Loading   | Load resources only when needed.                    |
| 🧩 Service Worker | Script that runs in background for caching/offline. |
| 🧭 Web Worker     | Runs JS in a separate thread for heavy tasks.       |
| 🧩 IIFE           | Function that runs immediately after it’s defined.  |
| 🧾 JSON           | Lightweight format for storing & sending data.      |

---

## ⚛️ React Core Concepts

| 🧩 **Concept**                      | 📖 **Explanation**                                                                            |
| ----------------------------------- | --------------------------------------------------------------------------------------------- |
| 🏗️ React Limitations                | React is UI‑only; needs extra libs for routing, state, and architecture.                      |
| 🌳 Virtual DOM                      | React diffs a virtual tree with the real DOM → fewer, faster updates.                         |
| 🧵 Fiber                            | New engine for incremental, prioritized rendering → smoother UI.                              |
| 🔄 Reconciliation                   | Compares elements by keys, updates only what changed.                                         |
| 🚨 StrictMode                       | Highlights unsafe patterns, double‑invokes effects in dev.                                    |
| ⚡ Hooks vs Redux                   | Hooks fine for local/simple state; Redux/alternatives for complex global state.               |
| 🗂️ State Strategy                   | Local = UI, Context = cross‑cutting, Store = global/complex.                                  |
| 📦 Context Pitfall                  | Overuse causes re‑renders → split contexts or memoize values.                                 |
| 🛠️ Redux Toolkit / Zustand / Recoil | RTK = robust, Zustand = lightweight, Recoil = flexible but experimental.                      |
| 🧠 useMemo vs useCallback           | `useMemo` caches values, `useCallback` caches functions.                                      |
| 🧹 Side Effects                     | Managed with `useEffect`; always clean up subscriptions/timers.                               |
| 🚀 Performance                      | Use `React.memo`, virtualization, code‑splitting, bundle analysis.                            |
| 📜 Large Lists                      | Use virtualization (`react-window`, `react-virtualized`).                                     |
| 🧯 Memory Leaks                     | Always clean up effects to avoid stale listeners.                                             |
| ⚖️ Functional vs Class              | Functional + Hooks = modern; Class = legacy but supported.                                    |
| 🪝 Custom Hooks                     | Encapsulate reusable logic across components.                                                 |
| 🎭 HOCs                             | Wrap components to inject props/behavior.                                                     |
| 🎛️ Controlled vs Uncontrolled       | Controlled = state‑driven, Uncontrolled = ref‑driven.                                         |
| 🌐 Data Fetching                    | Use `useEffect` for API calls; handle cleanup + errors.                                       |
| ⏳ Suspense                         | Shows fallback UI while waiting for async data.                                               |
| 🔀 Race Conditions                  | Track request IDs or cancel stale promises.                                                   |
| 🔍 Debounce                         | Delay input handling with `setTimeout` or lodash debounce.                                    |
| ⚡ Optimistic UI                    | Update immediately, rollback if server fails.                                                 |
| 🛣️ React Router                     | Maps URL → Component, supports dynamic params.                                                |
| 🔐 Auth                             | Use route guards, Context, or HOCs for protected routes.                                      |
| 🌍 SSR Benefits                     | Faster load + SEO boost.                                                                      |
| ⚖️ Next.js vs CSR                   | Next.js \= SSR/SSG/ISR, CSR = simpler but weaker SEO.                                         |
| 🛡️ Error Boundaries                 | Catch render errors, show fallback UI.                                                        |
| 📊 Monitoring                       | Use Sentry, LogRocket, or custom logging.                                                     |
| ♿ Accessibility                    | Semantic HTML, ARIA roles, test with axe/Lighthouse.                                          |
| 🌏 i18n                             | Use i18next or react‑intl with providers.                                                     |
| 🧪 Testing                          | Jest + RTL for unit, Cypress/Playwright for E2E.                                              |
| 📏 Window Resize                    | Add listener in `useEffect`, update state.                                                    |
| 📉 Scaling Issues                   | Profile with DevTools/Lighthouse → fix with memoization, virtualization, bundle optimization. |

---

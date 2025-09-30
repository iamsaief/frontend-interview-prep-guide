<div align="center">
    <img height="60" src="https://img.icons8.com/color/344/javascript.png" />
    <img height="55" src="https://svgmix.com/uploads/e86a0a-react.svg" />
    <h1>🚀 The Ultimate Frontend Interview Prep Guide</h1>
</div>

আমি এই রিসোর্সটি তৈরি করেছি **শেখা, শেয়ার করা এবং কমিউনিটি গ্রোথ** 🌱 এর জন্য। যদি এটি আপনার কাজে লাগে, তবে একটি ⭐️ বা শেয়ার আমার জন্য অনেক বড় ব্যাপার হবে!

✨ শুভকামনা, **Happy coding!**

React ও JavaScript ইন্টারভিউ প্রস্তুতির জন্য ১০০+ Q&A ও cheat sheet। Frontend developer দের জন্য শেখা, রিভিশন ও ইন্টারভিউ ক্র্যাক করার গাইড।

<p align="center">
💬 In case you want to reach out or just say hi, ↩️ <br/>
<a href="https://www.facebook.com/saiefalemon">Facebook</a> | <a href="https://www.linkedin.com/in/saiefalemon">LinkedIn</a> | <a href="https://www.iamsaief.github.io.com/">Portfolio</a>
</p>

---

**🗂️ সূচিপত্র**

- [✴️ ৫০টা JavaScript Interview Q\&A](#️-৫০টা-javascript-interview-qa)
  - [🏗️ Core Concepts \& Fundamentals](#️-core-concepts--fundamentals)
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

# ✴️ ৫০টা JavaScript Interview Q&A

## 🏗️ Core Concepts & Fundamentals

Q1. var, let, আর const এর মধ্যে পার্থক্য কী?
A1. var function-scoped, hoisted হয়; let/const block-scoped; const reassign করা যায় না।

Q2. Hoisting কী?
A2. Variable আর function declaration execution-এর আগে scope-এর উপরে তুলে আনা হয়।

Q3. == আর === এর মধ্যে পার্থক্য কী?
A3. == type coercion করে, === strict type + value check করে।

Q4. Closure কী এবং কেন দরকার?
A4. Closure হলো function যেটা outer scope-এর variable মনে রাখে; data encapsulation আর state রাখার জন্য দরকার।

Q5. Scope কী?
A5. Variable কোথায় accessible হবে সেটা নির্ধারণ করে: global, function, block।

Q6. Synchronous vs Asynchronous code পার্থক্য কী?
A6. Sync line-by-line চলে; Async non-blocking হয় (callback, promise, async/await দিয়ে)।

Q7. Higher-order function কী?
A7. Function যেটা অন্য function নেয় বা return করে।

Q8. null vs undefined পার্থক্য কী?
A8. undefined = declare হয়েছে কিন্তু assign হয়নি; null = ইচ্ছাকৃত empty value।

Q9. Template literals কী?
A9. Backtick string যেটা interpolation আর multiline support করে।

Q10. Primitive vs Reference type পার্থক্য কী?
A10. Primitive immutable, value দিয়ে store হয়; Object/Array reference দিয়ে store হয়।

## 🗂️ Objects, Functions & Prototypes

Q11. Prototypal inheritance কীভাবে কাজ করে?
A11. Object তার prototype chain থেকে property/method পায়।

Q12. Function declaration vs expression পার্থক্য কী?
A12. Declaration hoisted হয়, expression হয় না।

Q13. Arrow function vs regular function পার্থক্য কী?
A13. Arrow-এর নিজস্ব this বা arguments নেই।

Q14. this keyword কী বোঝায়?
A14. Function যেই object execute করছে সেটাকে বোঝায়।

Q15. bind(), call(), apply() এর পার্থক্য কী?
A15. তিনটাই this সেট করে; call/apply সাথে সাথে invoke করে (apply array নেয়), bind নতুন function return করে।

Q16. IIFE কী?
A16. Immediately Invoked Function Expression, define হওয়ার সাথে সাথে execute হয়।

Q17. Shallow copy vs Deep copy পার্থক্য কী?
A17. Shallow reference copy করে; Deep nested object duplicate করে।

Q18. Array চেক করবেন কিভাবে?
A18. Array.isArray(obj) দিয়ে।

Q19. Object.freeze() vs Object.seal() পার্থক্য কী?
A19. freeze = add/remove/modify কিছুই করা যায় না; seal = add/remove করা যায় না, modify করা যায়।

Q20. Event delegation কী?
A20. Parent element-এ একটাই listener attach করে child event handle করা।

## 🚀 Asynchronous JavaScript

Q21. Promise কী?
A21. Async operation-এর eventual result represent করে।

Q22. async/await কী?
A22. Promise-এর উপর syntactic sugar, readable async code লেখার জন্য।

Q23. Event loop কীভাবে কাজ করে?
A23. Call stack আর callback queue manage করে async task execute করে।

Q24. Microtask vs Macrotask পার্থক্য কী?
A24. Microtask (Promise, MutationObserver) আগে চলে; Macrotask (setTimeout) পরে।

Q25. setTimeout vs setImmediate পার্থক্য কী?
A25. setTimeout delay পরে চলে; setImmediate current phase শেষে চলে (Node.js)।

Q26. Promise.all() vs Promise.race() পার্থক্য কী?
A26. all সব resolve/reject হওয়া পর্যন্ত wait করে; race প্রথম settle হওয়া promise return করে।

Q27. Callback hell কী?
A27. Nested callback structure → unreadable code; solution = Promise/async-await।

Q28. Concurrency vs Parallelism পার্থক্য কী?
A28. Concurrency = একসাথে multiple কাজ progress করে; Parallelism = একসাথে execute হয়।

Q29. Fetch request cancel করবেন কিভাবে?
A29. AbortController ব্যবহার করে।

Q30. Debounce vs Throttle পার্থক্য কী?
A30. Debounce = inactivity শেষে execute; Throttle = fixed interval-এ execute।

## 🌍 ES6+ Features

Q31. Default parameter কী?
A31. Function parameter-এর default value।

Q32. Rest vs Spread operator পার্থক্য কী?
A32. Rest argument collect করে array বানায়; Spread array/object expand করে।

Q33. Module কী?
A33. ES6 import/export দিয়ে modular code।

Q34. Generator কী?
A34. Function যেটা pause/resume হয় yield দিয়ে।

Q35. Symbol কী?
A35. Unique, immutable primitive, mostly object key হিসেবে।

Q36. Destructuring কী?
A36. Array/object থেকে value আলাদা variable-এ নেওয়া।

Q37. WeakMap vs WeakSet পার্থক্য কী?
A37. Weak reference রাখে, garbage collection-friendly।

Q38. Optional chaining কী?
A38. ?. দিয়ে nested property safely access করা যায়।

Q39. Nullish coalescing কী?
A39. ?? শুধু null/undefined হলে fallback দেয়।

Q40. Tagged template literal কী?
A40. Template literal custom function দিয়ে process করা।

## ⚖️ Advanced Concepts & Performance

Q41. Currying কী?
A41. Multi-arg function → nested single-arg function।

Q42. Memoization কী?
A42. Function result cache করে performance বাড়ানো।

Q43. Tail call optimization কী?
A43. Recursive call stack reuse করে memory save করা।

Q44. Service worker কী?
A44. Background script → caching, offline, push notification।

Q45. localStorage vs sessionStorage vs cookies পার্থক্য কী?
A45. localStorage স্থায়ী, sessionStorage tab-close এ clear হয়, cookies request-এর সাথে যায়।

Q46. `==` vs `Object.is()` পার্থক্য কী?
A46. `Object.is` `===` এর মতো, কিন্তু `NaN` আর -`0` ঠিকভাবে handle করে।

Q47. Garbage collection কীভাবে কাজ করে?
A47. Reachability check করে unreferenced object remove করে।

Q48. Event bubbling vs capturing পার্থক্য কী?
A48. Bubbling = child → parent, Capturing = parent → child।

Q49. `map()`, `forEach()`, `filter()`, `reduce()` পার্থক্য কী?
A49. map transform করে, forEach iterate করে, filter select করে, reduce accumulate করে।

Q50. Pure function কী?
A50. Side-effect ছাড়া, same input → same output দেয়।

---

# ⚛️ 50 React Interview Q&A

## 🏗️ Architecture & Core Concepts

Q1. React-এর limitation কী large-scale app বানানোর সময়?
A1. React শুধু UI library; routing, state management আর architecture-এর জন্য আলাদা solution লাগে।

Q2. React Virtual DOM কিভাবে কাজ করে?
A2. React Virtual DOM diff করে আগের tree-এর সাথে, তারপর minimal real DOM update করে।

Q3. Hooks কি পুরোপুরি Redux replace করতে পারে?
A3. ছোট app-এ পারে, কিন্তু complex global state-এর জন্য Redux বা alternative ভালো।

Q4. Large app-এ state manage করার best practice কী?
A4. Local state UI-এর জন্য, Context cross-cutting concern-এর জন্য, আর external store complex global state-এর জন্য।

Q5. Large component tree optimize করবেন কিভাবে?
A5. Memoization, code-splitting, virtualization, আর unnecessary re-render এড়ানো।

Q6. React StrictMode কী করে?
A6. Unsafe lifecycle detect করে, effect double invoke করে, আর legacy pattern warn করে।

Q7. Unnecessary re-render কিভাবে prevent করবেন?
A7. React.memo, useCallback, useMemo ব্যবহার করুন, আর নতুন object/array reference avoid করুন।

Q8. Functional vs Class component-এর পার্থক্য কী?
A8. Functional সহজ, hook-based, modern; Class legacy কিন্তু supported।

Q9. React Fiber architecture-এর গুরুত্ব কী?
A9. Fiber incremental rendering আর concurrency enable করে, UI smooth রাখে।

Q10. React side effect কিভাবে handle করে?
A10. useEffect দিয়ে, dependency আর cleanup ঠিকভাবে manage করতে হয়।

---

## 🗂️ State Management

Q11. useMemo vs useCallback পার্থক্য কী?
A11. useMemo value cache করে, useCallback function reference cache করে।

Q12. Dynamic form handling কিভাবে করবেন?
A12. Controlled input আর React Hook Form-এর মতো library ব্যবহার করুন।

Q13. Lazy loading কীভাবে কাজ করে?
A13. Component bundle split করে, দরকার হলে load করে।

Q14. Error boundary-এর কাজ কী?
A14. Render error catch করে fallback UI দেখায়।

Q15. SSR-এর সুবিধা কী?
A15. SEO, performance আর perceived load time improve করে।

Q16. React-এ styling-এর approach কী কী?
A16. CSS Modules, CSS-in-JS, Tailwind, styled-components।

Q17. Redux ছাড়া sibling component data pass করবেন কিভাবে?
A17. State lift up বা Context ব্যবহার করুন।

Q18. API fetch করার জন্য useEffect কিভাবে ব্যবহার করবেন?
A18. Mount বা dependency change হলে call করবেন।

Q19. Async operation কিভাবে handle করবেন?
A19. async/await বা Promise ব্যবহার করুন, cleanup সহ।

Q20. Window resize হলে component re-render করবেন কিভাবে?
A20. useEffect-এ resize listener add করে state update করবেন।

Q21. Context API state management-এ কিভাবে কাজ করে?
A21. Prop drilling ছাড়া global state share করে।

Q22. React Router-এর কাজ কী?
A22. URL map করে component render করে, dynamic param support করে।

Q23. Controlled vs Uncontrolled component পার্থক্য কী?
A23. Controlled state-driven, uncontrolled ref-driven।

Q24. Large list/grid optimize করবেন কিভাবে?
A24. Virtualization (react-window, react-virtualized) ব্যবহার করুন।

Q25. Shallow vs Deep comparison পার্থক্য কী?
A25. Shallow শুধু reference check করে, Deep nested structure check করে।

Q26. Async state update কিভাবে handle করবেন?
A26. React batch করে; previous state দরকার হলে functional update ব্যবহার করুন।

Q27. Custom hook কেন ব্যবহার করবেন?
A27. Reusable logic encapsulate করার জন্য।

Q28. HOC কীভাবে কাজ করে?
A28. Component wrap করে extra props/behavior দেয়।

Q29. Debounced search কিভাবে করবেন?
A29. setTimeout বা lodash debounce ব্যবহার করুন।

Q30. Reconciliation কীভাবে কাজ করে?
A30. Key দিয়ে element match করে, শুধু changed node update করে।

---

## 🚀 Advanced & Performance

Q31. Large app-এর জন্য folder structure কেমন হওয়া উচিত?
A31. Feature/domain-based, atomic design follow করুন।

Q32. Redux Toolkit vs Zustand vs Recoil?
A32. RTK boilerplate-free, Zustand lightweight, Recoil flexible কিন্তু experimental।

Q33. Global vs Local state trade-off কী?
A33. Global cross-cutting concern-এর জন্য, Local isolated UI-এর জন্য।

Q34. Context overuse-এর সমস্যা কী?
A34. Re-render বাড়ে; context split বা memoization ব্যবহার করুন।

Q35. Suspense কীভাবে কাজ করে?
A35. Async data আসা পর্যন্ত fallback UI দেখায়।

Q36. Concurrent rendering-এর সুবিধা কী?
A36. UI responsive রাখে, তবে update reorder হতে পারে।

Q37. Bundle size optimize করবেন কিভাবে?
A37. Tree-shaking, dynamic import, bundle analyzer ব্যবহার করুন।

Q38. Infinite scroll কিভাবে করবেন?
A38. IntersectionObserver + virtualization ব্যবহার করুন।

Q39. Memory leak কিভাবে fix করবেন?
A39. Effect cleanup (unsubscribe, clearTimeout) করতে হবে।

Q40. Async race condition কিভাবে handle করবেন?
A40. Request ID track করুন বা stale promise cancel করুন।

---

## 🌍 SSR, Routing & Data

Q41. Next.js vs CSR trade-off কী?
A41. Next.js SEO/performance ভালো, CSR simple কিন্তু SEO দুর্বল।

Q42. Auth flow কিভাবে implement করবেন?
A42. Route guard, Context বা HOC ব্যবহার করুন।

Q43. Large form handle করার best practice কী?
A43. React Hook Form performant, Formik feature-rich।

Q44. Optimistic UI update কিভাবে করবেন?
A44. State আগে update করুন, fail হলে rollback করুন।

Q45. React + GraphQL integration কিভাবে করবেন?
A45. Apollo/Relay দিয়ে query, cache, normalization manage করুন।

---

## ⚖️ Accessibility, Testing & UX

Q46. Accessibility নিশ্চিত করবেন কিভাবে?
A46. Semantic HTML, ARIA role, axe/Lighthouse ব্যবহার করুন।

Q47. i18n কিভাবে implement করবেন?
A47. i18next বা react-intl context provider দিয়ে।

Q48. React test strategy কী?
A48. Jest/RTL unit test, Cypress/Playwright integration test।

Q49. Error logging/monitoring কিভাবে করবেন?
A49. Sentry, LogRocket বা custom logger + error boundary।

Q50. Scale-এ performance degrade হলে কী করবেন?
A50. React DevTools, Profiler, Lighthouse দিয়ে bottleneck খুঁজে memoization, virtualization, bundle optimize করবেন।

---

# 🤖 Cheat Sheets

## ✴️ JavaScript Core Concepts

### 🧠 Functions & Scope

Functions হলো JS এর backbone। Scope আর Execution Context বুঝলে bug কম হবে আর code হবে পরিষ্কার।

| 📌 **Concept**            | 📖 **Explanation**                                               |
| ------------------------- | ---------------------------------------------------------------- |
| 🔒 Closure                | একটা function যেটা outer scope এর variable মনে রাখে।             |
| 🕶️ Shadowing              | Inner variable বাইরের একই নামের variable কে ঢেকে ফেলে।           |
| 🗂️ Scope                  | Variable কোথায় access করা যাবে সেটা define করে।                  |
| 📍 Lexical Scope          | Scope নির্ধারণ হয় code কোথায় লেখা হয়েছে তার উপর।                 |
| 🧱 Block Scope            | `let`/`const` দিয়ে declare করা variable শুধু `{}` এর ভেতরে থাকে। |
| 🧾 Execution Context      | JS code কোন environment এ run হচ্ছে সেটা।                        |
| 📚 Call Stack             | Function call গুলো কোন order এ হচ্ছে তার list।                   |
| 🧩 Higher‑Order Function  | Function যেটা আরেকটা function নেয় বা return করে।                 |
| 🧮 Pure Function          | Same input দিলে same output দেয়, কোনো side effect নেই।           |
| 🧩 Currying               | বড় function কে ছোট ছোট reusable function এ ভাঙা।                 |
| 🔄 Recursion              | Function নিজেকে নিজেই call করে যতক্ষণ না base case আসে।          |
| 🧮 Tail Call Optimization | Recursion optimize করে যাতে call stack না বাড়ে।                  |

---

### ⚡ Async & Concurrency

JavaScript single‑threaded, কিন্তু async pattern দিয়ে API call, timer, animation smooth ভাবে handle করা যায়।

| 📌 **Concept**           | 📖 **Explanation**                                             |
| ------------------------ | -------------------------------------------------------------- |
| 📞 Callback              | Function যেটা আরেকটা function এ pass করা হয় পরে run করার জন্য। |
| 🤝 Promise               | Future এ কোনো value আসবে তার placeholder।                      |
| ⏳ Async/Await           | Async code সহজে লেখার syntax, `.then()` chain এর বিকল্প।       |
| 🔄 Event Loop            | Async task manage করে JS কে single‑threaded রেখেও।             |
| 🧵 Microtask Queue       | Promise আর async event এর queue (normal task এর আগে run হয়)।   |
| ⏱️ Debounce              | Function delay করে যতক্ষণ না user trigger বন্ধ করে।            |
| 🚦 Throttle              | Function কে নির্দিষ্ট সময় gap এ সীমাবদ্ধ করে।                  |
| 🧭 setTimeout            | Delay দিয়ে একবার function run করে।                             |
| 🧭 setInterval           | নির্দিষ্ট সময় gap এ বারবার function run করে।                   |
| 🧩 clearTimeout          | setTimeout cancel করে।                                         |
| 🧩 clearInterval         | setInterval বন্ধ করে।                                          |
| 🧩 requestAnimationFrame | Screen refresh এর সাথে sync করে animation run করে।             |

---

### 🏗️ Objects & Prototypes

JS এ সবকিছু প্রায় Object। Prototype আর Inheritance দিয়ে property/method share হয়।

| 📌 **Concept**                | 📖 **Explanation**                                         |
| ----------------------------- | ---------------------------------------------------------- |
| 👤 `this`                     | Function কে যে object call করছে সেটা refer করে।            |
| 🧬 Prototype                  | Object অন্য object থেকে property/method inherit করে।       |
| 🧳 Inheritance                | এক object আরেকটার property/method reuse করে।               |
| 🧩 Factory Function           | Function যেটা `class`/`new` ছাড়া নতুন object return করে।   |
| 🏗️ Constructor Function       | Function যেটা `new` দিয়ে object বানাতে use হয়।             |
| 🧑‍🏫 Class                      | Prototype এর উপর syntactic sugar, object blueprint বানাতে। |
| 🧬 Super                      | Parent class এর constructor/method call করে।               |
| 🧩 Mixins                     | Method copy করে object এ reuse করা।                        |
| 🧭 Composition                | Inheritance এর বদলে ছোট ছোট অংশ combine করে object বানানো। |
| 🧑‍🤝‍🧑 Object.freeze              | Object এর property পরিবর্তন আটকায়।                         |
| 🧭 Object.keys/values/entries | Object এর property নাম, value বা pair বের করে।             |
| 🧩 Object.assign/fromEntries  | Key‑value pair থেকে object copy বা rebuild করে।            |

---

### 📊 Data Types & Values

JS types tricky হতে পারে। Value কিভাবে behave করে সেটা জানলে bug কম হয়।

| 📌 **Concept**            | 📖 **Explanation**                                            |
| ------------------------- | ------------------------------------------------------------- |
| 🔄 Type Coercion          | JS auto‑convert করে type (`"1" + 1 → "11"`)।                  |
| 🔧 Type Conversion        | Manually type change করা (`Number("1")`)।                     |
| ✅ Truthy/Falsy           | Value যেগুলো condition এ true/false behave করে।               |
| 🚫 Null vs Undefined      | Null = ইচ্ছাকৃত empty, Undefined = assign করা হয়নি।           |
| ❌ NaN                    | Invalid math এর result (“Not a Number”)।                      |
| ⚖️ == vs ===              | `==` শুধু value check করে, `===` value + type check করে।      |
| 🧱 Primitive vs Reference | Primitive copy হয় value দিয়ে, object/array হয় reference দিয়ে। |
| 🧩 Symbol                 | Unique, immutable value, object key হিসেবে use হয়।            |
| 🧭 BigInt                 | `Number.MAX_SAFE_INTEGER` এর চেয়ে বড় সংখ্যা handle করে।       |
| 🧭 WeakRef                | Weak reference ধরে রাখে (GC‑friendly)।                        |
| 🧹 Garbage Collection     | JS unused memory free করে দেয়।                                |

---

### 🧩 Arrays & Collections

Array আর collection data manipulate করার মূল হাতিয়ার।

| 📌 **Concept**     | 📖 **Explanation**                                        |
| ------------------ | --------------------------------------------------------- |
| 🧮 Array.map       | প্রতিটি element কে transform করে নতুন array বানায়।        |
| 🧹 Array.filter    | Condition মিলে এমন element গুলো return করে।               |
| 🧮 Array.reduce    | Array এর value গুলোকে accumulate করে single result বানায়। |
| 🧾 Array.forEach   | প্রতিটি element এর জন্য function run করে (return দেয় না)। |
| 🧭 Array.find      | Condition মিলে প্রথম element return করে।                  |
| 🧩 Array.some      | অন্তত একটাতে condition true হলে true দেয়।                 |
| 🧩 Array.every     | সব element condition মিলে গেলে true দেয়।                  |
| 🧮 Array.flat      | Nested array কে এক লেভেলে flatten করে।                    |
| 🧾 Array.includes  | Array এর মধ্যে value আছে কিনা check করে।                  |
| 🧮 Map             | Key‑value pair store করে (key যেকোনো type হতে পারে)।      |
| 📋 Set             | Unique value store করে।                                   |
| 🧭 WeakMap/WeakSet | Map/Set এর মতো কিন্তু GC prevent করে না।                  |

---

### 🌐 DOM & Events

DOM JS কে browser এর সাথে connect করে। Event handling interactivity এর জন্য জরুরি।

| 📌 **Concept**      | 📖 **Explanation**                                           |
| ------------------- | ------------------------------------------------------------ |
| 🧭 Event Delegation | Parent element এ একবার listener attach করে child handle করা। |
| 🧩 Event Bubbling   | Event child → parent এ propagate হয়।                         |
| 🧭 Event Capturing  | Event parent → child এ propagate হয়।                         |
| 🧩 Stop Propagation | Event propagation বন্ধ করে।                                  |
| 🧭 Prevent Default  | Browser এর default behavior (যেমন form submit) আটকায়।        |
| 🧩 DOMContentLoaded | HTML পুরো load হলে event fire হয়।                            |
| 🧭 Window.onload    | Page + resource load হলে event fire হয়।                      |

---

### 🛠️ Language Features & Utilities

Modern JS এ অনেক feature আছে code clean, safe আর expressive করার জন্য।

| 📌 **Concept**        | 📖 **Explanation**                                         |
| --------------------- | ---------------------------------------------------------- |
| 🌪️ Spread Operator    | Array/object কে individual element এ expand করে।           |
| 📥 Rest Operator      | Extra argument গুলোকে array তে collect করে।                |
| 🧩 Destructuring      | Array/object থেকে value আলাদা variable এ নেয়া।             |
| 📝 Template Literals  | String এর মধ্যে expression embed করা `` `Hi ${name}` ``।   |
| ⚡ Short Circuit      | Logical operator প্রথম truthy/falsy value return করে।      |
| ❓ Optional Chaining  | Nested property safely access করা (`obj?.prop`)।           |
| 🧑‍💻 Strict Mode        | Silent error ধরতে সাহায্য করে, clean code enforce করে।     |
| 🧩 Polyfill           | পুরনো browser এ missing feature add করার code।             |
| 🧭 Transpiler (Babel) | Modern JS কে পুরনো JS এ convert করে compatibility এর জন্য। |
| 🧮 Generators         | Function pause/resume করতে পারে (`function*`)।             |
| 🧭 Intl API           | Date, number, currency format করার জন্য।                   |
| 🧩 Proxy              | Object এর operation intercept করার wrapper।                |
| 🧭 Reflect            | Object operation এর জন্য built‑in method।                  |

---

### 📦 Modules & Performance

Modules আর performance pattern বড় app scale করতে আর efficient রাখতে সাহায্য করে।

| 📌 **Concept**    | 📖 **Explanation**                                    |
| ----------------- | ----------------------------------------------------- |
| 🧭 Module         | আলাদা file যেটা code export/import করে reuse করা যায়। |
| 🧭 Default Import | Module থেকে main export import করা।                   |
| 🧩 Named Import   | Module থেকে নির্দিষ্ট export import করা।              |
| 🧭 Dynamic Import | দরকার হলে runtime এ module load করা (`import()`)।     |
| 🧩 Tree Shaking   | Unused code bundle থেকে remove করা।                   |
| 🧭 Lazy Loading   | Resource শুধু দরকার হলে load করা।                     |
| 🧩 Service Worker | Background এ run হয়, caching/offline support দেয়।     |
| 🧭 Web Worker     | আলাদা thread এ JS run করে heavy কাজের জন্য।           |
| 🧩 IIFE           | Function define করার সাথে সাথে run হয়।                |
| 🧾 JSON           | Lightweight format data store আর send করার জন্য।      |

---

## ⚛️ React Core Concepts

| 🧩 **Concept**                | 📖 **Explanation (বাংলা)**                                                                    |
| ----------------------------- | --------------------------------------------------------------------------------------------- |
| 🏗️ React Limitations          | React শুধু UI library; routing, state management আর architecture-এর জন্য আলাদা solution লাগে। |
| 🌳 Virtual DOM                | React Virtual DOM diff করে real DOM-এর সাথে → কম update, দ্রুত performance।                   |
| 🧵 Fiber                      | Incremental + prioritized rendering করে UI smooth রাখে।                                       |
| 🔄 Reconciliation             | Key দিয়ে element match করে, শুধু পরিবর্তিত node update করে।                                   |
| 🚨 StrictMode                 | Unsafe pattern detect করে, effect double invoke করে dev mode-এ।                               |
| ⚡ Hooks vs Redux             | ছোট app-এ Hooks যথেষ্ট; বড়/complex global state-এর জন্য Redux বা alternative দরকার।           |
| 🗂️ State Strategy             | Local = UI state, Context = cross-cutting concern, Store = global/complex state।              |
| 📦 Context Pitfall            | বেশি ব্যবহার করলে re-render বাড়ে → context split/memoize করতে হবে।                            |
| 🛠️ RTK / Zustand / Recoil     | RTK = robust, Zustand = lightweight, Recoil = flexible কিন্তু experimental।                   |
| 🧠 useMemo vs useCallback     | `useMemo` value cache করে, `useCallback` function cache করে।                                  |
| 🧹 Side Effects               | `useEffect` দিয়ে handle হয়; সবসময় cleanup করতে হবে।                                           |
| 🚀 Performance                | `React.memo`, virtualization, code-splitting, bundle analysis ব্যবহার করুন।                   |
| 📜 Large Lists                | Virtualization (`react-window`, `react-virtualized`) ব্যবহার করুন।                            |
| 🧯 Memory Leaks               | Effect cleanup (unsubscribe/clearTimeout) না করলে leak হয়।                                    |
| ⚖️ Functional vs Class        | Functional + Hooks modern, Class legacy কিন্তু supported।                                     |
| 🪝 Custom Hooks               | Reusable logic encapsulate করার জন্য।                                                         |
| 🎭 HOCs                       | Component wrap করে extra props/behavior দেয়।                                                  |
| 🎛️ Controlled vs Uncontrolled | Controlled = state-driven, Uncontrolled = ref-driven।                                         |
| 🌐 Data Fetching              | `useEffect` দিয়ে API call করুন; cleanup + error handle করুন।                                  |
| ⏳ Suspense                   | Async data আসা পর্যন্ত fallback UI দেখায়।                                                     |
| 🔀 Race Conditions            | Request ID track করুন বা stale promise cancel করুন।                                           |
| 🔍 Debounce                   | Input delay করতে `setTimeout` বা lodash debounce ব্যবহার করুন।                                |
| ⚡ Optimistic UI              | আগে state update করুন, fail হলে rollback করুন।                                                |
| 🛣️ React Router               | URL → Component map করে, dynamic param support করে।                                           |
| 🔐 Auth                       | Route guard, Context বা HOC দিয়ে protected route করুন।                                        |
| 🌍 SSR Benefits               | SEO + faster load time দেয়।                                                                   |
| ⚖️ Next.js vs CSR             | Next.js \= SSR/SSG/ISR, CSR = simple কিন্তু SEO দুর্বল।                                       |
| 🛡️ Error Boundaries           | Render error catch করে fallback UI দেখায়।                                                     |
| 📊 Monitoring                 | Sentry, LogRocket বা custom logger ব্যবহার করুন।                                              |
| ♿ Accessibility              | Semantic HTML, ARIA role, axe/Lighthouse দিয়ে test করুন।                                      |
| 🌏 i18n                       | i18next বা react-intl provider দিয়ে multi-locale support করুন।                                |
| 🧪 Testing                    | Jest + RTL unit test, Cypress/Playwright integration/E2E।                                     |
| 📏 Window Resize              | `useEffect`\-এ listener add করে state update করুন।                                            |
| 📉 Scaling Issues             | DevTools/Lighthouse দিয়ে profile → memoization, virtualization, bundle optimize করুন।         |

<div align="center">
    <img height="40" src="https://upload.wikimedia.org/wikipedia/commons/9/99/Unofficial_JavaScript_logo_2.svg" />&nbsp;
    <img height="40" src="https://upload.wikimedia.org/wikipedia/commons/a/a7/React-icon.svg" />
    <h1>🚀 The Ultimate Frontend Interview Prep Guide</h1>
</div>

React ও JavaScript ইন্টারভিউ প্রস্তুতির জন্য ১০০+ Q&A ও cheat sheet। Frontend developer দের জন্য শেখা, রিভিশন ও ইন্টারভিউ ক্র্যাক করার গাইড।

আমি এই রিসোর্সটি তৈরি করেছি **শেখা, শেয়ার করা এবং কমিউনিটি গ্রোথ** 🌱 এর জন্য। যদি এটি আপনার কাজে লাগে, তবে একটি ⭐️ বা শেয়ার আমার জন্য অনেক বড় ব্যাপার হবে!

✨ শুভকামনা, **Happy coding!**

<p align="center">
💬 In case you want to reach out or just say hi, ↩️ <br/>
<a href="https://www.facebook.com/saiefalemon">Facebook</a> | <a href="https://www.linkedin.com/in/saiefalemon">LinkedIn</a> | <a href="https://iamsaief.github.io/">Portfolio</a>
</p>

---

**🗂️ সূচিপত্র**

- [✴️ 50 JavaScript Interview Q\&A](#️-50-javascript-interview-qa)
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

# ✴️ 50 JavaScript Interview Q&A

## 🏗️ Core Concepts & Fundamentals

**Q1. `var`, `let`, আর `const` এর মধ্যে পার্থক্য কী?**

👉 `var` function-scoped আর hoisted হয়, তাই block এর বাইরে থেকেও access করা যায়। `let` আর `const` block-scoped, মানে শুধুমাত্র {} এর ভেতরে কাজ করে। তবে `const` দিয়ে declare করলে reassign করা যায় না।

```js
var a = 1;
let b = 2;
const c = 3;
```

**Q2. Hoisting কী?**

👉 Hoisting মানে হলো variable আর function declaration execution-এর আগে scope-এর উপরে উঠে যায়। তাই declare করার আগেও access করা যায়, যদিও value `undefined` থাকবে।

```js
console.log(a); // undefined
var a = 5;
```

**Q3. `==` আর `===` এর মধ্যে পার্থক্য কী?**

👉 `==` type coercion করে অর্থাৎ আলাদা type হলে convert করে compare করে। `===` strict equality check করে, মানে value আর type দুটোই একই হতে হবে।

```js
5 == "5"; // true
5 === "5"; // false
```

**Q4. Closure কী এবং কেন দরকার?**

👉 Closure হলো function যেটা তার outer scope-এর variable মনে রাখে, এমনকি সেই scope শেষ হলেও। এটি data encapsulation বা private variable তৈরি করতে সাহায্য করে।

```js
function counter() {
  let count = 0;
  return () => ++count;
}
const c = counter();
console.log(c()); // 1
```

**Q5. Scope কী?**

👉 Scope বলে দেয় কোন variable কোথায় access করা যাবে। Global scope পুরো কোডে কাজ করে, function scope শুধু function এর মধ্যে, আর block scope `{}` এর মধ্যে সীমাবদ্ধ থাকে।

```js
let x = 1;
function test() {
  let y = 2;
}
```

**Q6. Synchronous vs Asynchronous code পার্থক্য কী?**

👉 Synchronous code line-by-line execute হয়, তাই একটি কাজ শেষ না হলে পরেরটা শুরু হয় না। Asynchronous code non-blocking হয়, যেমন callback, promise, async/await ব্যবহার করে parallel এ কাজ করা যায়।

```js
console.log("1");
setTimeout(() => console.log("2"), 0);
console.log("3");
// Output: 1,3,2
```

**Q7. Higher-order function কী?**

👉 Higher-order function হলো function যেটা অন্য function কে argument হিসেবে নেয় বা return করে। এগুলো functional programming-এ অনেক ব্যবহার হয়।

```js
const apply = (fn, x) => fn(x);
apply((n) => n * 2, 5); // 10
```

**Q8. `null` vs `undefined` পার্থক্য কী?**

👉 `undefined` মানে variable declare হয়েছে কিন্তু কোনো value assign হয়নি। `null` মানে developer ইচ্ছাকৃতভাবে empty বা "কিছু নেই" value দিয়েছে।

```js
let a; // undefined
let b = null; // null
```

**Q9. Template literals কী?**

👉 Template literals হলো backtick string, যেখানে variable interpolation (`${}`) করা যায় এবং multiline string লিখতে সুবিধা হয়।

```js
let name = "Saief";
console.log(`Hello ${name} Welcome!`);
```

**Q10. Primitive vs Reference type পার্থক্য কী?**

👉 Primitive (string, number, boolean ইত্যাদি) immutable এবং value দিয়ে store হয়। Reference type (object, array) memory reference দিয়ে store হয়, তাই copy করলে reference share হয়।

```js
let x = 5;
let y = x;
y = 10; // x = 5
let arr = [1];
let arr2 = arr;
arr2.push(2); // arr = [1,2]
```

## 🗂️ Objects, Functions & Prototypes

**Q11. Prototypal inheritance কীভাবে কাজ করে?**

👉 JavaScript এ object তার prototype chain থেকে property আর method access করে। এটি OOP এর inheritance এর মত কাজ করে।

```js
const parent = {
  greet() {
    return "hi";
  },
};
const child = Object.create(parent);
console.log(child.greet()); // "hi"
```

**Q12. Function declaration vs expression পার্থক্য কী?**

👉 Function declaration hoisting হয়, তাই আগে লিখলেও পরে ব্যবহার করা যায়। Function expression variable এর মতো behave করে, তাই আগে call করলে error হবে।

```js
foo(); // works
function foo() {}

bar(); // error
const bar = function () {};
```

**Q13. Arrow function vs regular function পার্থক্য কী?**

👉 Arrow function এর নিজস্ব `this` বা `arguments` থাকে না, outer scope থেকে নেয়। Regular function নিজের `this` context পায়।

```js
const obj = {
  val: 10,
  reg: function () {
    return this.val;
  },
  arr: () => this.val,
};
console.log(obj.reg()); // 10
console.log(obj.arr()); // undefined
```

**Q14. `this` keyword কী বোঝায়?**

👉 `this` সেই object কে refer করে যেটার মাধ্যমে function call হয়েছে। Execution context অনুযায়ী এর মান আলাদা হয়।

```js
function show() {
  console.log(this.name);
}
const user = { name: "Saief", show };
user.show(); // "Saief"
```

**Q15. `bind()`, `call()`, `apply()` এর পার্থক্য কী?**

👉 তিনটাই `this` context সেট করে। `call` এবং `apply` function সাথে সাথে invoke করে, শুধু `apply` arguments array নেয়। `bind` নতুন function return করে যা পরে call করা যায়।

```js
function greet(msg) {
  console.log(msg, this.name);
}
const user = { name: "Saief" };
greet.call(user, "Hi"); // Hi Saief
greet.apply(user, ["Yo"]); // Yo Saief
const fn = greet.bind(user, "Hello");
fn(); // Hello Saief
```

**Q16. IIFE কী?**

👉 IIFE মানে Immediately Invoked Function Expression। Function define হওয়ার সাথে সাথে execute হয়, যাতে আলাদা scope তৈরি হয়।

```js
(function () {
  console.log("IIFE run");
})();
```

**Q17. Shallow copy vs Deep copy পার্থক্য কী?**

👉 Shallow copy শুধু প্রথম লেভেলের reference copy করে। Deep copy পুরো nested object কে duplicate করে যাতে মূল object পরিবর্তন হলেও copy তে প্রভাব না পড়ে।

```js
let obj = { a: 1, b: { c: 2 } };
let shallow = { ...obj };
shallow.b.c = 99;
console.log(obj.b.c); // 99 (shallow effect)
```

**Q18. Array চেক করবেন কিভাবে?**

👉 `Array.isArray(obj)` দিয়ে check করা যায়। অন্য method যেমন `instanceof Array` ব্যবহার করলে কিছু ক্ষেত্রে সঠিক নাও হতে পারে।

```js
Array.isArray([1, 2]); // true
Array.isArray("hi"); // false
```

**Q19. `Object.freeze()` vs `Object.seal()` পার্থক্য কী?**

👉 `Object.freeze()` করলে object এর property add, remove, modify কিছুই করা যায় না। `Object.seal()` এ add/remove করা যায় না কিন্তু modify করা যায়।

```js
const obj = { a: 1 };
Object.freeze(obj);
obj.a = 2; // no effect
```

**Q20. Event delegation কী?**

👉 Event delegation হলো parent element-এ একটি event listener বসানো, যা bubbling এর মাধ্যমে child elements এর event handle করে। এটি performance বাড়ায়।

```js
document.getElementById("list").addEventListener("click", (e) => {
  if (e.target.tagName === "LI") console.log(e.target.textContent);
});
```

## 🚀 Asynchronous JavaScript

**Q21. Promise কী?**

👉 Promise হলো async operation এর eventual result represent করার object। এর তিনটি state থাকে: pending, resolved, rejected।

```js
const p = new Promise((res, rej) => res("done"));
p.then(console.log); // "done"
```

**Q22. async/await কী?**

👉 async/await হলো promise এর syntactic sugar, যা asynchronous code কে synchronous এর মতো readable করে।

```js
async function getData() {
  const res = await fetch("/api");
  return res.json();
}
```

**Q23. Event loop কীভাবে কাজ করে?**

👉 Event loop call stack আর callback queue manage করে। যখন stack খালি হয়, তখন queue থেকে async callback execute হয়।

```js
console.log("1");
setTimeout(() => console.log("2"), 0);
console.log("3"); // Output: 1,3,2
```

**Q24. Microtask vs Macrotask পার্থক্য কী?**

👉 Microtask (Promise, MutationObserver) সবসময় আগে execute হয়। Macrotask যেমন setTimeout event loop এর পরের cycle এ চলে।

```js
Promise.resolve().then(() => console.log("micro"));
setTimeout(() => console.log("macro"), 0);
// Output: micro, macro
```

**Q25. `setTimeout` vs `setImmediate` পার্থক্য কী?**

👉 `setTimeout` নির্দিষ্ট delay পরে চলে। `setImmediate` current phase শেষ হলে চলে, তবে এটা Node.js specific।

**Q26. `Promise.all()` vs `Promise.race()` পার্থক্য কী?**

👉 `Promise.all()` সব promise resolve/reject না হওয়া পর্যন্ত wait করে। `Promise.race()` প্রথম যেটা settle হয় সেটা return করে।

```js
Promise.all([p1, p2]).then(console.log);
Promise.race([p1, p2]).then(console.log);
```

**Q27. Callback hell কী?**

👉 যখন অনেক nested callback ব্যবহার হয় তখন code unreadable হয়। এর সমাধান হলো Promise বা async/await।

```js
// Callback hell
doA(() => doB(() => doC(() => console.log("done"))));
```

**Q28. Concurrency vs Parallelism পার্থক্য কী?**

👉 Concurrency মানে একসাথে multiple কাজ progress করে, কিন্তু একসাথে execute না-ও হতে পারে। Parallelism মানে কাজগুলো একসাথে execute হয়।

**Q29. Fetch request cancel করবেন কিভাবে?**

👉 `AbortController` ব্যবহার করে request cancel করা যায়। এটি long running বা অপ্রয়োজনীয় request এ কাজে লাগে।

```js
const controller = new AbortController();
fetch("/api", { signal: controller.signal });
controller.abort();
```

**Q30. Debounce vs Throttle পার্থক্য কী?**

👉 Debounce মানে event trigger বারবার হলে শেষে একবার execute হবে। Throttle মানে নির্দিষ্ট interval এ event limit করা হয়।

```js
function debounce(fn, delay) {
  let t;
  return (...a) => {
    clearTimeout(t);
    t = setTimeout(() => fn(...a), delay);
  };
}
```

## 🌍 ES6+ Features

**Q31. Default parameter কী?**

👉 Function parameter এ default value assign করা যায়, যদি কোনো argument না দেওয়া হয়।

```js
function greet(name = "Guest") {
  console.log("Hello", name);
}
greet(); // Hello Guest
```

**Q32. Rest vs Spread operator পার্থক্য কী?**

👉 Rest operator function এর arguments কে array এ collect করে। Spread operator array/object কে expand করে অন্য array/object এ ব্যবহার করে।

```js
function sum(...nums) {
  return nums.reduce((a, b) => a + b, 0);
}
console.log(sum(1, 2, 3)); // 6

const arr = [1, 2];
const arr2 = [...arr, 3];
```

**Q33. Module কী?**

👉 Module মানে code কে আলাদা file এ ভাগ করে ES6 `import`/`export` এর মাধ্যমে reusable করা।

```js
// math.js
export const add = (a, b) => a + b;
// main.js
import { add } from "./math.js";
```

**Q34. Generator কী?**

👉 Generator হলো function যেটা pause এবং resume হতে পারে `yield` দিয়ে, যা asynchronous flow manage করতে সহায়ক।

```js
function* gen() {
  yield 1;
  yield 2;
}
const g = gen();
console.log(g.next().value); // 1
```

**Q35. Symbol কী?**

👉 Symbol হলো unique আর immutable primitive value, যা সাধারণত object এর unique property key হিসেবে ব্যবহার করা হয়।

```js
const id = Symbol("id");
const user = { [id]: 123 };
```

**Q36. Destructuring কী?**

👉 Destructuring দিয়ে array/object থেকে মান সহজে আলাদা variable এ assign করা যায়।

```js
const [a, b] = [1, 2];
const { name, age } = { name: "Saief", age: 28 };
```

**Q37. WeakMap vs WeakSet পার্থক্য কী?**

👉 WeakMap এবং WeakSet এ object এর weak reference থাকে, garbage collection এ automatically remove হয়ে যায়।

**Q38. Optional chaining কী?**

👉 Optional chaining (`?.`) দিয়ে nested property access করা যায় safely, error ছাড়াই।

```js
const user = { profile: { name: "Saief" } };
console.log(user.profile?.name); // Saief
```

**Q39. Nullish coalescing কী?**

👉 `??` operator null বা undefined হলে fallback value দেয়, কিন্তু false বা 0 হলে দেয় না।

```js
let x = null;
console.log(x ?? "default"); // default
```

**Q40. Tagged template literal কী?**

👉 Tagged template literal হলো function যেটা template literal কে custom process করে।

## ⚖️ Advanced Concepts & Performance

**Q41. Currying কী?**

👉 Currying হলো multi-arg function কে ভেঙে nested single-arg function এ রূপান্তর করা। এটি functional programming এ use হয়।

```js
const add = (a) => (b) => a + b;
const add5 = add(5);
console.log(add5(3)); // 8
```

**Q42. Memoization কী?**

👉 Memoization হলো expensive function‑এর ফল cache করে রাখা, ফলে একই input‑এ দ্রুত ন্যূনতম কম্পিউটেশন হয়।

```js
const memoize = (fn) => {
  const cache = new Map();
  return (arg) => (cache.has(arg) ? cache.get(arg) : cache.set(arg, fn(arg)) && cache.get(arg));
};
const slow = (n) => {
  /* heavy calc */
  return n * n;
};
const fast = memoize(slow);
```

**Q43. Tail call optimization কী?**

👉 TCO হলে recursive ফাংশনের শেষ কাজটাই recursive কল, তখন কল‑স্ট্যাক reuse করে stack overflow আটকায়; সব JS engines এটি সমর্থন করে না, তবে ভাল recursive pattern লিখতে সাহায্য করে।

```js
function fact(n, acc = 1) {
  if (n === 0) return acc;
  return fact(n - 1, acc * n); // tail position
}
```

**Q44. Service worker কী?**

👉 Service Worker background‑এ assets/requests cache করে, offline বা slow network‑এ দ্রুত response দেয় এবং background sync বা push notification চালায়।

```js
// register in main script
navigator.serviceWorker.register("/sw.js");
```

**Q45. `localStorage` vs `sessionStorage` vs `cookies` পার্থক্য কী?**

👉 localStorage data browser এ থাকে যতক্ষণ clear না করা হয়। sessionStorage tab close হলে clear হয়। cookies request এর সাথে server এ পাঠানো হয়।

```js
localStorage.setItem("theme", "dark"); // persists
sessionStorage.setItem("temp", "1"); // clears on tab close
```

**Q46. `==` vs `Object.is()` পার্থক্য কী?**

👉 `Object.is()` প্রায় `===` এর মতো, তবে `NaN` আর `-0` case গুলো সঠিকভাবে handle করে।

```js
NaN === NaN; // false
Object.is(NaN, NaN); // true
Object.is(0, -0); // false
```

**Q47. Garbage collection কীভাবে কাজ করে?**

👉 GC সাধারণত reachability দেখে: কোনো object যদি program থেকে reference না থাকে, সেটাকে রিমুভ করে। ঠিক কবে ও কীভাবে হয় engine নির্ভর।

```js
const obj = { a: 1 };
obj = null; // garbage collected
```

**Q48. Event bubbling vs capturing পার্থক্য কী?**

👉 Capturing: parent → child, Bubbling: child → parent. ডিফল্ট হলো bubbling; কোনও ক্ষেত্রে parent এ centralized handler রাখতে গেলে bubbling কাজে লাগে।

```js
// capture phase
elem.addEventListener("click", handler, true);
// bubble phase
elem.addEventListener("click", handler, false);
```

**Q49. `map()`, `forEach()`, `filter()`, `reduce()` পার্থক্য কী?**

👉 `map()` array transform করে, `filter()` subset বেছে নেয়, `reduce()` value aggregate করে। এগুলো একসাথে ব্যবহার করে readable data pipelines বানান।

```js
const nums = [1, 2, 3, 4];
const evens = nums.filter((n) => n % 2 === 0); // [2,4]
const doubled = nums.map((n) => n * 2); // [2,4,6,8]
const sum = nums.reduce((s, n) => s + n, 0); // 10
```

**Q50. Pure function কী?**

👉 Pure function একই input দিলে সবসময় একই output দেয় এবং কোনো external state পরিবর্তন করে না; testable, cacheable, predictable code‑base তৈরিতে সহায়ক।

```js
// pure
const add = (a, b) => a + b;
// impure (mutates external state)
let total = 0;
function addToTotal(x) {
  total += x;
}
```

---

# ⚛️ 50 React Interview Q&A

## 🏗️ Architecture & Core Concepts

**Q1. React-এর limitation কী large‑scale app বানাতে গেলে?**

👉 React শুধু UI library; routing, global state, এবং app architecture‑এর জন্য আপনাকে অতিরিক্ত libraries ও patterns (Router, state store, testing, build setup) নিতে হবে।

```jsx
// UI-only: you still need router & store separately
import React from "react";
import { BrowserRouter } from "react-router-dom";
// state: Redux / Zustand / Context
```

**Q2. Virtual DOM কীভাবে কাজ করে এবং কেন দরকার?**

👉 React Virtual DOM এ component tree রেখে আগের state‑এর সাথে diff করে, তারপর সবচেয়ে কম real DOM অপারেশনই করে-এই কারণে UI দ্রুত ও স্মুথ হয়।

```jsx
// conceptual: React updates virtual tree, then patches DOM efficiently
```

**Q3. Hooks কি Redux পুরোপুরি replace করতে পারে? কখন করবেন/কখন করবেন না?**

👉 ছোট বা মাঝারি scope‑এর state‑এ Hooks (`useState`, `useReducer`, `Context`) যথেষ্ট; কিন্তু shared complex logic, time‑travel debugging, বা predictability চাইলে Redux/RTK ভালো।

```jsx
// Local state
const [count, setCount] = useState(0);
// Global: consider store (RTK) for complex apps
```

**Q4. বড় অ্যাপে state‑management এর recommended pattern কী?**

👉 UI‑specific state রাখুন local component এ, cross‑cutting concerns (theme, auth) রাখুন Context‑এ, আর complex normalized global state রাখুন external store (RTK/Zustand) এ।

```jsx
// Example: local -> Context -> store
// Cart (global) -> Redux, Modal open (local) -> useState
```

**Q5. বড় component tree‑এর performance কিভাবে optimize করবেন?**

👉 Memoize pure components (`React.memo`), expensive calculations (`useMemo`), callbacks (`useCallback`); code‑split routes/components এবং large lists‑এ virtualization ব্যবহার করুন।

```jsx
const Item = React.memo(({item}) => /* render */);
const list = useMemo(()=> computeHeavy(items), [items]);
```

**Q6. React StrictMode কী করে developer‑mode এ?**

👉 StrictMode unsafe lifecycle ও deprecated patterns warn করে; effects কে double‑invoke করে side‑effect bugs ধরতে সাহায্য করে (only dev).

```jsx
<React.StrictMode>
  <App />
</React.StrictMode>
```

**Q7. অপরিহার্য re‑render কিভাবে কমাবেন?**

👉 প্যারেন্ট থেকে নতুন object/array পাঠানো এড়ান, memoize করুন, context‑value গুলো memoize করে দিন এবং expensive child‑কে `React.memo` দিয়ে wrap করুন।

```jsx
const value = useMemo(() => ({ user }), [user]);
<Ctx.Provider value={value}>...</Ctx.Provider>;
```

**Q8. Functional vs Class components - কবে কোনটা বেছে নিবেন?**

👉 Modern code‑base‑এ functional + Hooks ব্যবহার করুন (cleaner, smaller, composable). Class লাগবে legacy কোডে বা rare lifecycle edge cases‑এ।

**Q9. React Fiber‑এর গুরুত্ব সংক্ষেপে কী?**

👉 Fiber rendering engine যা work splitting ও prioritization করে-UI interruptible করে, responsiveness বাড়ায় এবং concurrent features enable করে।

**Q10. Side effects কীভাবে সঠিকভাবে manage করবেন?**

👉 `useEffect`/ `useLayoutEffect` এ effects লিখুন, dependency array ঠিক রাখুন এবং cleanup (unsubscribe/clear timers) নিশ্চিত করুন যাতে memory leak না হয়।

```jsx
useEffect(() => {
  const id = setInterval(tick, 1000);
  return () => clearInterval(id);
}, []);
```

---

## 🗂️ State Management

**Q11. useMemo vs useCallback পার্থক্য কী? কেন কখন কোনটা ব্যবহার করবেন?**

👉 useMemo একটি গণিত/কম্পিউটেশনাল মানকে ক্যাশ করে রাখে যাতে পরবর্তী re‑render‑এ আবার কল করলে ব্যয়বহুল কাজ না করতে হয়; useCallback একটি function reference ক্যাশ করে যাতে সেই function পাস করা component‑গুলো অপ্রয়োজনীয়ভাবে re‑render না করে। বাস্তবে, যদি আপনার UI‑এ বড় তালিকা থাকে এবং প্রতিবার parent রেন্ডার করলে child component‑এর expensive compute না হতে চান, useMemo; যদি prop হিসেবে function পাঠালে child বারবার রেন্ডার হয়, useCallback ব্যবহার করবেন।

```jsx
const filtered = useMemo(() => {
  return items.filter((i) => i.name.includes(query)); // heavy when items large
}, [items, query]);

const handleSelect = useCallback((id) => {
  // stable reference passed to many child rows
  setSelectedId(id);
}, []);
```

**Q12. Dynamic form handling কিভাবে করবেন - React Hook Form দিয়ে বাস্তব উদাহরণ?**

👉 অনেক ইনপুট, ভ্যালিডেশন ও পারফরম্যান্স থাকলে React Hook Form ভালো because it minimizes re‑renders এবং সহজ API দেয়। কাজের উদাহরণ: multi‑step signup যেখানে nested fields এবং async validation রয়েছে।

```jsx
import { useForm } from "react-hook-form";

function Signup() {
  const {
    register,
    handleSubmit,
    formState: { errors },
  } = useForm();
  const onSubmit = (data) => fetch("/api/signup", { method: "POST", body: JSON.stringify(data) });

  return (
    <form onSubmit={handleSubmit(onSubmit)}>
      <input {...register("email", { required: true })} placeholder="Email" />
      {errors.email && <span>Required</span>}
      <input {...register("password", { minLength: 6 })} type="password" />
      <button type="submit">Sign up</button>
    </form>
  );
}
```

ব্যাখ্যা: এখানে RHF field‑level registration দিয়ে প্রতিটি ইনপুট local control রাখে, ফলে প্রতি keypress এ পুরো ফর্ম re‑render হয় না - পারফরম্যান্স বাড়ে।

**Q13. Lazy loading কবে ও কিভাবে কাজে দেয় (React.lazy + Suspense) - বাস্তব কেস?**

👉 যখন অ্যাপ বড় এবং কিছু route‑specific ইউআই আগে থেকেই লোড করে রাখলে প্রারম্ভিক bundle বাড়ে, তখন React.lazy দিয়ে route‑level component ডাইনামিক লোড করে initial load ত্বরান্বিত করা যায়। উদাহরণ: Dashboard app‑এ AdminPanel কেবল admin ইউজারের জন্য দরকার - সেটা lazy load করতে পারেন।

```jsx
// App.js
const AdminPanel = React.lazy(() => import("./AdminPanel"));

function App() {
  return (
    <BrowserRouter>
      <Routes>
        <Route
          path="/admin"
          element={
            <Suspense fallback={<Spinner />}>
              <AdminPanel />
            </Suspense>
          }
        />
      </Routes>
    </BrowserRouter>
  );
}
```

ব্যাখ্যা: Suspense fallback UI দেখায় যতক্ষণ module লোড হচ্ছে; এতে initial JS ছোট থাকে এবং perceived load time ভালো হয়।

**Q14. Error boundary কী ধরে, কোথায় সীমাবদ্ধতা আছে? বাস্তব উদাহরণ দেখান।**

👉 Error boundary শুধুমাত্র render‑phase ও lifecycle methods‑এ ওঠা exceptions ধরে এবং ওই subtree‑র জন্য একটি fallback UI দেখায়; এটি event handlers বা async promise rejection ধরতে পারে না। বাস্তবে, বড় UI block (e.g., third‑party widget) আলাদা ErrorBoundary‑এ রাখা উচিত।

```jsx
class ErrorBoundary extends React.Component {
  state = { hasError: false };
  static getDerivedStateFromError() {
    return { hasError: true };
  }
  componentDidCatch(error, info) {
    /* log to service */
  }
  render() {
    return this.state.hasError ? <Fallback /> : this.props.children;
  }
}
```

ব্যাখ্যা: আপনি UI এর critical parts (feeds, widgets) আলাদা boundary‑এ রাখলে single widget crash পুরো app ভাঙে না।

**Q15. SSR (Server‑Side Rendering) ব্যবহার করার মূল কারণ ও tradeoffs কি?**

👉 SSR SEO ও first‑contentful‑paint দ্রুত করার জন্য ভালো; কিন্তু server complexity, caching, data fetching orchestration (hydration) বড় করতে পারে। যদি আপনার landing pages SEO‑critical অথবা প্রথম লোড‑টাইম খুব গুরুত্বপূর্ণ হয়, SSR/SSG বেছে নিন; অন্যথায় CSR বা hybrid (Next.js) ভালো।

**Q16. React‑এ styling approaches - সিদ্ধান্ত নিতে practical guideline কি?**

👉 Project মাপ, team preference ও CSS scope বিবেচ্যে: utility‑first (Tailwind) দ্রুত UI, CSS Modules scoped traditional CSS জন্য, CSS‑in‑JS (styled‑components) runtime theming ও dynamic styles‑এর জন্য ভালো। বাস্তবে component library হলে CSS Modules বা CSS‑in‑JS ব্যবহার করুন যাতে styles encapsulated থাকে।

```jsx
// CSS Module example
import styles from "./Button.module.css";

function Button() {
  return <button className={styles.primary}>Click</button>;
}
```

**Q17. Redux ছাড়া sibling components‑এ data pass করা - practical way (example)?**

👉 সহজ ক্ষেত্রে state‑lift‑up: common parent‑এ state রাখা এবং props দিয়ে siblings‑এ পাঠান। Context প্রয়োজনে ব্যবহার করুন যদি অনেক siblings বা deeply nested components থাকে।

```jsx
function Parent() {
  const [query, setQuery] = useState("");
  return (
    <>
      <Search value={query} onChange={setQuery} />
      <Results query={query} />
    </>
  );
}
```

ব্যাখ্যা: যদি Results অনেক গভীরে থাকে এবং props drilling বাড়ে, তখন Context provider দিয়ে value share করা বুদ্ধিমানের কাজ।

**Q18. API fetch করার জন্য useEffect কিভাবে সাজাবেন - cleanup ও error handling সহ?**

👉 useEffect‑এ fetch করে loading/data/error states রাখুন, এবং AbortController দিয়ে stale requests cancel করুন-বিশেষ করে যখন component unmount বা dependency পরিবর্তন হয়।

```jsx
useEffect(() => {
  const ac = new AbortController();
  let mounted = true;

  async function load() {
    try {
      setLoading(true);
      const resp = await fetch(`/api/items?q=${encodeURIComponent(q)}`, { signal: ac.signal });
      if (!resp.ok) throw new Error("Fetch error");
      const json = await resp.json();
      if (mounted) setData(json);
    } catch (err) {
      if (err.name !== "AbortError" && mounted) setError(err);
    } finally {
      if (mounted) setLoading(false);
    }
  }

  load();
  return () => {
    mounted = false;
    ac.abort();
  };
}, [q]);
```

ব্যাখ্যা: এতে rapid query changes বা route change এ পুরানো request থেকে state overwrite হওয়া বন্ধ হয়। AbortController ও mounted flag দিয়ে stale response বা unmount‑পর update আটকানো হয়েছে।

**Q19. Async operation & state updates - race condition ও stale state কিভাবে এড়াবেন?**

👉 প্রতিটি async request কে একটি unique id দিন বা AbortController ব্যবহার করুন; এখানেই effect cleanup ও local mounted flag দরকার। Functional updates (prev => next) ব্যবহার করুন যেখানে previous state‑এর উপর নির্ভরতা আছে।

```jsx
let lastReq = 0;
useEffect(() => {
  const reqId = ++lastReq;
  let cancelled = false;

  (async () => {
    try {
      const res = await fetch(url);
      if (!res.ok) throw new Error("Network error");
      const data = await res.json();
      if (!cancelled && reqId === lastReq) setData(data);
    } catch (err) {
      if (!cancelled) setError(err);
    }
  })();

  return () => {
    cancelled = true;
  };
}, [url]);
```

ব্যাখ্যা: প্রতিটি effect চালানোর সময় unique `reqId` বাড়ে; শুধুমাত্র সর্বশেষ `reqId`‑এর response state‑এ বসবে, এতে race condition টলা পড়ে।

**Q20. Window resize হলে component re‑render: debounce/cleanup সহ practical pattern**

👉 প্রতিবার resize এ state আপডেট করলে performance খারাপ হবে; debounce করে update করুন এবং cleanup দিয়ে listener তুলে নিন।

```jsx
useEffect(() => {
  let t;
  const onR = () => {
    clearTimeout(t);
    t = setTimeout(() => setW(window.innerWidth), 200);
  };
  window.addEventListener("resize", onR);
  return () => {
    clearTimeout(t);
    window.removeEventListener("resize", onR);
  };
}, []);
```

ব্যাখ্যা: এতে continuous resize এ শুধু শেষ অবস্থায় state আপডেট হবে এবং re‑renders কমবে।

**Q21. Context API কখন ঠিক, কখন ভুল? (performance tips)**

👉 Context চমৎকার যখন low‑frequency global data চাই (theme, locale, auth). কিন্তু high‑frequency changing data (like typing cursor, live metrics) Context এ রাখলে পুরো subtree re‑render করে; সে ক্ষেত্রে external store বা selector pattern ব্যবহার করুন এবং provider value memoize করুন।

```jsx
const value = useMemo(() => ({ user, logout }), [user]);
<AuthContext.Provider value={value}>...</AuthContext.Provider>;
```

**Q22. React Router dynamic routing - example with params & navigation**

👉 UseParams দিয়ে URL params পড়েন, useNavigate দিয়ে কোড থেকে redirect করুন; page‑level data fetching এ param change‑এর সাথে effect টিগার করবেন।

```jsx
// ProductPage.jsx
const { id } = useParams();
useEffect(()=> { fetch(`/api/products/${id}`)... }, [id]);
const nav = useNavigate();
<button onClick={()=> nav('/cart')}>Go to cart</button>
```

**Q23. Controlled vs Uncontrolled components - কখন কোনটা বেছে নেবেন?**

👉 Controlled inputs state‑driven validation/instant UI sync চাইলে ব্যবহার করুন; simple forms বা 3rd‑party uncontrolled APIs থাকলে refs‑based uncontrolled inputs দ্রুত ও কম কোডে কাজ দেয়।

**Q24. Large lists optimize করার পূর্ণাঙ্গ pattern (virtualization + memo + keys)**

👉 Virtualize (react-window) করে DOM nodes কম রাখুন, row component memoize করুন এবং stable unique key ব্যবহার করুন; lazy load images এবং pagination/infinite loading মিলিয়ে ব্যবহার করুন।

```jsx
import { FixedSizeList as List } from "react-window";

<List height={500} itemCount={items.length} itemSize={50}>
  {({ index, style }) => <Row style={style} data={items[index]} />}
</List>;
```

**Q25. Shallow vs Deep comparison - practical implications ও immutable pattern**

👉 React (PureComponent/React.memo) shallow compare করে; nested mutation করলে পরিবর্তন ধরবে না-এজন্য immutable updates (spread, map) রাখুন যাতে reference change ঘটে এবং re‑render প্রয়োজনমতো হয়।

```jsx
// WRONG (mutates)
state.items.push(newItem);
// RIGHT (immutable)
setState((s) => ({ ...s, items: [...s.items, newItem] }));
```

**Q26. Async state update কিভাবে handle করবেন - React batching ও functional updates কি করে সাহায্য করে?**

👉 React একই event loop টিকে ধরে একাধিক state update একসাথে batch করে, যাতে অপ্রয়োজনীয় re‑render কমে। যখন নতুন state পুরোনো state‑এর উপর নির্ভর করে, তখন functional update (setState(prev=>…)) ব্যবহার করলে race condition এড়ায়।

```jsx
// BAD (race when multiple updates rely on previous)
setCount(count + 1);
setCount(count + 2);

// GOOD (functional updates are safe)
setCount((c) => c + 1);
setCount((c) => c + 2);
```

ব্যাখ্যা: network response বা rapid user actions এ functional update ব্যবহার করলে state lost হওয়ার ঝুঁকি কমে।

**Q27. Custom hook কেন বানবেন - উদাহরণসহ reusable pattern দেখান।**

👉 Custom hook reusable logic encapsulate করে ও componentগুলোকে পরিষ্কার রাখে; উদাহরণ: API fetch hook যা loading/data/error handle করে।

```jsx
import { useState, useEffect } from "react";

function useFetch(url) {
  const [state, setState] = useState({ loading: true, data: null, error: null });

  useEffect(() => {
    const ac = new AbortController();
    let mounted = true;

    async function fetchData() {
      try {
        setState({ loading: true, data: null, error: null });
        const res = await fetch(url, { signal: ac.signal });
        if (!res.ok) throw new Error(`Status ${res.status}`);
        const data = await res.json();
        if (mounted) setState({ loading: false, data, error: null });
      } catch (err) {
        if (err.name !== "AbortError" && mounted) setState({ loading: false, data: null, error: err });
      }
    }

    if (url) fetchData();

    return () => {
      mounted = false;
      ac.abort();
    };
  }, [url]);

  return state;
}

// Usage
// const { loading, data, error } = useFetch('/api/posts');
```

ব্যাখ্যা: এই hook‑টি reuse করে বিভিন্ন components দ্রুত এবং consistent ভাবে data fetch করতে পারবেন। AbortController ও mounted flag দিয়ে cleanup করা হয়েছে যাতে unmount বা rapid url পরিবর্তনে stale updates না আসে

**Q28. HOC কী এবং কখন HOC ব্যবহার করবেন - real example?**

👉 HOC (Higher‑Order Component) একটি component কে accept করে নতুন behavior/props যোগকরে একটি enhanced component return করে; cross‑cutting concern (auth, logging) inject করতে HOC এখনও প্রাকটিকাল।

```jsx
// withAuth HOC: protects a component
const withAuth = (Wrapped) => (props) => {
  const user = useContext(AuthContext);
  if (!user) return <LoginRedirect />;
  return <Wrapped {...props} />;
};
const ProtectedDashboard = withAuth(Dashboard);
```

ব্যাখ্যা: নতুন আলাদা validation বা data fetching logic সব একই UI components‑এ reuse করতে HOC সহজ করে।

**Q29. Debounced search React‑এ কিভাবে করবেন - practical example with hooks**

👉 User typing এ প্রতিটি keypress‑এ API call করা expensive; debounce দিয়ে শেষ typing পরে একবারই call পাঠান। lodash/debounce ব্যবহার অথবা custom hook বানান।

```jsx
import { useState, useEffect } from "react";

function useDebounce(value, delay = 300) {
  const [debounced, setDebounced] = useState(value);
  useEffect(() => {
    const t = setTimeout(() => setDebounced(value), delay);
    return () => clearTimeout(t);
  }, [value, delay]);
  return debounced;
}

// Usage in component
const [q, setQ] = useState("");
const debouncedQ = useDebounce(q, 400);
useEffect(() => {
  if (debouncedQ) fetch(`/search?q=${debouncedQ}`);
}, [debouncedQ]);
```

ব্যাখ্যা: UI responsive থাকে এবং unnecessary network requests অনেক কমে।

**Q30. Reconciliation কীভাবে কাজ করে এবং keys কেন গুরুত্বপূর্ণ - practical tip**

👉 Reconciliation হলো React‑এর diff algorithm যা previous ও new virtual DOM তুলনা করে minimal DOM updates করে; list item‑এ stable unique key দিলে React element identity ধরে রাখে এবং reorder/insert/delete efficient হয়।

```jsx
// BAD: index as key causes bugs on reordering
items.map((item, idx) => <Row key={idx} item={item} />);
// GOOD: stable id key preserves component state
items.map((item) => <Row key={item.id} item={item} />);
```

ব্যাখ্যা: UI‑এ ইনপুট বা local state যুক্ত row থাকলে ঠিক key না দিলে user input বা animation ভুল স্থানে বসতে পারে - তাই unique persistent key ব্যবহার করুন।

---

## 🚀 Advanced & Performance

**Q31. বড় অ্যাপের জন্য folder structure কেমন হওয়া উচিত?**

👉 Feature/Domain‑based স্ট্রাকচার রাখুন যাতে feature অনুযায়ী কোড, টেস্ট ও টাইপ এক জায়গায় থাকে; shared UI এবং util আলাদা রাখলে ownership, scalability আর CI সহজ হয়।

```js
src/
├─ features/
│  ├─ products/
│  │  ├─ ProductList.jsx
│  │  ├─ ProductCard.jsx
│  │  ├─ productSlice.js
│  │  └─ Product.test.jsx
│  ├─ cart/
│  │  ├─ Cart.jsx
│  │  ├─ cartApi.js
│  │  └─ Cart.test.jsx
│  └─ auth/
│     ├─ AuthProvider.jsx
│     ├─ authApi.js
│     └─ useAuth.test.jsx
├─ ui/
│  ├─ Button.jsx
│  ├─ Modal.jsx
│  └─ Spinner.jsx
├─ utils/
│  ├─ formatPrice.js
│  └─ fetcher.js
├─ hooks/
│  ├─ useFetch.js
│  └─ useDebounce.js
├─ styles/
│  └─ globals.css
├─ App.jsx
└─ index.jsx
```

**Q32. Redux Toolkit vs Zustand vs Recoil — কখন কোনটা বেছে নিবেন?**

👉 RTK: normalized state, middleware ও devtools দরকার হলে; Zustand: ছোট‑medium apps এ lightweight ও minimal API; Recoil: React‑centric atom/selector pattern চাইলে। প্রজেক্টের complexity, debuggability আর bundle‑size দেখে সিদ্ধান্ত নিন।

```js
// Zustand উদাহরণ: ছোট global state
import create from "zustand";
const useStore = create((set) => ({
  cart: [],
  add: (item) => set((s) => ({ cart: [...s.cart, item] })),
}));
```

**Q33. Global vs Local state — বাস্তব সিদ্ধান্তের নিয়ম কী?**

👉 Local: UI‑specific (modal, input), Global: shared across routes/screens (auth, cart). High‑frequency updates global এ দিলে subtree re‑renders বেড়ে যায়, তাই selector বা derived state ব্যবহার করে minimize করুন।

**Q34. Context বেশি ব্যবহার করলে সমস্যা কী হয় এবং mitigation কী?**

👉 অনেক পরিবর্তনশীল Context value থাকলে পুরো provider‑এর subtree re‑render হয়; সমাধান: context split (theme/auth আলাদা) ও provider value‑কে useMemo দিয়ে stabilize করা।

```jsx
const authValue = useMemo(() => ({ user, logout }), [user]);
<AuthProvider value={authValue}>...</AuthProvider>;
```

**Q35. Suspense কীভাবে ব্যবহার করবেন (code‑splitting প্র্যাকটিস)?**

👉 Component‑level lazy loading এর জন্য Suspense ব্যবহার করুন—route‑specific বা heavy widgets lazy রাখলে initial bundle ছোট হয় এবং fallback UX consistent থাকে। Data Suspense এখনো limited; code Suspense production‑ready।

```jsx
const Analytics = React.lazy(() => import("./Analytics"));
<Suspense fallback={<Spinner />}>
  <Analytics />
</Suspense>;
```

**Q36. Concurrent rendering এর সুবিধা ও সতর্কতা কী?**

👉 সুবিধা: rendering interruptible হওয়ায় UI responsive থাকে; সতর্কতা: effects timing/ordering বদলাতে পারে, তাই side‑effects idempotent রাখুন এবং assumptions‑এ কোন ordering নির্ভর করবেন না।

**Q37. Bundle size কমানোর বাস্তব কৌশলগুলো কী?**

👉 Dynamic imports (বড় বা route‑specific কোডকে runtime‑এ লোড করুন যাতে initial bundle ছোট থাকে), tree‑shaking friendly imports (লাইব্রেরির পুরো প্যাকেজ না নিয়ে কেবল যেটা দরকার সেটাই ইমপোর্ট করুন বা ES module ভার্সন ব্যবহার করুন।), analyzer দিয়ে bundle breakdown দেখুন, বড় লাইব্রেরি lazy load করুন এবং assets compress/serve আগে থেকে CDN দিয়ে দিন।

```js
// tree-shaking friendly
import pick from "lodash/pick";

const Chart = React.lazy(() => import("./heavy/Chart"));
```

**Q38. Infinite scroll বাস্তবায়নের সেরা প্যাটার্ন কী?**

👉 IntersectionObserver দিয়ে sentinel observe করুন, লোডিং flag রাখুন যাতে duplicate requests না যায়, এবং virtualization (react-window) ব্যবহার করে DOM light রাখুন।

```js
const sentinelRef = useRef();
useEffect(() => {
  const io = new IntersectionObserver(([e]) => {
    if (e.isIntersecting && !loading) loadMore();
  });
  if (sentinelRef.current) io.observe(sentinelRef.current);
  return () => io.disconnect();
}, [loading]);
```

**Q39. Memory leak কীভাবে খুঁজবেন এবং ঠিক করবেন — practical checklist**

👉 Symptoms: increasing memory, detached DOM, event flood. Fixes: effect cleanup (remove listeners, clear intervals), AbortController cancel fetch, disconnect observers, unsubscribe sockets; Browser DevTools → Performance/Memory দিয়ে root cause খুঁজুন।

```jsx
useEffect(() => {
  const id = setInterval(poll, 5000);
  return () => clearInterval(id); // cleanup
}, []);
```

**Q40. Async race condition কিভাবে robustly হ্যান্ডেল করবেন?**

👉 AbortController দিয়ে পুরোনো fetch cancel করুন অথবা request‑id track করে শুধুমাত্র latest response লাগান; optimistic updates হলে transaction id দিয়ে rollback handle করুন।

```js
useEffect(() => {
  const ac = new AbortController();
  const fetchData = async () => {
    try {
      const res = await fetch(url, { signal: ac.signal });
      if (!res.ok) throw new Error("Fetch failed");
      const json = await res.json();
      setData(json);
    } catch (err) {
      if (err.name !== "AbortError") setError(err);
    }
  };
  fetchData();
  return () => ac.abort();
}, [url]);
```

---

## 🌍 SSR, Routing & Data

**Q41. Next.js vs CSR trade‑off কী?**

👉 Next.js (SSR/SSG) প্রথম‑পেইন্ট (FCP) দ্রুত করে এবং SEO উন্নত করে, কিন্তু সার্ভার complexity ও build/deploy flow বাড়ায়; CSR সহজ, UX‑heavy বা internal apps‑এ ভাল। সিদ্ধান্ত - SEO/first‑load গুরুত্বপূর্ণ হলে Next.js, অন্যথায় CSR বা hybrid ব্যবহার করুন।

```jsx
// Next.js page (SSG example)
export async function getStaticProps() {
  const res = await fetch("https://api.example.com/posts");
  return { props: { posts: await res.json() } };
}
export default function Page({ posts }) {
  return <PostList posts={posts} />;
}
```

**Q42. Auth flow React/Next এ কিভাবে বাস্তবায়ন করবেন (practical pattern)?**

👉 Authentication token server‑set cookie অথবা client JWT হিসাবে রাখুন; route guard করতে higher‑order component বা middleware ব্যবহার করুন এবং auth state Context/Store‑এ রাখুন। Server‑side rendering হলে cookie‑based token server থেকে validate করুন।

```jsx
// simple client guard (React)
function Protected({ children }) {
  const { user } = useAuth();
  if (!user) return <Navigate to="/login" />;
  return children;
}
```

**Q43. Large form হলে performance ও validation কীভাবে সাজাবেন?**

👉 React Hook Form ব্যবহার করে uncontrolled approach + field registration করুন, validation rules lazy বা async(validate on blur) রাখুন; huge forms‑এ virtualize long field lists এবং section‑wise submit/use partial saves করুন।

```jsx
// RHF partial save example
const { register, handleSubmit } = useForm();
const onSubmit = async (data) => await api.savePart(data);
```

**Q44. Optimistic UI update কিভাবে নিরাপদে করবেন (rollback pattern)?**

👉 UI‑state আগে আপডেট করে UX দ্রুত দেখান, ব্যর্থ হলে rollback করুন; request id বা previous snapshot রাখুন এবং error এ previous state ফেরত দিন।

```jsx
async function toggleLike(id) {
  const prev = likes;
  setLikes((s) => (s.includes(id) ? s.filter((x) => x !== id) : [...s, id]));
  try {
    await api.toggleLike(id);
  } catch (e) {
    setLikes(prev); // rollback on failure
  }
}
```

**Q45. React + GraphQL (Apollo) integration — cache ও data fetch pattern?**

👉 Apollo Client দিয়ে query ও cache normalization করে UI দ্রুত আপডেট পাই; mutations এ optimisticResponse দিন এবং cache.update ব্যবহার করে local updates রাখুন। Data fetching server‑side করলে Apollo SSR helpers ব্যবহার করুন।

```js
// optimistic like mutation
const [toggle] = useMutation(TOGGLE_LIKE, {
  optimisticResponse: { toggleLike: { id, liked: true } },
  update(cache, { data: { toggleLike } }) {
    cache.modify({ id: cache.identify({ __typename: "Post", id }), fields: { liked: () => toggleLike.liked } });
  },
});
```

---

## ⚖️ Accessibility, Testing & UX

**Q46. Accessibility নিশ্চিত করবেন কিভাবে — দ্রুত চেকলিস্ট ও উদাহরণ**

👉 Semantic HTML, proper ARIA attributes, keyboard navigation এবং contrast নিশ্চিত করুন; automated tools (axe, Lighthouse) ও.manual testing screen reader দিয়ে চালান।

```jsx
// semantic + aria example
<button aria-label="Close dialog" onClick={close}>✕</button>
<nav aria-label="Primary">
  <a href="/home">Home</a>
</nav>
```

**Q47. i18n কিভাবে বাস্তবায়ন করবেন — pattern ও performance টিপস**

👉 Strings externalize করে locale ফাইল রাখুন, lazy‑load translations per route, এবং ICU/plural rules সমর্থন করা লাইব্রেরি (i18next/react-intl) ব্যবহার করুন; server‑side render হলে locale detect ও prefetch করুন।

```js
// i18next usage sketch
const { t } = useTranslation();
return <h1>{t("welcome", { name })}</h1>;
```

**Q48. React টেস্টিং স্ট্র্যাটেজি — unit, integration, end‑to‑end practical guide**

👉 Unit test: pure components/logic (Jest). Integration: component interaction with DOM (React Testing Library). E2E: user flows (Cypress/Playwright). Tests ছোট, deterministic ও fast রাখুন; critical flows এ E2E যোগ করুন।

```js
// RTL example: check button triggers callback
test("submits form", async () => {
  render(<Form onSubmit={mock} />);
  userEvent.type(screen.getByLabelText(/email/i), "a@b.com");
  userEvent.click(screen.getByRole("button", { name: /submit/i }));
  expect(mock).toHaveBeenCalled();
});
```

**Q49. Error logging ও monitoring কিভাবে সাজাবেন — best practice**

👉 Error boundary/UI capture + centralized client logger (Sentry/LogRocket) ব্যবহার করুন; breadcrumbs, user context ও release tagging যোগ করুন; server errors আলাদা ট্র্যাক করুন এবং rate‑limit noisy logs।

```js
// pseudocode: capture error with context
Sentry.captureException(err, { userId: user.id, route: location.pathname });
```

**Q50. Scale‑এ performance degrade হলে কী করবেন — step‑by‑step debugging plan**

👉 Steps -

1. Reproduce with profiler (React DevTools, Lighthouse).
2. Identify hot components (expensive renders, large bundles).
3. Apply targeted fixes: memoization, virtualization, code‑split, smaller libs.
4. Re‑measure and iterate.

```js
// quick checklist:
// Profiler -> Flamegraph -> isolate component -> fix (memo/virtualize) -> measure
```

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

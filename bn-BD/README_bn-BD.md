<div align="center">
    <img height="40" src="https://svgmix.com/uploads/d64401-javascript.svg" />
    <img height="40" src="https://svgmix.com/uploads/e86a0a-react.svg" />
    <h1>🚀 The Ultimate Frontend Interview Prep Guide</h1>
</div>

React ও JavaScript ইন্টারভিউ প্রস্তুতির জন্য ১০০+ Q&A ও cheat sheet। Frontend developer দের জন্য শেখা, রিভিশন ও ইন্টারভিউ ক্র্যাক করার গাইড।

আমি এই রিসোর্সটি তৈরি করেছি **শেখা, শেয়ার করা এবং কমিউনিটি গ্রোথ** 🌱 এর জন্য। যদি এটি আপনার কাজে লাগে, তবে একটি ⭐️ বা শেয়ার আমার জন্য অনেক বড় ব্যাপার হবে!

✨ শুভকামনা, **Happy coding!**

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

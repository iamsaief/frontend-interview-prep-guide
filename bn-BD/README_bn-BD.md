<div align="center">
    <img height="60" src="https://img.icons8.com/color/344/javascript.png" />
    <img height="55" src="https://svgmix.com/uploads/e86a0a-react.svg" />
    <h1>Frontend Interview Q&A 🎓</h1>
</div>

<p align="center">
💬 In case you want to reach out or just say hi, ↩️ <br/>
<a href="https://www.facebook.com/saiefalemon">Facebook</a> | <a href="https://www.linkedin.com/in/saiefalemon">LinkedIn</a> | <a href="https://www.iamsaief.github.io.com/">Portfolio</a>
</p>

---

**🗂️ সূচিপত্র**

- [⚡ 50 React Interview Q\&A](#-50-react-interview-qa)
  - [🏗️ Architecture \& Core Concepts](#️-architecture--core-concepts)
  - [🗂️ State Management](#️-state-management)
  - [🚀 Advanced \& Performance](#-advanced--performance)
  - [🌍 SSR, Routing \& Data](#-ssr-routing--data)
  - [⚖️ Accessibility, Testing \& UX](#️-accessibility-testing--ux)
  - [⚡ React Core Concepts Cheat Sheet](#-react-core-concepts-cheat-sheet)

---

# ⚡ 50 React Interview Q&A

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

## ⚡ React Core Concepts Cheat Sheet

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

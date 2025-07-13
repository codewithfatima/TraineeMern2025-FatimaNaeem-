### ### ##  Component Lifecycle (Class Components)

React class components go through three main lifecycle phases:

- **Mounting** – Component is being created and inserted into the DOM.  
- **Updating** – Component is re-rendered due to state or prop changes.  
- **Unmounting** – Component is removed from the DOM.

Key lifecycle methods:
- `constructor` – Initializes state.
- `componentDidMount` – Runs once after the component mounts.
- `componentDidUpdate` – Runs after every update.
- `componentWillUnmount` – Used for cleanup before removal.

> 📝 In **functional components**, these are handled using `useEffect()`.

---

##  Keys & Lists

- **Lists** in React are used to render multiple items using iteration.
- **Keys** are unique identifiers used by React to track list items and optimize rendering.
- Keys help React identify which items have changed, been added, or removed.
- Keys must be **unique and stable**. Using indexes as keys is discouraged unless the list is static.

---

## 🧰 React Hooks (Built-in)

Hooks let you use state and other React features in functional components. Common hooks include:

- `useState` – Manages local state within a component.
- `useEffect` – Handles side effects like data fetching or subscriptions.
- `useContext` – Accesses React context values.
- `useRef` – Holds mutable values or DOM references.
- `useMemo` – Memoizes expensive computations.
- `useCallback` – Memoizes functions to prevent re-renders.
- `useReducer` – Alternative to `useState` for complex state logic.

### 🔒 Rules of Hooks:
- Must be called at the top level of a component.
- Must be called in the same order on every render.
- Only call hooks inside functional components or other hooks.

---

## 🧠 Custom Hooks

- Custom hooks are user-defined functions that reuse hook logic.
- They start with `use` (e.g., `useForm`, `useToggle`).
- Help keep components clean and logic reusable across files.
- Can combine multiple hooks inside one custom hook.

**Common use cases:**
- Form handling
- Toggle states
- Data fetching
- Debouncing

---

## 🛣 React Router (v6+)

React Router is a library for adding routing to React applications.

- **BrowserRouter** is the base component that wraps the app and enables routing.
- **Routes** define the set of available paths.
- **Route** components specify which component renders for a given path.
- **Link** components are used for navigation without page reloads.
- **Dynamic Routes** allow use of URL parameters (e.g., `/user/:id`).
- A wildcard `*` path is used for 404 or "Not Found" pages.
- Hooks like `useNavigate`, `useParams`, and `useLocation` help interact with routes.

### # Introduction

```bash
npx create-react-app my-app
cd my-app
npm start
````

Folder structure includes `src/`, `public/`, `App.js`, and `index.js`.

## Creating a React Application

start the app with Create React App and render the `App` component in `index.js`.

## Components & Templates

Components are reusable parts of the UI. Templates use HTML tags like `<div>` and `<h1>`.

```js
function Header() {
  return <h1>My App</h1>;
}
```

# Dynamic Values in Templates

Use `{}` to insert JavaScript values in JSX.

```js
const name = 'Net Ninja';
<h1>Hello, {name}!</h1>;
```

# Multiple Components

Use different files for components and include them in `App.js`.

```js
import Navbar from './Navbar';
import Home from './Home';

function App() {
  return (
    <>
      <Navbar />
      <Home />
    </>
  );
}
```

# Adding Styles

Apply CSS via class names or inline styles:

```js
<h1 style={{ color: 'blue' }}>Hello</h1>;
```

# Click Events

Attach event handlers like `onClick` to elements.

```js
<button onClick={() => alert('Clicked!')}>Click me</button>;
```

# Using State (useState)

Manage data inside components that can change.

```js
const [count, setCount] = useState(0);
```

# Intro to React Dev Tools

Use a browser extension to inspect components, props, and state.

# Outputting Lists

Show lists using `.map()` and assign a `key` to each item.

```js
numbers.map(n => <li key={n}>{n}</li>);
```

# Props

Pass information into components.

```js
<Greeting name="Shaun" />;
```

# Reusing Components

Use the same component with different props to reuse it.

# Functions as Props

Give child components functions from the parent to use.

# useEffect Hook (Basics)

Run code after the component renders.

```js
useEffect(() => {
  console.log('Mounted');
}, []);
```

# useEffect Dependencies

Limit updates by including dependencies.

```js
useEffect(() => {
  console.log(count);
}, [count]);
```

# Using JSON Server

Set up a mock REST API for development.

# Fetching Data with useEffect

Load data when the component first shows.

```js
useEffect(() => {
  fetch('/blogs')
    .then(res => res.json())
    .then(data => setBlogs(data));
}, []);
```

# Conditional Loading Message

Show messages while data is loading.

```js
{isLoading ? 'Loading...' : <BlogList blogs={blogs} />}
```

# Handling Fetch Errors

Catch errors during fetch and show a message.

```js
fetch('/blogs')
  .then(res => res.json())
  .then(setBlogs)
  .catch(err => setError(err.message));
```

# Making a Custom Hook

Move shared logic into a reusable hook.

```js
function useFetch(url) {
  const [data, setData] = useState(null);
  useEffect(() => {
    fetch(url)
      .then(r => r.json())
      .then(setData);
  }, [url]);
  return data;
}
```

# The React Router

Set up routes for different components.

```js
<BrowserRouter>
  <Routes>
    <Route path="/" element={<Home />} />
  </Routes>
</BrowserRouter>
```

# Exact Match Routes

Ensure each route only matches the exact path.

```js
<Route path="/" element={<Home />} />
```

# Router Links

Navigate between pages using `<Link>` instead of `<a>`.

```js
<Link to="/create">Create Blog</Link>;
```

# useEffect Cleanup

Clean up side effects (like timers) on unmount.

```js
useEffect(() => {
  const timer = setTimeout(() => {}, 1000);
  return () => clearTimeout(timer);
}, []);
```

# Route Parameters

Get dynamic parts of the URL.

```js
const { id } = useParams();
```

# Reusing Custom Hooks

Use the same custom hook in different parts of your app.

```js
const blogs = useFetch('/blogs');
```

# Controlled Inputs (forms)

Link form fields to state variables.

```js
<input value={title} onChange={e => setTitle(e.target.value)} />;
```

# Submit Events

Handle form submission and prevent default reload.

```js
function handleSubmit(e) {
  e.preventDefault();
}
```

# Making a POST Request

Send new data to the server.

```js
fetch('/blogs', {
  method: 'POST',
  headers: { 'Content-Type': 'application/json' },
  body: JSON.stringify(blog),
});
```

# Programmatic Redirects

Change routes after an action using `useNavigate()`.

```js
const navigate = useNavigate();
navigate('/');
```

# Deleting Blogs

Remove items by calling DELETE on the server.

```js
fetch(`/blogs/${id}`, { method: 'DELETE' });
```

# 404 Pages & Next Steps

Show a NotFound page when no routes match:

```js
<Route path="*" element={<NotFound />} />;
```


##  Component Lifecycle (Class Components)

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

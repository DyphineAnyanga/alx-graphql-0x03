# alx-rick-and-morty-app

This is a React + Next.js project for working with the Rick and Morty API.  
Part of the **ALX GraphQL** learning track.

---

## 🧱 New Feature: Error Boundary

### 📁 File
`components/ErrorBoundary.tsx`

### 🔒 Purpose
This component provides a way to catch JavaScript errors in any part of the React component tree, log them, and display a fallback UI instead of crashing the whole app.

### 🔧 Usage

Wrap any component that may throw an error inside `<ErrorBoundary>` in your JSX:

```tsx
import ErrorBoundary from './components/ErrorBoundary';
import SomeComponent from './components/SomeComponent';

function App() {
  return (
    <ErrorBoundary>
      <SomeComponent />
    </ErrorBoundary>
  );
}

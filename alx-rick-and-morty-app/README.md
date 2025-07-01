# alx-rick-and-morty-app

This is a React + Next.js project for working with the Rick and Morty API.  
Part of the **ALX GraphQL** learning track.

---

## 🧱 New Feature: Error Boundary

## ⚙️ Application-Level Integration of ErrorBoundary

The `ErrorBoundary` component has been integrated into the app globally to catch rendering errors anywhere in the component tree.

### 📄 Modified File
`pages/_app.tsx`

### 🔧 How It's Used

We wrapped the main application component inside the `ErrorBoundary` to ensure any rendering issues are gracefully handled:

```tsx
import ErrorBoundary from '@/components/ErrorBoundary';
import type { AppProps } from 'next/app';

function MyApp({ Component, pageProps }: AppProps) {
  return (
    <ErrorBoundary>
      <Component {...pageProps} />
    </ErrorBoundary>
  );
}

export default MyApp;


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

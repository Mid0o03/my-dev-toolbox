# Next.js App Router

## File Conventions
- `page.js`: Unique UI of a route.
- `layout.js`: Shared UI for a segment and its children.
- `loading.js`: Loading UI for a segment and its children.
- `error.js`: Error UI for a segment and its children.
- `not-found.js`: 404 UI.

## Server vs Client Components
- **Server Components (Default)**: Rendered on the server. No `useState`, `useEffect`. Access to backend resources.
- **Client Components**: Use `"use client"` at the top. Interactive, use hooks.

## Data Fetching
```javascript
// Server Component
async function Page() {
  const data = await fetch('https://api.example.com/data');
  const res = await data.json();
  return <div>{res.name}</div>;
}
```

## Routing
- `Link`: `<Link href="/dashboard">Dashboard</Link>`
- `useRouter`: `const router = useRouter(); router.push('/home');` (Client only)
- `usePathname`, `useSearchParams`.

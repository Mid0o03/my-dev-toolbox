# State Management (Zustand & Redux)

## Zustand (Simple & Fast)
```javascript
import { create } from 'zustand'

const useStore = create((set) => ({
  count: 0,
  inc: () => set((state) => ({ count: state.count + 1 })),
  dec: () => set((state) => ({ count: state.count - 1 })),
}))

function Counter() {
  const { count, inc } = useStore()
  return (
    <div>
      <span>{count}</span>
      <button onClick={inc}>one up</button>
    </div>
  )
}
```

## Redux Toolkit (Standard for large apps)
- **Store**: The single source of truth.
- **Slice**: Contains logic for a specific feature.
- **Actions**: Plain objects that describe what happened.
- **Reducers**: Functions that determine state changes based on actions.

```javascript
const counterSlice = createSlice({
  name: 'counter',
  initialState: { value: 0 },
  reducers: {
    increment: state => { state.value += 1 },
  },
})
```

## When to use what?
- **Local State (`useState`)**: Tab state, form inputs, local UI.
- **Context API**: Deeply nested components, theme, user auth (slow for high-frequency updates).
- **Zustand**: Most mid-to-large apps. Excellent performance, no boilerplate.
- **Redux**: Extremely large apps with complex debugging needs.
- **React Query/SWR**: Server state (fetching, caching, syncing).

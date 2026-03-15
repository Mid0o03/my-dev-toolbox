# React Hooks Cheat Sheet

## Basic Hooks
- `useState(initialState)`: State management. `const [state, setState] = useState(initial);`
- `useEffect(effect, dependencies)`: Side effects. `useEffect(() => { ... return () => cleanup; }, [dep1, dep2]);`
- `useContext(ContextObject)`: Context consumption. `const val = useContext(MyContext);`

## Additional Hooks
- `useRef(initialValue)`: Persistent mutable value (ref). `const myRef = useRef(null);`
- `useMemo(() => compute, deps)`: Memoize expensive computations.
- `useCallback(fn, deps)`: Memoize functions.
- `useReducer(reducer, initialArg, init)`: Complex state logic. `const [state, dispatch] = useReducer(reducer, initial);`
- `useLayoutEffect`: Same as `useEffect` but fires synchronously after all DOM mutations.

## Custom Hooks
Create a hook to reuse stateful logic:
```javascript
function useWindowSize() {
  const [size, setSize] = useState(window.innerWidth);
  useEffect(() => {
    const handleResize = () => setSize(window.innerWidth);
    window.addEventListener('resize', handleResize);
    return () => window.removeEventListener('resize', handleResize);
  }, []);
  return size;
}
```

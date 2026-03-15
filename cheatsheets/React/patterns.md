# React Design Patterns

## Presentational & Container Components
- **Presentational**: Concerned with how things look. Props only.
- **Container**: Concerned with how things work. Fetching data, managing state.

## Higher-Order Components (HOC)
A function that takes a component and returns a new component.
```javascript
const withLogging = (WrappedComponent) => {
  return (props) => {
    console.log('Props:', props);
    return <WrappedComponent {...props} />;
  };
};
```

## Render Props
A component with a render prop takes a function that returns a React element and calls it instead of implementing its own render logic.
```javascript
<DataProvider render={data => (
  <h1>Hello {data.name}</h1>
)}/>
```

## Compound Components
Components that work together to form a unit (e.g., Select & Option).
```javascript
<Menu>
  <Menu.Item>Home</Menu.Item>
  <Menu.Item>Settings</Menu.Item>
</Menu>
```

## Controlled vs Uncontrolled
- **Controlled**: React state is the "single source of truth" for form data.
- **Uncontrolled**: DOM handles the form data. Use `useRef` to access.

# TypeScript Utility Types

TypeScript provides several utility types to facilitate common type transformations.

- `Partial<T>`: Constructs a type with all properties of T set to optional.
- `Required<T>`: Constructs a type with all properties of T set to required.
- `Readonly<T>`: Constructs a type with all properties of T set to readonly.
- `Record<K, T>`: Constructs an object type whose property keys are K and whose property values are T.
- `Pick<T, K>`: Constructs a type by picking the set of properties K from T.
- `Omit<T, K>`: Constructs a type by picking all properties from T and then removing K.
- `Exclude<T, U>`: Excludes from T those types that are assignable to U.
- `Extract<T, U>`: Extracts from T those types that are assignable to U.
- `NonNullable<T>`: Excludes null and undefined from T.
- `Parameters<T>`: Obtains the parameters of a function type in a tuple.
- `ReturnType<T>`: Obtains the return type of a function type.

```typescript
interface Todo {
  title: string;
  description: string;
}

const todo1: Partial<Todo> = {
  title: "organize desk",
};
```

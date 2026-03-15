# TypeScript Basics

## Basic Types
- `boolean`: `let isDone: boolean = false;`
- `number`: `let decimal: number = 6;`
- `string`: `let color: string = "blue";`
- `Array`: `let list: number[] = [1, 2, 3];` or `Array<number>`
- `Tuple`: `let x: [string, number] = ["hello", 10];`
- `Enum`: `enum Color {Red, Green, Blue}`
- `Any`: `let notSure: any = 4;`
- `Void`: `function warnUser(): void { ... }`

## Interfaces vs Types
- **Interface**: Primarily for objects and classes. Extendable.
```typescript
interface User {
  id: number;
  name: string;
}
```
- **Type**: For any type (primitives, unions, tuples).
```typescript
type ID = string | number;
```

## Functions
```typescript
function add(x: number, y: number): number {
  return x + y;
}

const myAdd = (x: number, y: number): number => x + y;
```

## Generics
```typescript
function identity<T>(arg: T): T {
  return arg;
}
```

# ES6+ Essentials

## Destructuring
```javascript
// Objects
const { name, age } = user;
const { name: userName } = user; // Rename

// Arrays
const [first, second] = list;
const [head, ...tail] = list; // Rest operator
```

## Spread Operator
```javascript
// Copy/Merge Objects
const newUser = { ...user, id: 1 };

// Copy/Merge Arrays
const newList = [...list, 4];
```

## Optional Chaining & Nullish Coalescing
```javascript
// Avoid "cannot read property of undefined"
const work = user?.job?.title;

// Default value only if null or undefined
const name = user.name ?? "Anonymous";
```

## Map & Set
```javascript
const myMap = new Map();
myMap.set('id', 1);

const mySet = new Set([1, 1, 2]); // [1, 2]
```

## Template Literals
```javascript
console.log(`Hello ${user.name}!`);
```

## Arrow Functions
```javascript
const multiply = (a, b) => a * b;
```

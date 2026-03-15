# 📊 JavaScript: Array Methods

## 🔄 .map() -> Transform
Creates a NEW array by modifying each element.
\`\`\`javascript
const prices = [10, 20, 30];
const pricesWithTax = prices.map(p => p * 1.2); 
// Result: [12, 24, 36]
\`\`\`

## ✂️ .filter() -> Filter
Creates a NEW array with elements that pass the condition.
\`\`\`javascript
const expenses = [15, 50, 5, 120];
const highExpenses = expenses.filter(e => e > 20); 
// Result: [50, 120]
\`\`\`

## ➕ .reduce() -> Accumulate
Reduces the array to a SINGLE value (e.g., total sum, average).
\`\`\`javascript
const cart = [10, 20, 30];
const total = cart.reduce((acc, current) => acc + current, 0); 
// Result: 60 (The 0 at the end is the initial value)
\`\`\`

## 🔍 Other highly useful methods:
* \`.find()\` : Returns the FIRST element that passes the test.
* \`.includes()\` : Checks if a value exists (returns true/false).
* \`.some()\` : Checks if AT LEAST ONE element passes the test.
* \`.every()\` : Checks if ALL elements pass the test.
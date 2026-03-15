# 🖥️ DOM Manipulation (Document Object Model)

## 🎯 Selecting elements
```javascript
// Most commonly used (selects the first matching element)
const btn = document.querySelector('.my-button');

// Selects ALL matching elements (returns a NodeList)
const allItems = document.querySelectorAll('.item');
```

## 🎨 Modifying content and classes
```javascript
const title = document.querySelector('h1');

// Change text content
title.textContent = "New Title!";

// Add / Remove a CSS class
title.classList.add('active');
title.classList.remove('hidden');

// Toggle (adds if missing, removes if present)
title.classList.toggle('dark-mode');
```

## 👂 Listening to events
```javascript
const button = document.querySelector('button');

button.addEventListener('click', (event) => {
    // Prevents page reload if it's inside a form
    event.preventDefault(); 
    console.log("Button was clicked!");
});
```

## 🏗️ Creating & Removing Elements
```javascript
// Create a new element
const newDiv = document.createElement('div');
newDiv.id = 'dynamic-id';
newDiv.textContent = 'I was born from JS!';

// Add to the DOM
document.body.appendChild(newDiv);

// Remove an element
newDiv.remove();
```

## 🌳 Traversing the DOM
```javascript
const el = document.querySelector('.item');

const parent = el.parentElement;
const children = el.children; 
const closest = el.closest('.container'); // Finds nearest parent matching selector
```

## ⚡ Event Delegation
Avoid adding listeners to every single item. Add one to the parent!
```javascript
const list = document.querySelector('ul');

list.addEventListener('click', (e) => {
  if (e.target.matches('li')) {
    console.log('Li clicked:', e.target.textContent);
  }
});
```
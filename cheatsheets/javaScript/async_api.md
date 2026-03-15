# 🌍 Async & Fetch API

## 🚀 The Perfect Pattern (Async / Await + Try / Catch)
```javascript
async function getData(url) {
    try {
        const response = await fetch(url);
        
        if (!response.ok) {
            throw new Error(`HTTP Error: ${response.status}`);
        }
        
        const data = await response.json();
        return data;

    } catch (error) {
        console.error("API issue:", error.message);
    }
}
```

## 🔗 Promise.all (Parallel requests)
```javascript
const [users, posts] = await Promise.all([
  fetch('/users').then(res => res.json()),
  fetch('/posts').then(res => res.json())
]);
```

## 🛑 AbortController (Cancel request)
```javascript
const controller = new AbortController();

fetch(url, { signal: controller.signal });

// Cancel the request later
controller.abort();
```

## 🛠️ Delay Helper (Sleep)
```javascript
const delay = (ms) => new Promise(res => setTimeout(res, ms));

await delay(2000); // Wait 2 seconds
```
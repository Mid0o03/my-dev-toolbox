# Express.js Patterns

## Basic Setup
```javascript
const express = require('express');
const app = express();

app.use(express.json()); // Body parser

app.listen(3000, () => console.log('Server running on port 3000'));
```

## Middleware
Functions that have access to `req`, `res`, and `next`.
```javascript
app.use((req, res, next) => {
  console.log(`${req.method} ${req.url}`);
  next();
});
```

## Routing
Organizing routes using `express.Router()`.
```javascript
const router = express.Router();
router.get('/users', (req, res) => { ... });
module.exports = router;
```

## Error Handling
Middleware with four arguments.
```javascript
app.use((err, req, res, next) => {
  console.error(err.stack);
  res.status(500).send('Something broke!');
});
```

## Common Middlewares
- `cors`: Enable CORS.
- `helmet`: Secure app by setting various HTTP headers.
- `morgan`: HTTP request logger.
- `express-validator`: Input validation.

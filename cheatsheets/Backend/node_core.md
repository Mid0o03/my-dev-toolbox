# Node.js Core Concepts

## Event Loop
- **Node.js**: Single-threaded, non-blocking, asynchronous.
- **Phases**: Timers, Pending Callbacks, Idle/Prepare, Poll, Check, Close Callbacks.

## Common Core Modules
- `fs`: File system operations (read/write files).
- `path`: Utilities for working with file and directory paths.
- `http`/`https`: Creating servers and making requests.
- `os`: Operating system information.
- `crypto`: Cryptographic functionality.
- `events`: EventEmitter class for custom events.

## Promises & Async/Await
```javascript
const fs = require('fs').promises;

async function readFile() {
  try {
    const data = await fs.readFile('file.txt', 'utf8');
    console.log(data);
  } catch (err) {
    console.error(err);
  }
}
```

## Buffer & Streams
- **Buffer**: Temporary memory to store raw binary data.
- **Streams**: Reading/writing data in chunks (Readable, Writable, Duplex, Transform).

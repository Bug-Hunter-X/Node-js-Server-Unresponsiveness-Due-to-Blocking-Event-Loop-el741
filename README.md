# Node.js Server Unresponsiveness

This repository demonstrates a common Node.js issue: blocking the event loop, leading to server unresponsiveness.  The `bug.js` file contains code that simulates a long-running task, causing the server to hang for 5 seconds on every request.  This is resolved in `bugSolution.js` using asynchronous operations to prevent blocking.

**Problem:** Synchronous operations within the request handler block the event loop, preventing Node.js from handling other requests.  This leads to poor performance and a potentially unresponsive server.

**Solution:**  Utilize asynchronous programming techniques (e.g., `setTimeout`, `setImmediate`, or promises/async/await) to avoid blocking the event loop.  This ensures that Node.js can continue handling requests even while long-running tasks are being executed.

This example highlights the importance of asynchronous programming in Node.js for building scalable and responsive applications.
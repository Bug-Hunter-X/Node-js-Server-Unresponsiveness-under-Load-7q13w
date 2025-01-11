# Node.js Server Unresponsiveness under Load

This repository demonstrates a common issue in Node.js applications where the server becomes unresponsive or hangs under a heavy load of requests. The problem stems from inefficient request handling, potentially leading to memory leaks or blocking the event loop. 

The `server.js` file contains the buggy code, while `server-solution.js` provides a corrected implementation that addresses the issue. The solution involves using techniques like asynchronous operations, proper resource management, and potentially employing a load balancer or process manager for scaling.

## Reproducing the Bug

1. Clone this repository.
2. Navigate to the project directory.
3. Run `node server.js`.
4. Simulate multiple concurrent requests using tools like `ab` or `wrk`.
5. Observe the server's response time and overall responsiveness.

## Solution

The solution lies in optimizing request handling. This often involves:

* **Asynchronous Operations:** Employ asynchronous functions to prevent blocking the event loop.
* **Resource Management:**  Ensure proper handling of resources like database connections and file descriptors.
* **Load Balancing/Process Managers:** For high-traffic applications, consider using a load balancer (e.g., Nginx) or a process manager (e.g., PM2) to distribute requests across multiple server instances.

Refer to `server-solution.js` for an implementation demonstrating a more efficient handling of requests, preventing the server from hanging under load.
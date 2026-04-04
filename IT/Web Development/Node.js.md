#js #web #back-end 
```bash
node app.js
```
**Node.js vs Browser**

| Feature                   | Node.js             | Browser     |
| ------------------------- | ------------------- | ----------- |
| **File System Access**    | Yes                 | No          |
| **Networking (TCP/UDP)**  | Yes                 | No          |
| **DOM Access**            | No                  | Yes         |
| **Global Object**         | `global`              | `window`/`self` |
| **Modules**               | CommonJS/ESM        | ESM/Scripts |
| **Environment Variables** | Yes (`process.env`) | No          |
| **Security**              | Full OS access      | Sandboxed   |
| **Package Management**    | npm/yarn            | CDN/Bundler |

**Node.js Architecture Diagram**
1. Client Request Phase
	- Clients send requests to the Node.js server
	- Each request is added to the _Event Queue_
2. Event Loop Phase
	- The Event Loop continuously checks the _Event Queue_
	- Picks up requests one by one in a loop
3. Request Processing
	- Simple (non-blocking) tasks are handled immediately by the main thread
	- Complex/blocking tasks are offloaded to the Thread Pool
4. Response Phase
	- When blocking tasks complete, their callbacks are placed in the _Callback Queue_
	- Event Loop processes callbacks and sends responses
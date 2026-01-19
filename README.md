## CS472-Node-Event-Loop
### Update the `README.md` file, to include the answers to the following questions:
1. What is LibUV?
2. How does Node.js handle I/O operations asynchronously? What role does the event loop play in this process?
3. What are the advantages and limitations of a single-threaded model?
4. What is the difference between `setImmediate(f)` and `setTimeout(f, Time)`? 
5. What is the difference between `process.nextTick(f)` and `setImmediate(f)`?
6. What is the difference between `process.nextTick(f)` and `queueMicrotask(f)`?
7. Name 10 of Node Core modules
8. Name 10 of Node Global objects
  
#### From your Terminal, navigate to the `test` folder, and run `npm i`
Write down your observation and explain what happens in Node when you run the following commands:
   1. `npm run start`  
   2. For Windows: `SET UV_THREADPOOL_SIZE=2 && npm run start`
   3. For MacOS: `export UV_THREADPOOL_SIZE=2 && npm run start`

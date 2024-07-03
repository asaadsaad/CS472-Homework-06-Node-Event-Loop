## CS472-Node-Event-Loop
### Update the `README.md` file, to include the answers to the following questions:
1. What is LibUV?
3. Explain the difference between `setImmediate(f)` and `setTimeout(f, Time)`? 
4. Explain the difference between `process.nextTick(f)` and `setImmediate(f)`?
5. Explain the difference between `process.nextTick(f)` and `queueMicrotask(f)`?
6. Name 10 of Node Core modules
7. Name 10 of Node Global objects
  
#### Navigate to the `test` folder, run `npm i`
Write down your observation and explain what happens in Node when you run the following commands:
   * `npm run start`  
   * For Windows: `SET UV_THREADPOOL_SIZE=2 && npm run start`
   * For MacOS: `export UV_THREADPOOL_SIZE=2 && npm run start`

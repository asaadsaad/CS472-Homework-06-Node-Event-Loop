## CS472-Node-Event-Loop
#### Question 1
Write your answers to the following questions:
1. What is LibUV?
2. How does Node.js handle I/O operations asynchronously? What role does the event loop play in this process?
3. What are the advantages and limitations of a single-threaded model?
4. What is the difference between `setImmediate(f)` and `setTimeout(f, Time)`? 
5. What is the difference between `process.nextTick(f)` and `setImmediate(f)`?
6. What is the difference between `process.nextTick(f)` and `queueMicrotask(f)`?
7. Name 10 of Node Core modules
8. Name 10 of Node Global objects

#### Question 2
Test understanding of the Event Loop phases, microtasks vs macrotasks. Given the following code:
```typescript
console.log("A");

setTimeout(() => {
  console.log("B");
}, 0);

Promise.resolve().then(() => {
  console.log("C");
});

process.nextTick(() => {
  console.log("D");
});

console.log("E");
```
1. Write down the exact order of the output.
2. Explain why the output occurs in that order.

#### Question 03
Given the following code:
```typescript
function heavyComputation() {
  let sum = 0;
  for (let i = 0; i < 5_000_000_000; i++) {
    sum += i;
  }
  return sum;
}

console.log("Server started");

setTimeout(() => {
  console.log("Timeout callback");
}, 0);

heavyComputation();

console.log("Server is ready");
```
1. Explain why setTimeout is delayed, even though it is scheduled with a delay of 0.
2. Explain why converting heavyComputation to async and using await does not fix the problem.
3. Exaplain how can we effectively fix the problem, so that the event loop is not blocked.
  
#### Question 04
From your Terminal, navigate to the `test` folder, and write down your observation and explain what happens in Node when you run the following commands:
   1. `npx tsx app.ts`  
   2. Windows: `SET UV_THREADPOOL_SIZE=2 && npx tsx app.ts` OR MacOS: `export UV_THREADPOOL_SIZE=2 && npx tsx app.ts`
   3. Windows: `SET UV_THREADPOOL_SIZE=10 && npx tsx app.ts` OR MacOS: `export UV_THREADPOOL_SIZE=10 && npx tsx app.ts`

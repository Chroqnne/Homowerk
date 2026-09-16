# Classwork feedback 20260911

**Student:** Jonathan
**Classwork:** Recursion and abstract data types (stack and queue)
**Date:** 2026-09-11

## Score

**87 / 100**

| Question | Score |
|---|---|
| Q1 Recursion (18) | 14 |
| Q2 Recursion in detail (20) | 20 |
| Q3 Stack (20) | 18 |
| Q4 Queue (26) | 19 |
| Q5 Applications (16) | 16 |

## Feedback on incorrect answers

**Q1 (a) definition of recursion (-1 mark)**
- Good - a function calling itself with a recursion step and a base step. Add that each call works on a smaller or simpler version of the same problem, which is what guarantees convergence.

**Q1 (c) why a stack suits recursion (-3 marks)**
- LIFO and the reverse return order are correct. Missing the mechanism: each call pushes an activation record (return address + local variables), and records are popped in reverse order so the most recent call returns first.

**Q3 (b) stack implementation (-2 marks)**
- The logic is correct. Two problems: (1) the body of pop() is not indented - 'global topPointer', 'item = None' and 'if topPointer >= 0:' sit at the left margin, so the function will not run; (2) 'stackFull : int' is not valid Python and the array is built from a variable that has not been assigned. Some lines also use non-breaking spaces from pasting, which Python rejects.

**Q4 (b) circular array (-2 marks)**
- Wrap-around and reuse of freed space are explained and both pointers are described. Missing: this avoids shifting the remaining elements, which an ordinary array would require after every dequeue.

**Q4 (c) circular queue (-5 marks)**
- Full/empty checks and 'global' are correct, but the wrap-around compares the pointer against QueLen - 1 (the number of items) instead of the array capacity QueFul - 1. With an empty queue neither branch is taken, so enqueue stores nothing at all. Use RearPointer = (RearPointer + 1) % QueFul.

## Notes (no marks deducted)

**Q1 (b) base case**
- Full marks. Stating that the recursion stops and converges to a definite result answers the question. You could also add that the base case is the simplest instance, solved without any further recursive call.

**Q2 (a) to_binary unfolding**
- Full marks. Your expression evaluates to "1101" and the nesting order is shown correctly, so the unfolding is right. Writing the final string out explicitly would make the answer clearer still.

**Q3 (c) another use of a stack**
- Full marks - the question did not require a reason. Note that 'entering and deleting text' is very close to the undo example already given in the question; a clearly different application (browser back button, call stack, balanced brackets) would be a stronger answer.

**Q4 (a) FIFO / enqueue / dequeue**
- Full marks. Your answer was placed in a small box inside the answer frame - it covers FIFO and the difference between enqueue and dequeue. Please put answers directly in the answer frame next time so they are not missed.

---
_Detailed notes are also added as comments in your Word file._

# Classwork feedback 20260918

**Student:** Jonathan
**Classwork:** Abstract data types - binary tree, linked list, circular queue
**Date:** 2026-09-18

## Score

**91 / 100**

| Question | Score |
|---|---|
| Q1 Binary tree concepts (25) | 24 |
| Q2 Linked list (35) | 30 |
| Q3 Circular queue programming (40) | 37 |

## Feedback on incorrect answers

**Q1 (f) choice of key (-1 mark)**
- You cover uniqueness, comparability, the duplication of surnames and the effect on searching. The final mark is for a closing point about the consequence - for example that duplicate keys make two records impossible to tell apart, so the search cannot identify a single student.

**Q2 (b) null pointer (-1 mark)**
- The end-of-list meaning and the value -1 are both correct. The missing point is that it specifically marks a node with no successor - the last node of the list - and that the same value is used to terminate the free list.

**Q2 (c) insertAtStart (-2 marks)**
- Four of the five lines are correct. The second line is wrong: to move `heapStartPointer` on you must follow the free-list pointer, so it is `heapStartPointer <- myLinkedListPointers[heapStartPointer]`. `myLinkedList` holds the data, not the pointers, so as written it would take a data value and use it as an array index.

**Q2 (d) removeItem (-1 mark)**
- The WHILE condition, the first-node case and the return to the heap are all correct. One mark is lost for the spelling: `previousPoiter` is not a declared identifier, so the line would not run as written.

**Q2 (e) returning a node to the heap (-1 mark)**
- Returning the node to the beginning of the free list, and the fact that it can be used again, are credited. Missing: the two pointer updates that actually do it - the removed node's pointer is set to the old `heapStartPointer`, and `heapStartPointer` is then moved to the removed node.

**Q3 (b) enqueue wrap-around (-2 marks)**
- The global declaration, the full check and storing the item at `rear` are all correct. The wrap-around loses its marks: when `rear` is 7 it must become **0**, not 1, because the list has eight slots numbered 0 to 7. Setting it to 1 strands index 0 after the first wrap, so one slot is lost and the queue would report "Queue full" while a slot is still free. Your screenshot shows `front = 0` in `dequeue()`, so this looks like a slip in the written answer rather than in your code - check the same line in `enqueue()`.

**Q3 (f) three further dequeue calls (-1 mark)**
- The three "EMPTY" values and the reason - that the queue holds no remaining orders - are correct. The final mark is for naming the check in the code: `dequeue()` tests `orderCount == 0` and returns "EMPTY" **before** it reads the list, which is why the call is safe.

## Notes (no marks deducted)

**Q1 (b) level and height**
- Full marks. Level 3 and height 2 are both correct. To make the answer complete in the exam it also helps to state that the root is counted as level 1, which is what makes 45 level 3, and to define height as the number of edges on the longest path from the root to the deepest leaf.

**Q1 (e) inserting 40**
- Full marks. Your answer - 45, left child - is correct, and the three comparisons are right.

**Q2 (a) trace table**
- Full marks. Every itemPointer is correct, and `-1` in the last row is the right value: the node holding 61 is the last node in the list, so its next pointer is the null pointer. It is worth adding in words that the search stops and returns the index once the item is found.

**Q3 (c) dequeue wrap-around**
- Full marks. Your screenshot shows `front = 0` when front is 7, which is correct, so this part is credited even though the written answer says 1.

**Q3 (e) screenshot**
- Full marks. The output appears in the correct order, and the screenshot also shows the code, which was useful when checking the wrap-around above.

---
_Detailed notes are also added as comments in your Word file._

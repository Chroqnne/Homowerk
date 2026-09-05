# Classwork feedback 20260904

**Student:** Jonathon
**Classwork:** Algorithms - Big-O, linear search, binary search, insertion sort
**Date:** 2026-09-04

## Score

**82 / 100**

| Question | Score |
|---|---|
| Q1 | 27/30 |
| Q2 | 35/40 |
| Q3 | 20/30 |

## Feedback on incorrect answers

**Q1 (a)(ii) (-3 marks)**
- The returned value is 3, not 5 (and the index of 8 is 2, not 3). The loop sets found=True at i=2, then i is incremented to 3 before the loop exits.

**Q2 (a) (-5 marks)**
- upper set to len(data) instead of len(data) - 1 - mid can reach len(data) and cause an IndexError at the boundary.

**Q3 (a) (-6 marks)**
- Outer loop hard-coded as 'range(1, 10)' instead of 'range(1, len(values))' - the function only works for lists of exactly 10 items.

**Q3 (b) (-4 marks)**
- count = count + 1 placed outside the while loop, so it adds 1 per item instead of per shift; also keep 'range(1, len(values))'.

---
_Detailed notes are also added as comments in your Word file._

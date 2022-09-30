# Memory Management
---
### There are only
- Numbers
  - chars
  - inttegers
  - boolean
  - floating point
  - instructions
    - When compiled are just numbers
- Basic math
  - In instructions 
- Moving number around
  - In instructions 

1. Allocate
2. Deallocate

|          | code and static vars |    stack    |         heap        |
|:--------:|:--------------------:|:-----------:|:-------------------:|
| location | always same (static) |    varies   |        varies       |
|   size   |      always same     | always same |        varies       |
| lifetime |       infinity       | block scope | as long as you want |

---

## Garbage Collector
- Better performance
- Hard to remember when to delete

**If you can't reach it via stack or pointer, it's garbage**



[Week 2](../w2.md)

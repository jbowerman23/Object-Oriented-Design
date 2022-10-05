# Object Ownership & Smart Pointers

[Back to Homepage](../index.md)<br>
[Back to Week 3](../w3.md)

---

## Relationship Type Review

Is-a: Inheritance
- 1:1 Cardinality
- association= lifetime
  - child owns stuff from parent

Holds-a
- Contains

Has-a
- Type dependence 
  - needs something specifici about the other object  

---

## Smart Pointers

```c++
#include <memory>

std::unique_ptr // 
std::shared_ptr // Can have multiple shared pointers that point to the same object
std::weak_ptr

shared_ptr blah(new Person()); // Shared pointer contains person pointer, also creates a reference count to keep track of how many pointers are pointing at that thing.

// When reference count becomes zero it will delete Person

```
Unique pointer
- deletes pointer in destruction

Share pointers have share ownership
- Deletes pointer if no other smart pointer points to it
- last person to leave turns off the lights
- Holds a relationship

Weak pointer
- 

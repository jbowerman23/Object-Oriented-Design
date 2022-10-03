# Unit Testing and Encapsulation

[Back to Homepage](../index.md) <br>
[Week 2](../w2.md)

---

### Types of Testing
- Unit
  - Testing small parts of code
  - Smallest thing you can test stand alone
- Functional

- Intergration
  - Functions that call other functions
  - Classes that use other classes  
- End to End
  - Multiple apps working together

## Unit Tests
- Everything works like I think its supposed to
- Incorrect usage has fallback

```c#

/*
Class invariant: Value is always between 0.0 and 100.0 (Guarenteed, promise)
  Write tests to verify this is always true
*/

class Percentage {
  public double Value {
    get{return value;};
    set(double newValue) {
      if (newValue < 0.0 || newValue > 100) {
        throw newInvalidArgumentException();
      }
      value = newValue;
    }
  } 
}

```
**Class invariants should be true throughout the life of the object** <br><br>

constructor <br>
|<br>
|<br>
| Method Calls<br>
|<br>
|<br>
destructor / Garbage collector



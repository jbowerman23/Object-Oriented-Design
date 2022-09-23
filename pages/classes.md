# Classes in C++ and C#
---

## Review 

Encapsulation
- Separate interface from implementation
- Sepatate what from how

Class Designer vs. Client
- When someone else designs cant see inside the box
- Care more about the inputs and outputs, public interface

---

# SOLID
- **S**ingle Responsibility Prinicle
  - Each class should have one specific theme/responsibility
  - Keep it simple/focused
  - Should only have one reason to change

- Open/Closed Principle
- Liskov Substitution Principle
- Interface Segregation Principle
- Dependencey Inversion Principle

![Computing Systems!](https://devopedia.org/images/article/177/8101.1558682601.png)

---

# C++

Elements to C++:
- include statments
- comments
- functions
- classes
  - default everything private 
- structs
  - default everything public

```c++
#include <iostream>
// comments in code

int functionName(int variable){
  // stuff
}

class className {
  //stuff
}

struct Person {
  //stuff
}

```

Example struct
----

```c++
struct Point{
  int x;
  int y;
};

Point p;
Point p2;

p.x
p2.x

```

Example Class
----

```c++
class Point{
  private:
    int x;
    int y;
   
  public:
    int getX() const;
};

Point p;
Point p2;

p.x
p2.x

```

When function is a member of a class, methods (member function) get access to other private variables in the class

If you have a getter can replace the code later.
Keep variables private.
Getters public 

**.h files** contains skeleton of the class
- declarations of functions
- Mediocore interface explanation
  - Doesn't really have implementation

**.cpp file** shows implementation 

## Constructor and Destructors
- Consturctor has same name as class
  - No return type
  - special method
  - Initalize object
    - Default values
  - Setting up object with stuff in it 
- Destructor called when you stop using your instance of this class
  - Clean up allocated memory
  - ensure resources are unlocked

```c++
class Point{
  Point(int, int); // Constructor
  ~Point(); // Destructor
  
  int x;
  int y;
  
  public:
    int getX() const;
};
```





[Back to Week 1](../w1.md)

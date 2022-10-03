# Classes in C++ and C#

[Back to Homepage](../index.md) <br>
[Back to Week 1](../w1.md)

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
---

## Memory Allocation
Stack is efficent but infelxible
- Always add to next spot on stack

<br> Heap much more flexible
- Can find free space avaliable 
- A lot slower to put something on the heap
- Can have enough memory, not enough consecutive memory

Can use stack, but once you leave the function, the stack gets cleaned up
When using heap have to manually delete or else you get memory leaks

```c++
Point p; // goes on stack
Point *p2 = new Point(3,4); // pointers go on heap, new says find memory on heap

```

# C#

Value types

Reference types

Has a garbage collector
- use more cpu power bc it is doing tasks in the background

no equivalent to a destructor

```c#

private static void downloadGoogle()
{
  WebClient client = new();
  string webpage = client.DownloadString("https://www.google.com/")
  File.WriteAllText("google.html", webpage);
}

```

WIth C# all class related stuff goes into one file a .cs file

```c#
internal class Point
{
  private int x; // each individual thing needs to be tagged with public/private
  private int y;
  
  public int X { get; private set; } // Properties: things that look like fields but have built in getters and setters
  public int Y { get; private set; }
  
  public Point(int x, int y)
  {
    this.x = x;
    this.y = y;
  }
}

```

namespace helps organized code, if multiple classes with same name

static methods dont have to create an instance to used that method

cant have null variables without ? 

```c#

internal calss PizzaOrder
{
  private string? cheeze;
  private string? sauce;
  private bool isGlutenFree;
  private int diameter = 14;
  private List<String> toppings;
  
}


```







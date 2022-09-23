# Intro 
---

## Types of Programming

### Structured:
- break apart into functions/subroutines.modules

### Object Oriented Programming:
- combining data and code into self contained groupings

### Functional:
- use of math like functions to organize code into reuseable blocks

---

## Uses
- Games
- GUIs
- Web Services

All are long-lived state frequently accessed

---

## Classes
- Constructor
- Method
- fields/properties/memer variable
- instances 
  - a specific one of a blueprint
- access restrictions

---

## Encapsulation
  
  ```c++
  #include <iostream> // Allows us to read to or write from the console
  #include <istream>
  
  string readContnents(string filename);
  ifstream input(filename);
   
  int fileId;
  int readPos;
   
  int i;
  input >> i; 
  
  cin >> i;
  ```
 
Have classes to group and create simplier interfacee

- Show interface
- Hide implementation

##ifstream:
- subclass of istream
- cin is a different istream sub class

---

## Cohesion vs Coupling
- Cohesion is how well things go together
- Coupling is how much different things are mixed together

Minimum interactions needed, coupling is necessary, but want to minimuze it. <br>
0% coupling is just a bunch of different functions that dont interact with each other at all. <br>
Want to try to keep functions small (about 10 lines).

```c++
class Student {
  private:
  string firstName;
  string lastName;
  char middleInitial;
  long studentId;
  string major;
  
  public:
  string makeFormalName(){
    return lastName + ", " + firstName + " " + middleInitial + "."
  }
  
}

```

---

## Class designer vs. Client
- Class designer, come up with interface, implementation
- Client, has to use the class

---

[Back to Week 1](w1.md)

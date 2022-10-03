# Programming by Contract

[Back to Homepage](../index.md) <br>
[Back to Week 2](../w2.md)

---
### Put the responsibility on the client to fufill the preconditions and postconditions
- Must Trust Clients to do it right

Classes: Levels of Complexity
---
1. POD (Plain Old Data)
    - Dont have to worry about designing

2. Computed Fields
    - Only rely on data inside class
      - Internal data

3. Uses contained objects
    - Objects that contain other complicated objects

4. Orchestrates interactions between objects
    - Two different objects, need to do something with both of them in a specific order or way

---

Room Class <br>
Person Class<br>

```c#
List<Person> occupants
  int maxOccupancy;     // If at max occ want to reject new person entering room
  
Room currentRoom;

```

How do you know if room can accept person? Can person move? Updating of fields? <br>

Create mediator that helps keep track of everything. Knows about other objects, updates rooms and persons.

---

Programming by Contract
---
Design by Contract, other name
- Original idea created with eiffle
- Preconditions: needs to be true beforehand
  - In order to remove something from the stack or queue, there needs to be something in the stack or queue
- Postconditions: will be true after method is executed
  - For end user to help them understand the class
  - File.close()
    - file will no longer be locked
    - Write operations with this object will fail
  - remove() breaks any open iterators

- Class invariants
  - True for the lifetime of instances 
  - Health is always non-negative for player in video game
- Implementation invariants
  - Implementation notes  
- Interface invariant

### Method
- Name
- Parameters
- Preconditions
- Postcoditions
- budy

BCPL (Basic Common Programming Language) -> B -> C -> C++ -> Java -> C#

- Comments
- Assert
- Language Feautre
    - Usually compiled out in producted (Assert too)  

----

## Defensive Programming
- Have a back up plan to every single case
- Leads to exceptions
- Not trusting user to not do this
- Many if statements, null checks
- Will never go super wrong, cause all cases are covered

- All exceptions add overhead, slower







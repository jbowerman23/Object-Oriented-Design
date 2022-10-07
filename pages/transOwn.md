# Transferring Ownership

[Back to Homepage](../index.md) <br>
[Back to Week 3](w3.md)

----

## Smart Pointers
- unique
  - only one  
- shared
  - delete when last one is destroyed
- weak
  - option to get a shared pointer

- allows for easier memory management than raw pointers
- allows more control than garbage collection


```c++
class List {
  unique_ptr<int[]>backingArray;
}

```

## Copy

## Move

```
RegistrationForm -> unique_ptr(Person) createPerson() -> return unique_ptr(new Person())

// Because person will outlive form, maybe return pointer as person will be on heap
// Dont want to tie their lifetimes together

make_unique<Person>(...); // Creates a new person without using new keyword

```
